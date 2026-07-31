# NEXUS-MD / PEREZ-MD — WhatsApp Bot

## Overview
A WhatsApp multi-device bot built with [Baileys](https://github.com/whiskeysockets/Baileys) (Node.js). Features group management, media commands, AI chat (OpenAI/Gemini), sticker creation, YouTube downloads, and more.

## Stack
- **Runtime:** Node.js (CommonJS)
- **WhatsApp library:** `@whiskeysockets/baileys` (custom fork)
- **Database:** PostgreSQL (`pg`)
- **Entry point:** `index.js`
- **Bot logic:** `Perez.js`

## ⚠️ Status: Not runnable yet

The following directories are referenced in code but **missing from the repo**:
- `./database/` — PostgreSQL config & settings fetch (`database/config.js`, `database/fetchSettings.js`)
- `./lib/` — Helper utilities (`lib/dreadexif.js`, `lib/dreadfunc.js`)
- `./store/` — In-memory Baileys store (`store/store.js`)

These files must be added before the bot can start.

## Required environment variables

| Variable | Description |
|---|---|
| `SESSION` | Base64-encoded WhatsApp session credentials (from pairing tool) |
| `BOTNAME` | Display name for the bot (default: `𝙋𝙀𝙍𝙀𝙕-𝙈𝘿`) |
| `PORT` | HTTP port (default: `8000`) |
| `STICKER_PACKNAME` | Sticker pack label |
| Database URL | PostgreSQL connection (check `database/config.js` once added) |

## How to run (once files are added)
```bash
npm install
node index.js
```

## Getting a session
Use the pairing tool at https://perez-md-pairing.onrender.com to generate a session string, then set it as the `SESSION` environment variable.

## User preferences
<!-- Add preferences here -->
