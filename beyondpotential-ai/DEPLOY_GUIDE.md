# Beyond Potential AI — Deployment Guide

## What you have
- `api/chat.js` — the secure backend that holds your API key
- `public/index.html` — the full chat interface
- `vercel.json` — tells Vercel how to run everything

---

## Step 1 — Get your Anthropic API key
1. Go to console.anthropic.com
2. Sign in or create an account
3. Click "API Keys" in the left menu
4. Click "Create Key", name it "Beyond Potential"
5. COPY IT IMMEDIATELY — it only shows once
6. Add billing credit ($5 to start is fine)

---

## Step 2 — Create a GitHub repo
1. Go to github.com and create a free account if you don't have one
2. Click the "+" button top right → "New repository"
3. Name it: beyondpotential-ai
4. Set it to Private
5. Click "Create repository"
6. Upload the three files/folders from this project:
   - api/chat.js
   - public/index.html
   - vercel.json

---

## Step 3 — Deploy on Vercel
1. Go to vercel.com and create a free account
2. Click "Add New Project"
3. Connect your GitHub account
4. Select the beyondpotential-ai repo
5. Click Deploy (Vercel auto-detects the config)

---

## Step 4 — Add your API key (CRITICAL)
This is the most important step. Never put your key in the code itself.

1. In Vercel, go to your project dashboard
2. Click "Settings" → "Environment Variables"
3. Click "Add New"
4. Name: ANTHROPIC_API_KEY
5. Value: paste your key from Step 1
6. Click Save
7. Go to "Deployments" and redeploy so the key takes effect

---

## Step 5 — Get your live URL
Vercel gives you a free URL like:
beyondpotential-ai.vercel.app

That is your live AI. Share it. Embed it in Whop. Send it to your partner.

---

## Step 6 — Embed in Whop
1. Go to your Beyond Potential Whop community
2. Find the "Beyond Potential AI" channel
3. Edit the channel
4. Add your Vercel URL as the linked resource
5. Members click it and the full branded AI opens

---

## Updating the AI
When you want to add new transcripts or update the persona:
1. Edit api/chat.js — update the KNOWLEDGE_BASE or SYSTEM_PROMPT sections
2. Push the change to GitHub
3. Vercel auto-redeploys in about 30 seconds

---

## Cost reminder
Running on Claude Haiku 4.5:
- ~$0.013 per conversation exchange
- ~$13/month at 100 active members using it 10x each
- With prompt caching added later: drops to ~$2-3/month at same usage

Way cheaper than CustomGPT at scale.

---

## Questions?
Bring any error messages or screenshots back to Claude and we'll fix it immediately.
