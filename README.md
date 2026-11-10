# second-brain

Give Claude a memory that lasts between chats.

A second brain is a plain folder of notes ([Obsidian](https://obsidian.md) vault) that Claude reads at the start of every chat and updates at the end. It knows who you are, what you're working on and what you decided last week, so you stop explaining yourself from scratch.

This repository is a starter kit. You don't copy anything by hand: Claude reads the setup guide, asks you a few questions and builds the vault for you.

## Setup

1. Install [Obsidian](https://obsidian.md) (free).
2. Create an empty vault in Obsidian and remember where the folder is.
3. Open [Claude Code](https://claude.com/claude-code) or the Claude desktop app with access to that folder, and send:

```
Set up my second brain from https://github.com/shizukesadev/second-brain
My vault is here: <path to your vault folder>
```

That's it. Claude will ask about you and your projects, create the notes and connect itself to the vault.

## What you get

| Note | What it does |
|---|---|
| `Home` | Entry point: what's in focus now, where everything lives |
| `90 Claude/Instructions for Claude` | The rules Claude follows when working with your vault. Edit them any time |
| `90 Claude/About me` | Short profile: who you are, goals, how you like answers |
| `90 Claude/Session log` | Claude writes what you did and decided after each session |
| `90 Claude/What I learned` | Claude records your corrections so it doesn't repeat mistakes |
| `00 Inbox/Reminders` | Ask "remind me" and Claude brings it up at the start of the next chat |
| `01 Projects` | One note per project, with a dated "Decisions" section |
| `99 Templates` | Daily note, idea, project, session |

The structure follows a simple scheme: Inbox, Projects (things with an end), Areas (things that last), Resources, Archive, Journal.

## How it works

- **Start of a chat:** Claude reads `Instructions for Claude` and `Home`, then the notes for the topic you bring up.
- **During work:** decisions go into the project note with a date and a reason.
- **End of a session:** a short entry in `Session log`.
- **Nothing gets deleted:** old notes move to `04 Archive`.

## Good to know

- **Which Claude:** Claude needs access to the folder. Claude Code and the desktop app with folder access can do everything. A regular web or phone chat can't write files: Claude will give you the notes as text and you paste them into Obsidian.
- **Privacy:** the vault is a folder on your computer. Claude never writes passwords, API keys or tokens into it, but don't sync it to places you don't trust.
- **What Claude changes:** only the vault folder you named. If you use Claude Code, it asks before adding one line to `~/.claude/CLAUDE.md` so every new session reads the vault automatically.
- **It's yours:** rename folders, change rules, write in any language. Claude creates the notes in the language you talk to it in.

## License

[MIT](LICENSE)

## По-русски

Второй мозг для Claude: папка заметок в Obsidian, которую Claude читает в начале каждого чата и дополняет в конце. Он помнит, кто ты, над чем работаешь и что вы решили. Поставь Obsidian, создай пустое хранилище и напиши Claude: `Собери мне второй мозг по https://github.com/shizukesadev/second-brain, хранилище лежит тут: <путь к папке>`. Дальше он всё сделает сам, заметки будут на русском.
