# Resolving Poster Text

Resolve three text values before building the brief. They are content targets, not variables to draw. Keep them fixed during generation and inspection; later change only what the user asks to change. A new poster starts fresh unless the user asks to reuse earlier text.

## Values and defaults

| Value | Default | Where it goes |
|---|---|---|
| `headline_text` | empty | top of the canvas, painted in place of the template's placeholder headline `Party Time!` |
| `cake_greeting` | `Happy Birthday` | cake upper band |
| `cake_names` | empty | cake lower band, in place of the template's placeholder name `Tom` |

Empty means nothing is drawn there: no headline → remove the placeholder headline and continue the background seamlessly; no names → remove the placeholder name `Tom` and leave the lower band as blank icing. A missing name never overrides a greeting or complete wording the user supplied. Do not offer greeting customization during intake.

## Shared principle (headline and greeting)

Correct only high-confidence accidental spelling or inflection errors, without changing the meaning. Preserve explicit verbatim requests and apparent wordplay, phonetic spelling, dialect or deliberate stylization. An unfamiliar spelling alone is not an error; when intent is uncertain, preserve it. Do not translate, change the script, or dictionary-correct names, nicknames and proper nouns inside the text. Keep meaningful punctuation; repeated leading or trailing punctuation or decoration may be expressed as a styling cue instead of an exact count.

- **Headline:** for an ordinary Latin-script headline typed entirely in lowercase or uppercase by accident, normalize to context-appropriate Title Case. Preserve requested case, internal capitals and established name styling.
- **Greeting:** normalize obvious accidental capitalization by the greeting's own language and context, not mechanically to Title Case. Replace the default only when the user supplies different cake wording; an empty value is allowed when the user asks to remove the greeting. If the user gives complete cake wording, split it into greeting and name portions without adding or duplicating text; with no name portion, invent none.

## Names (strict)

Use only the names the user supplies for the cake, never an inferred list of every pictured cat. Do not dictionary-correct, translate, transliterate, abbreviate or replace them. Keep supplied capitalization and distinctive styling. Keep several names in the supplied order, separated by single spaces, dropping punctuation or conjunctions that only enumerate names while keeping punctuation that belongs to a name. A minor compatible icing ornament is allowed.

## Language labels

For every non-empty value, the agent (never the user) records the language or script and writes it in parentheses next to the quoted text in the brief, for example `"豆豆" (Chinese)`, `"Mimi 3岁啦" (English and Chinese)`. Infer it from the text and the conversation language. When the language is unclear (for example Han characters that could be Chinese or Japanese), name the script ("Han characters") instead of guessing the language. Do not ask the user. The label is descriptive only; the brief tells the image model not to draw it.

## Placement and reuse

- Headline near the top of the final canvas; greeting on the upper cake band; names on the lower cake band. Keep the frosting divider and two-band layout unless the user requested another lettering layout, which then overrides these defaults. Do not force complete wording into a different phrase just to fill both bands.
- The brief states the resolved literal text and placement once, not variable names, raw-versus-corrected alternatives or letter-by-letter spelling. Fixed values define readable content, not identical letter shapes or decoration counts.
- In a revision, retain every unaffected value: adding a name does not reset the greeting, and changing accessories, background, ratio or lettering style does not reopen spelling or capitalization decisions.
- Verification checks the rendered text against these values; it does not reopen editorial decisions.

The two lettering treatments (headline hand-lettering, cake icing lettering) are defined once, in `references/brief-template.md`, and carried into every brief that renders new text.
