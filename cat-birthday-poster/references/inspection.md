# Inspection Details

`SKILL.md` Step 6 lists the P0 defects and the correction rules. This file adds the P1 and P2 detail. Read it when a candidate has findings that are not obviously P0.

## P1 - one targeted attempt, then disclose

Try at most one specific local edit for each. Skip it if no specific, plausible target exists.

- Lettering style: the headline or cake name looks like a standard digital font, a detached label, a boxed plaque or photorealistic 3D frosting instead of the required treatments (see the lettering specs in `references/brief-template.md`), or characters are split into pieces. Judge it against the spec only; do not start another call for uncertain letterform variation.
- Film treatment clearly too strong (plastic, HDR) or missing on the cats.
- Background gradient shows a seam, color cast or vignette.
- A small cover mark (MEOW badge, APRIL 21 label, c.a.t.'s and Purrco scripts, 10¢ box) is slightly blurred or its letterforms have drifted, but it is still present, correct and readable. (A missing mark or clearly changed text is P0.)
- The cake's frosting divider or two-band structure was changed (unless the user requested another layout).
- The composition has an accidental empty band, the headline is not near the top, or the cats clip awkwardly.
- An added illustrated object does not match the cover's style, or a cat's edge, halo or contact shadow looks unnatural.

## P2 - never a reason for another call

Color drift within the same family on Tom or the mice, small differences in line weight or grain, letterform differences, ambiguous capitalization, flexible decoration counts, small shifts in position or crop.

## Lettering defects: strategy

- Try a supported local image edit aimed at the specific lettering target.
- Do not launch broad font or package searches, download dependencies, or build a compositing pipeline just because the generated lettering looks mechanical. Code-based text is not a default fallback for this poster.
- Offer code-based text only when exact legibility is still unresolved, suitable local tools and fonts already exist, and the user accepts in plain words that standard font rendering may lose the hand-drawn look. Do not promise that another script or method will render perfectly.
- When these conditions are not met, say what the limitation is and stop that route.

## Checking text

Compare the rendered text with the resolved values and placement. Correct only clearly unreadable, missing or substituted words or names. Do not reopen spelling or capitalization decisions.

## Paired verification

Each hat and collar must come from the single selected pair (wearing adaptations such as curvature, size, partial occlusion and local fur or clothing changes are fine). No white asset background or unused accessory element appears. The illustrated table keeps its base size and is not extended into a platform for a cat.
