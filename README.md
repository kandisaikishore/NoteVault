# NoteVault — Handwritten Notes Hub & AI Study Toolkit

[![TypeScript](https://img.shields.io/badge/TypeScript-React-blue?logo=typescript)](https://www.typescriptlang.org/) [![Vite](https://img.shields.io/badge/Build-Vite-646CFF?logo=vite)](https://vite.dev/) [![GitHub](https://img.shields.io/badge/Source-GitHub-181717?logo=github)](https://github.com/saikishore2410/NoteVault) [![Issues](https://img.shields.io/github/issues/saikishore2410/NoteVault)](https://github.com/saikishore2410/NoteVault/issues)

**Turn handwritten STEM notes into searchable, reusable study material.**

NoteVault is a web-based study workspace for organizing handwritten academic and technical notes and using AI-assisted tools for revision, exploration, and knowledge discovery.

## Highlights
- Search and filter notes by subject, topic, tags, author, and extracted text.
- Browse multi-page notes with zoom, thumbnails, bookmarks, and study-history features.
- Use Gemini-powered OCR to help digitize handwritten material.
- Explore a multi-turn STEM tutor with optional search grounding where configured.
- Access audio transcription and voice-study workflows when required services are configured.
- Generate or edit diagrams and explore additional study tools.
- Sign in with Google and store study data using Firebase Authentication and Cloud Firestore.
- Responsive interface with dark and light themes.

AI features depend on external API access and quotas; review generated output for accuracy.

## Technology stack
- Frontend: React 19, TypeScript, Vite
- Styling/UI: Tailwind CSS, Lucide React, Motion
- Server: Node.js, Express, Vercel-compatible handlers, WebSocket
- AI: Google Gemini via @google/genai
- Identity/data: Firebase Authentication and Cloud Firestore

## Run locally
Requirements: Node.js 20+, npm, Firebase configuration, and a Gemini API key for AI features.

    git clone https://github.com/saikishore2410/NoteVault.git
    cd NoteVault
    npm install

Copy .env.example to .env and configure GEMINI_API_KEY and APP_URL. Complete Firebase configuration using project-specific values. Never commit secrets.

    npm run dev

The development server is configured for port 3000 by default.

## Quality checks
    npm run lint
    npm test
    npm run build

## Deployment
The repository includes Vercel-compatible handlers and vercel.json. Configure environment variables and review Firestore rules before deploying. A live URL is not listed because one has not been verified.

## Security and responsible use
Keep API keys out of source control, review Firestore rules, and avoid uploading sensitive material without permission. OCR and AI-generated answers are assistive outputs, not guaranteed facts.

## Contributing
Bug reports should include reproduction steps and expected behaviour. Pull requests should include relevant tests.

## License
No license file is currently declared. Add a license before granting reuse permissions.
