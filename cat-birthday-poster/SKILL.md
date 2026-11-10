---
name: cat-birthday-poster
description: Create a personalized vintage Tom and Jerry comic-book birthday poster by editing the bundled poster template with the user's real cat photo while preserving the cat's recognizable identity and photographic appearance. Use when the user requests a Tom and Jerry birthday poster or closely equivalent birthday artwork for their cat; do not use for ordinary pet edits, pet health questions, commercial artwork, or unrelated image requests.
license: Personal non-commercial use only; third-party characters are not licensed. See LICENSE.txt.
metadata:
  author: JoMeow the black cat
  version: "3.0.1"
---

# Tom and Jerry Cat Birthday Poster

Communicate in the user's language. Translate this skill's example questions when asking them.

The poster is made for a personal, non-commercial celebration of the user's cat. Never present it as official, licensed, endorsed, or suitable for sale, advertising, or merchandise. Keep this policy out of the image-tool brief.

## Capability Gate

Before any image task, verify that the agent can look at the supplied images and at the generated output itself (a file path alone is not enough unless an image-viewing mechanism lets the agent actually see it), and that reference-guided image editing is available. If either is missing, stop before generating and explain what is missing. Never claim an image was inspected, edited, or generated when it was not.

## Base Images

Every new poster edits a bundled base image. Never recreate the scene from text alone.

| Ratio | Base image | Comfortable number of cats |
|---|---|---|
| `4:3` (default) | `assets/templates/poster-4x3.png` | up to 5 |
| `1:1` | `assets/templates/poster-1x1.png` | up to 3 |
| `3:4` | `assets/templates/poster-3x4.png` | up to 2 |
| Any other ratio the user explicitly requests | the template with the nearest ratio, extended or cropped with the reflow notes in `references/brief-template.md` (best effort; tell the user) | as for that template |

Offer as standard choices only the ratios whose template file exists. If the included cats exceed the number in the table, send the capacity message from `references/multi-cat.md` once; if the user still wants all of them, proceed and make the cats as large as the free area allows.

## Core Requirements

These seven requirements decide whether a poster is acceptable. Step 6 checks them.

1. **Base art stays.** Except for the changes listed here, everything in the base image stays as shown: Tom, Jerry, the gray mouse, both mice's cake-slice caps with their head candles, the candle on top of the cake, the cake structure and its frosting divider, the table, the small cover marks (the MEOW badge, the APRIL 21 label, the c.a.t.'s script, the Purrco script and the 10¢ price box), and the background. The template also carries two placeholders: the headline `Party Time!` and the name `Tom` on the cake's lower band. Permitted changes: adding the selected cats and their accessories, replacing or removing the headline placeholder, replacing or removing the name placeholder, moving the c.a.t.'s and Purrco scripts a short distance when a long headline needs the room, replacing the cake greeting only when the user asked, and (ratios without a template) extending the canvas and moving or uniformly scaling the illustrated group as one unit. An explicit user request may authorize another localized change; whatever the user asked to change is then removed from the brief's protected list (slot rules in `references/brief-template.md`). Protect all three candles by default; read `references/candles.md` only when the user asks to change the candles or explicitly asks to show the cat's age with candles (a stated age alone is not such a request).
2. **Cats stay themselves.** Each selected cat appears exactly once and is recognizably the same real cat (coat, markings, face shape, eyes, nose, ears). Cats stay photographic: real fur, eyes, nose, whiskers, with restrained vintage-film treatment. Clothing and accessories the cat wears in the photo are part of its identity and stay (`references/accessory-index.md` covers collisions with the party items). Nothing from the photo's surroundings (floor, furniture, wall, bedding, cast shadow) enters the poster.
3. **Cats are the focal subject, on the right.** Tom is on the left, the cake near the center or center-left, every selected cat to the right of them. With a single cat, its head is at least comparable in size to Tom's head. With several cats, every honoree gets the largest portrait scale within the group (comparable among co-honorees, companions smaller) and the cat group as a whole is more prominent than Tom. In every case no cat covers Tom, the mice, the cake or its lettering. The illustrated table keeps its base size and is never extended into a platform for a cat. Two arrangements are both acceptable: (a) large head-and-upper-body portraits entering from the right or lower right, in front of the right end of the table, their bodies covering that part of the table and running down to the canvas edge; (b) the cats sitting naturally on the table with whole bodies, paws and contact shadows visible. Choose the one that keeps the cats larger and clearer, and never switch a layout that already works to the other. Never cut a body off at a line inside the picture (for example a torso ending flat at the tabletop or its edge), and never draw the table over a cat. Keep recognizable clothing or body markings visible where feasible. Do not preserve the source photo's full pose at the cost of cat prominence unless the user asks.
4. **Hat and collar.** Each honoree wears exactly one conical party hat and its matching collar from one paired set (`references/accessory-index.md`), worn naturally, with identity features still visible. Where the cat already wears its own item in the hat or collar spot, the cat's own item stays and that party item is omitted; everything else the cat wears stays too.
5. **Text is correct.** Headline, cake greeting and cake names match the values resolved in Step 4 and are readable. Without a headline, no headline appears.
6. **Canvas.** The artwork fills the canvas edge to edge in the requested ratio, with the base's pale-yellow-to-pale-blue gradient intact unless the user asks for a different background (then drawn in the cover's illustrated style), and no paper sheet, border or mockup.
7. **Two visual domains.** The illustrated domain (Tom, the mice, cake, table, background, lettering, and every added object that is not worn by a cat) keeps the cover's inked cel-animation look. The photographic domain is only the real cats and the accessories they wear. Do not carry ink outlines or flat fills onto cats, and do not photograph the illustrated parts.

