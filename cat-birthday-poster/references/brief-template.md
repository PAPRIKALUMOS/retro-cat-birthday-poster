# Image Brief Template

Fill the slots in `[brackets]`. Paste the fixed blocks (`BLOCK` names) verbatim; they are the tested wording. Include only the sections that apply. The brief describes the final state of this request, not a history, and states positive requirements; hard exclusions live only in the closing `Avoid` line.

## New poster from a template (`assets/templates/poster-*.png`)

```text
Asset: personalized cat birthday poster, [ratio], one image.

Input images:
Image 1: [template file] - base to edit.
Image 2: [cat photo] - identity reference for [cat label] only; not for its background, floor or lighting.
[Image 3...: [accessory file] - [hat and matching collar / hat only / collar only] worn by [cat label]; design reference only.]

Layout: LAYOUT_BLOCK
Cats: [for each cat: label, birthday cat or companion, identity description from Step 3 including what it wears; these anchors must stay recognizable]
Accessories: [cat label] wears [the hat from Image [n] on its head and the matching collar around its neck / only the hat from Image [n] on its head / only the collar from Image [n] around its neck], same colors, patterns and materials, fitted naturally to its pose[ and clothing]. [Name what the cat already wears so it is kept as in the photo; the party item for a spot that the cat's own item holds is omitted. Delete this line and the accessory image when no party item is used.]

Text:
Headline: "[headline]" ([language]) - paint it in place of the placeholder headline in Image 1 / none: remove the placeholder headline and continue the background seamlessly.
Cake upper band: "[greeting]" ([language]) - [leave as in Image 1 when the default] / [replace].
Cake lower band: replace the placeholder name "Tom" with "[names]" ([language]) / remove the placeholder name and leave the band as blank icing.
HEADLINE_SPEC
CAKE_SPEC
SCRIPT_NOTE

Zones:
Preserved: [PRESERVED_ELEMENTS]
Edit areas: the cat area on the right, the headline area (placeholder "Party Time!") and the cake's lower name band (placeholder "Tom")[; also [EXTRA_EDIT_AREAS] - only what the user explicitly asked to change].
Contact boundary: where a cat overlaps or touches the illustrated art, only that art's edge may change (local occlusion and contact shadow); nothing else.
Photographic domain: PHOTO_BLOCK
[Illustrated additions: ILLUS_BLOCK - only when objects are added]
[Exact counts: include only for an explicit non-default count, allocation or placement; see candles.md for candle totals]
Exactly: EXACT_BLOCK
Avoid: AVOID_LINE
```

### Fixed blocks

