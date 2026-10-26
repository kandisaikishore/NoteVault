# Development, Data Integrity, and Privacy Guide

NoteVault is a TypeScript/React notes and study-toolkit project. Check the current source and package manifests to confirm which study, AI, export, and persistence features are implemented.

## Setup

```bash
git clone https://github.com/kandisaikishore/NoteVault.git
cd NoteVault
```

Install dependencies using the package manager and scripts declared by the project. Configure any AI-provider keys locally; do not commit credentials or private note content.

## Notes and persistence tests

For implemented note workflows, test:
- Create, edit, delete, and search
- Empty content, long content, Unicode, and special characters
- Refresh/restart behavior for the documented persistence layer
- Malformed stored data and recovery from interrupted writes
- Duplicate identifiers and repeated save actions
- Export/import round trips if those features exist

Validate imported data before replacing existing notes. If persistence fails, show an actionable error and avoid reporting that content was saved when it was not.

## AI/study-tool boundaries

If AI assistance exists, mock the provider in automated tests. Cover missing credentials, timeouts, malformed output, and empty retrieval results. Do not fabricate source references or claim a note was retrieved when retrieval failed. Keep sensitive note text out of logs by default.

## Privacy and deletion

Document whether notes are stored in browser storage, a local file, or a remote service. Explain the actual deletion and backup behavior. If accounts exist, test that notes are isolated per user.

## Pull-request checklist

- [ ] Add regression tests for the changed note workflow.
- [ ] Run the current test, lint, type-check, and build scripts.
- [ ] Test malformed imports and persistence failures where applicable.
- [ ] State which external integrations were mocked.
- [ ] Avoid real user notes in fixtures and screenshots.