### Illustrated Additions

Any added illustrated object matches the cover: simplified slightly irregular hand-drawn forms, clean continuous black ink contours at the weight of neighboring objects, flat saturated fills, minimal hard-edged cel shading, subtle newsprint grain and print-registration irregularity. Express material through drawn shapes, not photorealistic texture, gloss, bevels or glow. This does not apply to the cats or their worn accessories and does not allow redrawing the base art.

## Workflow

### Step 1 - Route the request

- **New poster:** a usable cat photo is available. Continue with Steps 2-7. If the photo is missing or unusable, or a multi-cat decision is open, use Step 2 first.
- **Revision of a delivered poster:** read `references/editing.md`, edit the last accepted poster, skip the new-poster inspection.
- **Several outputs:** produce exactly the requested count; ask once if the count is unclear. Never add unsolicited variants.
- **Process question** (brief, prompt, settings, explanation of a delivered poster): answer in text only, without inspecting, editing or redelivering the image. Say whether you are quoting the actual payload or reconstructing it.
- **Compliance question** (does element X meet the requirements?): inspect the named element in full, including every script it contains, and answer with the observable differences. Do not edit unless asked.
- A newly uploaded cat photo starts a new poster unless the user says it supplements or replaces the current one.

### Step 2 - Validate input and ask once

A usable cat photo is required. Ask all unresolved items in one message and never repeat a question that is already resolved or defaulted. Inspect the message and attachments first.

Items to ask about: the cat photo, the cat's name, a headline and the ratio. Present all four as equal numbered items in the same message, never the name as a sub-point of another item. Only the photo is required; if the user answers without the others, apply their defaults and do not ask again. Offer no other customization menus unless the user raises them.

Defaults: no name → the placeholder name is removed and the cake's lower band stays blank; no headline → the placeholder headline is removed; no ratio → `4:3`; one clear cat → that cat is the birthday cat and wears the hat.

Multiple cats in the photo, or several photos: read `references/multi-cat.md`.

**No usable photo** - translate and send:

> 1. **Photo (required)** - Please upload one or more clear photos in which the cat's appearance can be identified reliably.
> 2. **Cat's name** - What is your cat's name? The cake will show `Happy Birthday <Name>`. If you would rather not use one, say so and the cake shows only `Happy Birthday`.
> 3. **Headline** - Would you like a headline at the top of the poster (for example a short phrase)? If not, none is added.
> 4. **Canvas ratio** - `4:3` by default (list the other available ratios).
>
> Only the photo is required; for anything you skip, I will use the defaults.

If the image contains no cat, or the cat is too small, occluded, dark or blurry, say so under **Photo (required)** and ask for a clearer view of the face, coat colors and markings; add the optional items only if the user has not yet had the chance to answer them.

**One clear cat, items still unresolved** - say "I identified one clear cat and will use it as the birthday cat", then ask only the unresolved items from the list above, ending with: "You may reply 'use defaults.'"

### Step 3 - Analyze the cats and assign images

