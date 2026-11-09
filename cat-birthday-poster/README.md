# Tom and Jerry Cat Birthday Poster

This reusable Agent Skill creates a personal, non-commercial birthday poster by combining a vintage cartoon-cover template with a user's real cat photo.

## Contents

- `SKILL.md` - core requirements and the 7-step workflow.
- `references/` - loaded on demand: `brief-template.md` (the fixed image brief and lettering specs), `text-rules.md`, `multi-cat.md`, `accessory-index.md`, `candles.md`, `inspection.md`, `editing.md`.
- `assets/templates/` - ready-made base posters, one per ratio (`poster-4x3.png`, `poster-1x1.png`, `poster-3x4.png`). The agent edits these; only ratios whose file exists are offered as standard choices.
- `assets/party-accessory-sets/` - nine independent hat-and-collar pairs. The agent attaches only the set(s) it needs; these are never edit bases.
- `assets/example-output.png` - documentation-only example of a finished poster. It is not an edit base, identity reference or generation input, and the agent does not show it to users.

## Example output

The annotations show the intended layout. The actual poster is generated from the user's cat photo and preferences.

![Annotated example output](assets/example-output.png)

## Tested environments

Tested on Codex. Other agents and image models have not been retested for v3.0.

See `SKILL.md` for the runtime workflow and `LICENSE.txt` for the use terms.
