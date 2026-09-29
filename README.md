# PAIMANA Foresight — SIH Prototype

## Included
- `index.html` — PAIMANA Foresight UI + Gemini-backed chatbot.
- `api/chat.js` — Vercel serverless endpoint for Gemini.
- `package.json` — Node 22.x project.
- `.env.example` — required environment variable.
- `.gitignore` — keeps secrets out of Git.

## Local test
Install Node.js 22 and the Vercel CLI:
`npm i -g vercel@latest`

Then:
`vercel login`
`vercel env add GEMINI_API_KEY development`
`vercel dev`

Open the local URL shown by Vercel.

## Deploy
Push the folder to GitHub and import the repository into Vercel, or run:
`vercel`
then:
`vercel --prod`

In Vercel → Project Settings → Environment Variables, add `GEMINI_API_KEY` for the environments you use, then redeploy.

## Security
Never put the Gemini key in `index.html` or frontend JavaScript. The browser calls `/api/chat`; only the Vercel function contacts Gemini.

## Demo
Test Overview → Dashboard → project details/what-if sliders → chatbot. Keep the prototype/sample-data language because these screens are not a live government data feed.
