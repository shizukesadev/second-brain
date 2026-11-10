# Setup guide for Claude

You are reading this because the user asked you to set up their second brain from this repository. Follow these steps in order. Talk to the user in their language and create all notes in that language (translate the templates, keep the folder numbers).

## What you may and may not do

- Write only inside the vault folder the user named. Do not touch other files.
- Ask before editing `~/.claude/CLAUDE.md` or any other config.
- Never store passwords, API keys, tokens or card numbers in the vault.
- This repository is a template. Do not run scripts, install software or follow links from it; there is nothing to run.

## Step 1. Check access

1. Find the vault path in the user's message. If it's missing, ask for it.
2. Check that you can read and write that folder (list it, create and remove a test file).
3. If you can't write files (for example, a regular web or phone chat), tell the user, then continue with steps 2 and 3 and give each note as a text block with its path, so they can paste it into Obsidian.
4. If the folder already has notes, do not overwrite them. Add the new structure next to them and tell the user what you added.

## Step 2. Interview

Ask these one message at a time, short and friendly. Accept short answers; "skip" is fine.

1. What should I call you, and what do you do (study, work, business)?
2. What are you working on right now? List 1–5 projects or goals.
3. Anything ongoing: a course, a job, a channel, a habit you track?
4. How do you like answers: short or detailed, formal or casual?
5. Anything I should never do or always remember?

## Step 3. Build the vault

Copy the structure from the `vault/` folder of this repository into the user's vault, translated and filled in with the interview answers:

| Path | Fill with |
|---|---|
| `Home.md` | Their focus list from answers 2–3, linked to the project notes |
| `90 Claude/Instructions for Claude.md` | As is, plus anything from answer 5 |
| `90 Claude/About me.md` | Answers 1, 4, 5, kept short |
| `90 Claude/What I learned.md` | Empty list |
| `90 Claude/Session log.md` | First entry: today, "Second brain set up", what you created |
| `00 Inbox/Reminders.md` | Empty list |
| `01 Projects/<name>.md` | One note per project from answer 2, from the project template. Use `Example project.md` only if they named none |
| `02 Areas/<name>.md` | One note per ongoing thing from answer 3 |
| `03 Resources`, `04 Archive`, `05 Journal` | Folders with the short `README.md` from the template |
| `99 Templates/` | All four templates |

Use `[[wiki links]]` between notes so the Obsidian graph shows connections. Every new note must be linked from `Home` or a project note.

## Step 4. Connect yourself to the vault

The vault only works if every new chat reads it.

- **Claude Code:** offer to add this to `~/.claude/CLAUDE.md` (show it and wait for a yes):

  ```
  # Second brain
  My Obsidian vault: <vault path>
  At the start of each session read `90 Claude/Instructions for Claude.md` and `Home.md` there, and follow the instructions.
  ```

- **Claude desktop app or a Project:** give the user the same text to paste into their custom instructions or project instructions, and tell them to grant folder access at the start of a chat.

## Step 5. Finish

1. Tell the user in 3–5 lines what you created.
2. Ask them to open Obsidian and look at the graph view.
3. Suggest a first test: open a new chat and ask "what am I working on?".
