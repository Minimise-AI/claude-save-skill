---
name: save
disable-model-invocation: true
description: Write lasting context into the AI brain only when the user types /save or clearly asks to save. Show a short plan of what would be written, wait for a yes, then write only those approved lines. Use when the user wants to keep something the session learned. Never run this on your own.
---

# /save

User-invoked only. This is the step that writes lasting context into the brain, which is the folder Claude reads from (usually `CLAUDE.md`, skills, and a little context on the person and the business). Nothing is written into those files automatically.

A yes to a change in the session is not a yes to saving it. Only a `/save` (or a clear "save that to the brain") starts this skill.

## What it needs

- **Claude Code**, so it can edit files in this workspace.
- A workspace folder Claude already reads from. If there is no `CLAUDE.md` at the root yet, say so and offer to create a short one as part of this save.

## Before writing anything

1. Look at what this session actually did or learned. Do not invent items to save.
2. Keep the brain small. It should only hold:
   - skills;
   - a little context for those skills;
   - a little context on the person and the business;
   - pointers to where the data lives, not a copy of the data itself.
3. Leave out anything that is temporary, already written, a secret, or only useful in this chat. If nothing is worth keeping, say so and stop.
4. Show a short plan, then wait for a yes:
   - **what** would be written, in plain English;
   - **where** (which file, and which section if it is obvious);
   - **why** it is worth keeping.
5. Change anything they point at. If they say no, do not write it.

## Write

1. Write only the approved lines, in the files they agreed.
2. Keep the wording short. Every extra line in the brain takes a little of Claude's attention on every later task.
3. Do not rewrite the whole file if a few lines will do. Do not add the same fact twice.
4. When you are done, tell them what was saved and where. If something was left out, say that too.

## Rules

- **Only when they ask.** Never run `/save` yourself, not even right after they have said yes to a change.
- **Show the plan first.** Nothing is written into the brain until they say yes to that plan.
- **Keep it lean.** If a pointer to an existing file will do, do not paste the file into the brain.
- **No secrets.** Never write API keys, passwords, tokens or private client data into brain files.
- **Do not fix the skill by adding rules.** If `/save` starts doing the wrong thing, find the line causing it and propose removing or changing that line first.
