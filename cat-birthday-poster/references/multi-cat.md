# Multiple Cats

Read this when the supplied photo or photos contain more than one cat, or the user mentions several cats.

## Two decisions, each with a default

| Decision | If the user did not say |
|---|---|
| Who appears on the poster | include every visible cat |
| Who is the birthday cat (honoree) | all included cats are honorees |

Resolve them from the user's own wording, however loosely phrased ("this is A and B", "the one on the left is celebrating", "put them all in"). Apply a default only to the part left unanswered. Never invent a restriction the user did not give.

Resulting combinations:
- Inclusion known, no honoree named → every included cat is a co-honoree with a hat. Record the assumption.
- Honorees named, inclusion unspecified → include all visible cats, emphasize the honorees, hats on the honorees only. Record the assumption.
- Both stated → follow them.

## Asking

If the user gave no composition information, ask once, in the same message as any unresolved optional items (name, headline, ratio):

> The photo contains multiple cats.
>
> **Please confirm**
> - Should all cats appear in the poster?
> - Which cat is the birthday cat?

If the reply answers only one question, apply the default to the other and continue. If it answers neither, repeat only **Please confirm**. "Use defaults" settles the optional items but not a wholly unanswered composition question.

## More cats than the ratio fits

The comfortable number of cats per ratio is in the Base Images table in `SKILL.md`. When the included cats exceed it, never refuse. Tell the user once, translated into their language:

> This photo has [N] cats; the [ratio] poster fits [M] comfortably, and with more the cats appear smaller.
> - Switch to [roomier ratio] (fits up to [K])
> - Pick [M] cats to feature
> - Keep all [N] anyway (smaller portraits)
>
> Reply with a choice, or "go ahead" to keep all.

- The roomier ratio is the next template with a larger number (`3:4` → `1:1` → `4:3`). If the poster is already `4:3`, leave out the switch option.
- If the photo already shows more cats than the ratio fits and inclusion is still unresolved, put this note into the same **Please confirm** message instead of sending a second one.
- "Go ahead", no clear choice, or no one to ask → keep all the cats, make them as large as the free area allows, and mention the assumption at delivery.
- Do not ask again after the user has answered.

## Layout and identity

- Every honoree gets the largest portrait scale within the cat group, with comparable prominence to the other honorees (not necessarily identical size, and no arbitrary lead). Companions are smaller. The whole cat group is more prominent than Tom.
- Roughly the right half is a useful guide. If space is tight, crop lower bodies at the canvas edge, never at the table top, and never crop faces.
- One identity brief per selected cat; label each cat in the brief ("the black cat on the left of the photo"). Each cat appears exactly once.
- Hats only on honorees. Use distinct but coordinated accessory sets unless the user asks for matching ones.

## Examples

- "这是我家 A 和 B" (no honoree named) → both included, both honorees; note the assumption in delivery.
- "左边那只过生日" → include all visible cats, left cat is the honoree with a hat, others smaller without hats.
- "都放进去吧" → inclusion answered; honorees unanswered → all included are co-honorees.
- A photo with three cats and no instruction → ask the **Please confirm** question once.
