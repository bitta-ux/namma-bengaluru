# Namma Bengaluru

**Swalpa adjust maadi.** This is a Claude skill that makes Claude talk like a Bengaluru techie for the whole session. It uses Kanglish slang and Indian-English grammar, grounded in linguistics research. Your code, commits and docs stay clean.

```
You:    my tests started failing after the upgrade

Claude: Enu guru, upgrade did kirik-a? Okay, found the scene. Your
        toDisplayDate output now has +05:30 at the end, but the snapshot
        was saved with Z. Problem is in the snapshot only, not your code.
        Do one thing: update the snapshots and rerun.
```

## Install

### Claude Code (plugin)

```bash
/plugin marketplace add bitta-ux/namma-bengaluru
```

```bash
/plugin install namma-bengaluru@namma-bengaluru
```

Then start it with `/namma-bengaluru:namma-bengaluru`.

### Claude Code (manual)

Clone the repo and copy the skill folder into your personal skills directory:

```bash
git clone https://github.com/bitta-ux/namma-bengaluru.git /tmp/namma-bengaluru
```

```bash
cp -r /tmp/namma-bengaluru/skills/namma-bengaluru ~/.claude/skills/
```

Then start it with `/namma-bengaluru`.

### claude.ai

Download `namma-bengaluru.skill` from the [latest release](https://github.com/bitta-ux/namma-bengaluru/releases/latest). Then upload it in **Settings → Capabilities → Skills**.

## Usage

| Command | What you get |
|---|---|
| `/namma-bengaluru` | Level 2, the default: friendly banter ("maga", "alva?", "-u" endings, the odd Silk Board joke) |
| `/namma-bengaluru 1` | Light: mostly Indian-English grammar ("only", "itself", "do one thing") |
| `/namma-bengaluru 3` | Full Kanglish: "enu guru", "yen maadodu", "oota aytha?" |

You can change the level mid-session with phrases like "swalpa less slang" or "full Kanglish". Say "normal mode" to switch it off.

## What it gets right

- **It lasts.** The voice stays on through topic changes and long sessions, not just for the next reply.
- **Work product stays professional.** Code, code comments, commit messages, PR descriptions, docs and drafted emails are written in plain English unless you ask otherwise. Your teammates never see the Silk Board jokes.
- **It reads the room.** For grief, health, money or a user who is genuinely upset, it drops to warm, near-plain English on its own.
- **The engineering stays exact.** The persona never makes an answer vaguer.

## Built on research, written with respect

The persona comes from a researched style guide that draws on:

- Wiltshire's acoustic study of Dravidian Indian English (2015)
- Maxwell's thesis on Kannada English intonation (University of Melbourne, 2014)
- Lange's corpus work on "only" and "itself" as Indian-English focus markers
- The OED's Indian English model, Kanglish references and Bengaluru slang guides

Some choices come straight from that research:

- **No "wery" for "very".** Kannada speakers largely keep v and w distinct, so the stereotype is wrong as well as mocking.
- **The jokes are civic, not ethnic.** It jokes about Silk Board traffic, the "best weather" during floods, the auto meter, and darshini coffee. These are the jokes Bengalureans make about their own city, never about people or how they speak.
- **It's Bengaluru, not generic "Indian".** No *bhai*, *bindaas* or Tamil *da*.

The full glossary, grammar patterns, cultural references and 20 sample dialogues are in [`skills/namma-bengaluru/references/style-guide.md`](skills/namma-bengaluru/references/style-guide.md).

## License

[MIT](LICENSE). Maja maadi.
