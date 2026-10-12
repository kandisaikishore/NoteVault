# 📝 NoteVault

## Live Demo / Deployment URL

**Deployment URL:** Not verified yet. Add the confirmed public application URL here after checking the live service. The GitHub repository link is not a deployment URL.


[![Repository](https://img.shields.io/badge/GitHub-Repository-181717?logo=github)](https://github.com/saikishore2410/NoteVault) [![Issues](https://img.shields.io/github/issues/saikishore2410/NoteVault)](https://github.com/saikishore2410/NoteVault/issues) [![Last Commit](https://img.shields.io/github/last-commit/saikishore2410/NoteVault)](https://github.com/saikishore2410/NoteVault/commits/main)

> NoteVault is a full-stack study workspace for handwritten STEM notes, AI-powered digitization, research grounding, and focused study workflows.

## At a glance

- **Purpose:** Understand the problem and supported workflows from the feature and scope sections below.
- **Setup:** Follow the project-specific steps in **Getting started** or **Run locally**; verify commands against the current source and package scripts.
- **Configuration:** Keep API keys, database passwords, tokens, and user data out of commits. Use local environment variables for secrets.
- **Quality:** Run the available build, tests, and lint checks before proposing changes.



NoteVault is a full-stack study workspace for handwritten STEM notes, AI-powered digitization, research grounding, and focused study workflows.

## What it includes

- 🔍 Search and filter notes by subject, topic, tags, authors, and OCR content.
- 📖 Multi-page note viewer with zoom, thumbnails, bookmarks, upvotes, and study-history resume.
- 🤖 Handwritten-note OCR powered by Gemini.
- 💬 Multi-turn STEM tutor with optional Google Search grounding.
- 🎙️ Audio transcription and a live voice study tutor.
- 🎬 STEM concept video generation and 🎵 focus-music generation.
- 🧩 Diagram generation/editing and campus study-spot discovery.
- 🔐 Google authentication and Firestore-backed user study data.
- 🌗 Responsive dark/light UI.

## Tech stack

**Frontend:** React 19, TypeScript, Vite, Tailwind CSS, Lucide React, Motion

**Backend:** Node.js, Express, Vercel serverless handlers, WebSocket

**AI:** Google Gemini via `@google/genai`

**Data/Auth:** Firebase Authentication and Cloud Firestore

## Local development

### Requirements

- Node.js 20+
- A Gemini API key for AI features
- Firebase project configuration for authentication and Firestore

### Setup

```bash
git clone https://github.com/saikishore2410/NoteVault.git
cd NoteVault
npm install
```

Create a local `.env` from `.env.example` and configure:

- `GEMINI_API_KEY`
- `APP_URL`

Then start the development server:

```bash
npm run dev
```

The app runs on `http://localhost:3000` by default.

## Quality checks

Run the same checks used by CI:

```bash
npm run lint
npm test
npm run build
```

## Deployment

### Vercel

The `api/` directory contains Vercel-compatible serverless handlers. Configure `GEMINI_API_KEY` in the Vercel project environment variables before deploying.

### Custom Node server

The root `server.ts` provides the full Express + WebSocket development/server runtime.

## Security notes

- Never commit a real `GEMINI_API_KEY` or other secrets.
- Firestore authorization is enforced in `firestore.rules`.
- Keep production API keys in the hosting provider's secret/environment-variable store.
