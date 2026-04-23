Sector Command — Smart Operations Dashboard

This is a fast, futuristic web dashboard with a NASA-flavored interface. It’s loaded with real-time stats, handy utilities, and an AI help desk.

Features

- Advanced UI — Glass effect and NASA-style design
- Live AQI & Weather — Up-to-date environment data
- Visual Effects — Scanlines, transitions, and slick animations
- Built-in Tools — Calculator, report issues, hydration timer
- AI Help Desk — Groq-powered support
- Local Storage — Saves everything right in your browser

What You Need

- Node.js 20+  (get it at https://nodejs.org)
- Bun (recommended)  (https://bun.sh)

Check your setup:

node -v
bun -v

Project Setup

1. Go to the right folder

Heads up: this project’s a little nested.

cd sector-command-main/sector-command-main

If you see package.json, src/, and vite.config.ts — you’re in the right place.

2. Install dependencies

Bun (recommended):

bun install

or with npm:

npm install

3. If “vite not found” pops up

bun add -d vite

Setting Up Your Environment

Create a .env file in the project’s root folder. Paste in:

VITE_SUPABASE_URL="https://uydqvzvwuffglobavach.supabase.co"
VITE_SUPABASE_PUBLISHABLE_KEY="your_supabase_key"
SUPABASE_URL="https://uydqvzvwuffglobavach.supabase.co"
SUPABASE_PUBLISHABLE_KEY="your_supabase_key"
GROQ_API_KEY="your_groq_key_here"

Groq AI Setup

By default, this project works with an existing Groq AI key.

Want to use your own? Here’s how.
1. Grab an API key at: https://console.groq.com/keys
2. Drop it into your .env like this:

GROQ_API_KEY="your_actual_api_key"

3. Restart the dev server:

bun run dev

Notes

- Without a valid key, the AI panel will just say: "Station OPS offline — control-room key missing."
- Don’t ever share your API key in public.

How to Run

bun run dev

Or:

npm run dev

Open your browser:

http://localhost:5173

(or whatever port shows up in your terminal)

What Works

Feature                | Status
---------------------- | ---------------
UI/Animations          | Works
AQI & Weather APIs     | Works
Tools                  | Works
AI Help Desk           | Needs an API key

Troubleshooting

“vite not found”
bun add -d vite

“script not found dev”
You’re likely in the wrong folder. Move to the inner directory where the project lives.

App won’t start
- Make sure .env exists and is filled out
- Try reinstalling dependencies

Clean Reset

rm -rf node_modules
rm package-lock.json
bun install

If you’re on PowerShell:

Remove-Item -Recurse -Force node_modules
Remove-Item package-lock.json -ErrorAction SilentlyContinue
bun install

Deployment Notes

- Works on Vercel once dependencies are squared away.
- Add your .env settings in Vercel’s dashboard.
- Never commit .env to your repo.

Tech Stack

- React
- Vite
- Groq AI
- Supabase
- Tailwind CSS

Final Note

Almost every issue comes down to these three things:
- Wrong folder
- Missing dependency
- Missing .env

Fix those, and you’ll be good to go.