**LAYOUT_BLOCK:** Tom on the left, the cake center-left, [N] real cat(s) filling the right half as large head-and-upper-body portraits entering from the right or lower right, standing in front of the right end of the table (the cat's body covers that part of the table and runs down to the canvas edge; no body ends at the table top or is cut off inside the picture). A single cat's head is at least comparable in size to Tom's head; with several cats the honorees get the largest portraits (comparable among co-honorees), companions are smaller, and the cat group as a whole is more prominent than Tom. The cats do not cover Tom, the mice, the cake or its lettering. The artwork fills the canvas edge to edge.

**PRESERVED_ELEMENTS (default list):** Tom; both mice with the cake-slice cap on each head and the lit candle on each cap; the lit candle on top of the cake; the cake and its frosting divider; the cake's upper-band lettering; the table; the small cover marks (the MEOW badge, the APRIL 21 label, the c.a.t.'s script, the Purrco script, the 10¢ price box); the pale-yellow-to-pale-blue background gradient with its paper grain. State them as they appear in Image 1, "exactly as they are" (the only exception: the c.a.t.'s and Purrco scripts may be moved a short distance as the headline spec allows).

**PHOTO_BLOCK:** Each real cat and the accessories it wears form one photographic layer: real fur, eyes, nose and whiskers, natural edges, coherent light, perspective and contact shadows, with fine film grain, gently faded color, mild warmth and subtle print softness. Only the cat and its worn accessories are photographic; everything around them is the poster's illustrated background.

**ILLUS_BLOCK:** Draw each added object in the cover's mid-century comic style: simplified slightly irregular forms, clean continuous black ink outlines at the weight of neighboring objects, flat saturated fills, minimal hard-edged shading, subtle newsprint grain.

**EXACT_BLOCK:** one Tom, two mice, [CANDLES], [N] real cat(s), at most one party hat and one party collar per honoree (none in a spot where the cat keeps its own item).

**AVOID_LINE:** white borders, paper edges or mockup backgrounds; vignette; added watermarks, added logos, or text beyond the lines requested above (the existing cover marks stay). (Keep this to hard exclusions only. If testing shows it makes a model draw these items, delete it.)

### Slot rules for explicit user changes

The default poster has three edit areas (the cat area, the headline, the cake's lower name band); everything else is preserved unless the user explicitly asked to change it. Describe regions by meaning (the right-hand cat area, the cake's upper band), never by pixel coordinates.

- **PRESERVED_ELEMENTS:** start from the default list above and delete every element the user asked to change, so one brief never asks for both a change and its preservation.
- **EXTRA_EDIT_AREAS:** empty by default. List each element the user asked to change with its new target once (the cake's upper band: the new greeting; the cake-top candle area: the final candle state; the background: the requested background; a cover mark: its new wording). A requested new background or mark is drawn in the cover's illustrated style.
- **CANDLES** (EXACT_BLOCK): by default `three lit candles (one on top of the cake, one on each mouse's cake-slice cap)`. When candles change, use the final total and allocation from `references/candles.md` instead.
- **Greeting:** when it is replaced, state the new wording in the Text section and do not also say "leave as in Image 1".

### Lettering specs

Two separate treatments. Carry only those that apply, each with the visual guide below.

**HEADLINE_SPEC:** The headline is painted directly onto the cover as one hand-lettered title in the style of the existing headline lettering in Image 1 (the template's placeholder, the accepted headline in a revision, or the headline lettering on a lettering-style reference image when Image 1 has none): chunky letters of varied widths, subtly uneven ink contours, organic spacing and a gently uneven baseline, filled with warm golden yellow, outlined with a thick hand-inked black line, with a subtle dark shadow that follows the irregular contours. The whole headline stays clear of every cover mark. If it is long, reduce the lettering size or set it on two lines in the same style; if it still needs room, the c.a.t.'s script may move a short distance to the upper left of the headline and the Purrco script to its lower right, unchanged in wording, size and look, never far from where they are and never overlapping the headline.

**CAKE_SPEC:** The cake names are slightly irregular, rounded blue icing-piped strokes lying on the curved surface of the cake's lower band, in the same blue hand-drawn icing stroke as the cake's upper-band lettering in the final poster; when the upper band is empty, follow the stroke character of the template's original "Happy Birthday" without redrawing those words.

**SCRIPT_NOTE:** Draw every character in its own script's hand-lettered form, with all strokes and components intact and readable. The language names in parentheses are descriptions; do not draw them.

## Fallback: ratio without a template

Used when the user explicitly requests a ratio that has no template file. Use the template with the nearest ratio as Image 1 and make these changes to the template brief:

- Add a reflow plan: extend the background gradient seamlessly to [ratio] with no seam, color cast or vignette (or crop only empty background); move the illustrated group toward the left or lower-left to free a continuous area on the right for the cats; keep the mice and cake lettering visible; keep the cover marks in their own positions; keep the headline near the top and distribute space on purpose so no empty band appears.
- The only allowed layout changes are moving and uniformly scaling the illustrated group (Tom, the mice, the cake, the table) as one unit, and extending or cropping empty background. Every character's appearance and the group's internal arrangement stay protected: nothing inside the group is redrawn, stretched or rearranged.
- Tell the user the result is best effort.

## Preflight (check the brief before every new-poster call)

- Only the necessary images are attached; each has one role.
- Cats, identity anchors, honorees and required prominence are right.
- Layout leaves the whole cake, its lettering, both mice and their candles clear, with enough continuous space on the right for portrait-scale cats.
- Ratio and output count are right.
- Headline, greeting and names match the resolved values and placement, including empty values; language labels are present.
- Each honoree's party hat and matching collar are both named, from one set (or the omitted one is stated).
- Preserved elements describe what the base image actually shows, and no element appears in both Preserved and Edit areas.
- Any explicit count or placement is consistent (candles: `references/candles.md`).
