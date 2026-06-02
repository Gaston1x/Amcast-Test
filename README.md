# AMCAT / SHL Style English Practice Lab

Static React practice app for AMCAT-style voice preparation:

- Full AMCAT sequence from Part A to Part G
- Speaking practice modes
- Local account creation/login
- Per-user question history with no-repeat question selection
- LocalStorage persistence

## Run Locally

From this folder:

```bash
npm run serve
```

Then open:

```text
http://127.0.0.1:8765/
```

Published GitHub Pages URL:

```text
https://gaston1x.github.io/Amcast-Test/
```

The full app is available at the repository root through `index.html`, so it can
open directly from GitHub Pages without command-line setup.

## Data Persistence

Accounts and used-question history are stored in the browser with `localStorage`.
This is intended for practice only. For production, replace this with a backend
such as Firebase, Supabase, or a custom API.

## No-Repeat Rule

Each question receives a stable content-based ID. When a user sees a question,
that ID is saved to the user's history. The app excludes those IDs from future
practice and full AMCAT simulations for that same user.