Write one short internal identity brief per selected cat: coat colors and distribution, distinctive markings, face shape, eye color and spacing, nose color, ear shape, build, asymmetry, and any clothing or accessories it wears. Do not invent unseen traits. Treat what the cat wears in the photo as identity features and keep it unless the user asks to remove it; `references/accessory-index.md` says what to do where it collides with the party hat or collar.

Decide which party items each honoree will wear: the pair by default, only one of them where the cat's own item holds the other spot, none if both spots are taken. Then choose a set for each honoree who wears at least one, using `references/accessory-index.md`.

Label every supplied image with one role, in attachment order:
- Image 1: the base image from "Base Images" - base to edit.
- Next: the selected cat photo(s) - identity reference only. When several photos show the same cat, use the fewest that add needed identity information.
- Next: the selected accessory file(s) - design reference for the party item(s) in use (the pair, or only the hat, or only the collar). Attach only the sets assigned to cats; never the whole directory.
- Any other user visual: one role only (identity, material, clothing, accessory or background reference).

Inspect the base image itself before describing it; do not fill gaps from memory.

### Step 4 - Resolve text and build the brief

Read `references/text-rules.md` to resolve the headline, cake greeting and cake names. Then open `references/brief-template.md` and fill its slots. Do not write a brief from memory or paste this skill into the image tool. The image tool receives only the filled brief and the labeled images, never the conversation, intake exchange, internal analysis or this skill.

### Step 5 - Generate

Run the brief's preflight (end of `references/brief-template.md`) before each new-poster call. It reviews the brief only; do not generate or inspect during it.

Edit from the base image. Request one candidate per image-tool call; correction candidates do not add to the deliverable count.

If the host delegates image generation to another agent, give it the final brief, the labeled images, and a separate operational instruction to make exactly one image-tool call and return the candidate or error without rewriting the brief or retrying. The controlling agent inspects the actual output before deciding on another call. Keep that operational instruction out of the image-model prompt.

### Step 6 - Inspect and correct

Inspect each new-poster candidate once, in full, before delivery. Check the seven Core Requirements and rank every finding:

- **P0 - must fix:** a Core Requirement is clearly broken: a cat missing, duplicated, not recognizable (including losing clothing or accessories it wears in the photo), or not photographic; a cat covering Tom, a mouse, the cake or its lettering; a cat's body cut off by a line inside the picture (for example a torso ending flat at the tabletop); base art or candles missing, duplicated or deformed; a small cover mark missing, covered (including by the headline) or its text clearly changed; a party hat or collar missing (unless left out because the cat's own item holds that spot), doubled (two party hats or two party collars), mixed from two sets or floating; text missing, unreadable, wrong, or the placeholder headline or the placeholder cake name still visible; white border, paper or mockup edge; imported photo environment; wrong ratio or count.
- **P1 - one targeted attempt:** see `references/inspection.md` (lettering style, film treatment, seams, small-mark drift, composition balance and similar).
- **P2 - not a defect:** a cat standing in front of the table or sitting on it (both are acceptable; do not correct one into the other), minor color-family drift, line or grain differences, letterform variation, ambiguous capitalization.

Correction rules:
- Fix a defect only when it is P0 (or one P1 attempt) and a specific feasible correction exists; a first candidate with a clear P0 defect may start a correction without any earlier round. Once a correction has been tried, continue only if it actually improved the result. Otherwise stop, deliver the best version, and disclose the unresolved item.
- Every extra image call names one observed defect and one concrete change, written from the image actually seen rather than from what the previous brief intended. Use a short local-edit brief that states the defect, the change, the contact area and what must not change.
- Use the best coherent version as the working base; never continue from a rejected or degraded one. If the first candidate has a global composition failure, a fresh candidate from the base image with a revised layout is allowed before delivery.
- Do not repeat an ineffective request, polish speculatively, or fix P2 items. Describe a change as done only after verifying it.
- **Checkpoint:** after 5 generated images in one task with a P0 still unresolved, deliver the best version, state what remains, and ask whether to continue. If no user can be asked, stop at 8 images and disclose the open item.

### Step 7 - Deliver and stop

Deliver one final version per requested output; earlier candidates are superseded. Briefly state any assumption you made (for example, all cats treated as honorees, or a party hat left out because the cat's own hat was kept) and offer to revise; disclose any unresolved P0. End the turn right after delivery without further inspection, correction or generation.
