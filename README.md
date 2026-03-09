# IR-MVP

This repository currently contains the **product concept** for IR-MVP.

- Main concept doc: [`PRODUCT_CONCEPT.md`](./PRODUCT_CONCEPT.md)
- Build plan: [`NEXT_STEPS.md`](./NEXT_STEPS.md)

## Can I view this on localhost from GitHub?
Short answer: **GitHub itself is not localhost**.

- On GitHub.com, you can view files and Markdown previews.
- To view anything on `http://localhost:...`, you must run a server on your own machine (or Codespaces).

## Run this repo locally (quick start)

### 1) Clone the repo
```bash
git clone https://github.com/<your-username>/IR-MVP.git
cd IR-MVP
```

### 2) Start a simple local server
Since this repo is docs-only right now, you can still host the files locally:

```bash
python3 -m http.server 8000
```

Then open:
- <http://localhost:8000>

You can click `PRODUCT_CONCEPT.md` from the directory listing.

## If you want a real app on localhost
Right now there is **no runnable frontend/backend code yet** (only concept docs). 

To make it behave like an app, next step is to scaffold a project (for example React/Next.js), then run:

```bash
npm install
npm run dev
```

(Those commands will work only after app code is added.)

## Suggested next implementation step
Build a first clickable prototype with:
1. Welcome screen
2. Onboarding form (name + date of birth)
3. Generated birth-to-present timeline with year circles
4. Memory card modal

Use `PRODUCT_CONCEPT.md` as the implementation reference.
