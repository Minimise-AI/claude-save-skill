# Save

A Claude Code skill that keeps your AI brain small. Claude does not write lasting context into it on its own. Nothing is saved unless you type `/save`.

It shows a short plan of what would be written, waits for a yes, then writes only those approved lines. Secrets stay out.

## What you need

- [Claude Code](https://claude.com/claude-code)

## Install

Copy the [`save`](save/) folder into either place:

- For every workspace on this computer: `~/.claude/skills/`
- For one project only: that project's `.claude/skills/`

Make the `skills` folder if it isn't there yet. You should end up with `save/SKILL.md` inside it.

To download: click the green **Code** button, then **Download ZIP**, unzip it, and copy the `save` folder across.

Open Claude Code in that workspace. From then on, lasting context is written only when you type `/save` (or you clearly ask to save it to the brain).

## Paste this into CLAUDE.md

Open the workspace `CLAUDE.md`. Create one at the root of the workspace if it isn't there yet. Paste these lines near the top. Keep them short.

```markdown
## Saving to the brain

Only `/save` writes lasting context into this workspace. You may edit working files if the task needs it, but never add to `CLAUDE.md`, skills, or other brain files unless the person types `/save` (or clearly asks you to save it to the brain).

A yes to a change is not a yes to saving it. When something is worth keeping, tell them it is ready and that they can type `/save`. Never run `/save` yourself, not even right after they have said yes.

The brain should stay small. It holds skills, a little context for those skills, a little context on the person and the business, and pointers to where the data lives. It does not need to know everything.
```

Made by Finn at [Minimise](https://minimise.co.nz).
