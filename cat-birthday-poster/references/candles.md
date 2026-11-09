# Candles

The base art has three lit candles: one on top of the cake, and one on each of the two mice's cake-slice caps (the small piece of cake each mouse wears on its head). All three are protected by default (see Core Requirements in `SKILL.md`), and the brief says so explicitly: "one candle on top of the cake and one candle on each mouse's cake-slice cap, three lit candles in total". Without that statement, image models tend to drop the head candles.

Read this file only when the user asks to change the candles (a count, numeral candles, a replacement) or explicitly asks to show the cat's age with candles. Merely giving the cat's age is not such a request. Never offer candle customization proactively.

## Rules

- Preserve both mice's cake-slice caps and head candles unless the user explicitly identifies those head elements and asks to remove or replace them. A general request about "cake candles" or "numeral candles" does not authorize touching them.
- Describe the requested final state as a total and an allocation: the head candles retained (normally 2) plus the number of separate candles on top of the cake, each with one flame. Say the arithmetic once when it helps, and check it before calling the image tool. The count of cake-top candles includes the existing one.
- A requested total counts every candle in the picture, so it includes the two head candles by default; do not ask about this. Cake-top candles = total minus 2. Ask only when the total is below 3, since the three protected candles already exceed it.
- Numeral candles and any other added candle are illustrated objects: draw them in the cover's inked style (see Illustrated Additions in `SKILL.md`). Do not add flames beyond one per candle.
- Large totals (for example a cat's age of 15 or more) may not fit on the cake top; confirm a reasonable arrangement with the user before generating rather than inventing one.
- In the brief, fill CANDLES and EXTRA_EDIT_AREAS with the final state and remove the cake-top candle from PRESERVED_ELEMENTS (slot rules in `references/brief-template.md`); never leave the default "three lit candles" sentence in a brief that changes candles.
- In a revision (`references/editing.md`), the same rules apply; state the final total and allocation, not an instruction to "add" candles.
