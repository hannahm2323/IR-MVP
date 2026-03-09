# IR-MVP: What to do next

If you’re asking, **“what is the next step I need to make?”** — this is the practical answer:

## Next step (do this first)
Build a **clickable MVP prototype** with:
1. Welcome screen
2. Onboarding form (name + date of birth)
3. Timeline view (year circles from birth year → current year)
4. “Add memory” modal/card

---

## Step-by-step plan

### Step 1) Scaffold a frontend app
Use React + Vite for speed:

```bash
npm create vite@latest ir-mvp-app -- --template react
cd ir-mvp-app
npm install
npm run dev
```

Open the URL shown in terminal (usually `http://localhost:5173`).

### Step 2) Create basic pages/components
Create these components first:
- `WelcomeScreen`
- `OnboardingForm`
- `TimelineCanvas`
- `MemoryCardModal`
- `EzraGuideBubble`

### Step 3) Add minimal state model
Start with local state (no backend yet):

```ts
type User = { name: string; dateOfBirth: string };

type MemoryCard = {
  id: string;
  date: string;
  title: string;
  story: string;
};
```

### Step 4) Implement onboarding logic
- Ask for `name` + `dateOfBirth`.
- On submit, generate years from birth year to current year.

### Step 5) Render timeline circles
- Center horizontal axis.
- One circle per year.
- Memory circles above/below the year axis.

### Step 6) Add memory creation
- Click year → open “Add memory” modal.
- Save title/story/date.
- Show memory circle linked to that year.

### Step 7) Add very light zoom/pan (MVP)
- Mouse wheel zoom on timeline container.
- Drag to pan.
- Keep this simple at first.

### Step 8) Ship a working v0
- Push to GitHub.
- Deploy on Vercel/Netlify.
- Then iterate on design polish and Ezra guidance.

---

## Definition of done for this next milestone
You’re done with the next step when you can:
1. Enter name + DOB
2. See generated year timeline
3. Add one memory card
4. Re-open and edit that memory

That gives you a **real, testable prototype** instead of concept docs only.
