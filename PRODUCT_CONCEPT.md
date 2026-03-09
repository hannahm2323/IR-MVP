# IR-MVP Product Concept: "Your Life, Intentionally Curated"

## 1) Product Vision
A private, calm, and joyful memory-keeping app that helps people curate meaningful life moments over time.

This is **not** a social network and **not** a bulk photo backup tool. It is a guided, intentional scrapbook timeline for reflection, storytelling, and preserving family history.

## 2) Who It Is For
1. People overwhelmed by huge, messy digital photo libraries.
2. Scrapbookers and journalers who want a digital ritual.
3. Families preserving stories for future generations.
4. People exploring memory gaps as part of self-discovery.

## 3) Core Product Principles
- **Private first**: Your memories are yours.
- **Curation over collection**: Highlights, not every file.
- **Slow software**: Encourages intentional reflection, not endless scrolling.
- **Visual clarity**: Colorful, modern, uncluttered.
- **Chronological grounding**: Every memory has a place in time.

## 4) MVP1 Experience Overview
MVP1 focuses on one user and one private timeline.

### Key Features
- Welcome + onboarding flow.
- Collect user name + date of birth.
- Auto-generate a timeline from birth year to current year.
- Show one circle per year on the main timeline axis.
- Allow adding memory circles above/below years.
- Open a memory/date card and add details:
  - Story text
  - Photos
  - Audio clip
  - Optional tags/people/place
- Include **Ezra**, a colorful, supportive in-app guide with stage-based variants.

## 5) Information Architecture

### Primary Objects
- **User**
  - id
  - name
  - dateOfBirth
  - createdAt
- **YearNode**
  - year
  - ageAtYear
  - hasMemories
- **MemoryCard**
  - id
  - date (or date range)
  - title
  - story
  - media[] (image/audio)
  - emotions/tags (optional)
  - people/places (optional)
  - createdAt
  - updatedAt

## 6) Screen Concepts

### A) Welcome Screen
**Goal:** Invite users into a calm, meaningful journey.

**Content blocks**
- Warm headline (e.g., "Let’s build your life timeline")
- Short value proposition (curate memories intentionally)
- Ezra intro illustration
- CTA: **Start my timeline**

### B) Onboarding Screen
**Goal:** Gather minimal data to generate the initial timeline.

**Fields**
- First name (required)
- Date of birth (required)

**Behavior**
- Validate required fields.
- On submit, create timeline from birth year to current year.
- Drop user into first timeline view.

### C) Timeline Screen (Core)
**Goal:** A visual chronology that feels playful and reflective.

**Visual model**
- Horizontal center axis with year circles in sequence.
- Memory circles appear above/below year circles.
- Colorful palette with clear contrast.
- Smooth zoom and pan interaction (Figma/Canva style):
  - Zoom out: decade-level overview.
  - Zoom in: year/month/day detail and memory density.

**Interactions**
- Click/tap a year circle → focus that year.
- Click/tap a memory circle → open card.
- Add memory button (+) anchored to selected year/date.

### D) Memory Card Detail
**Goal:** Capture story-rich moments, not just media.

**Fields**
- Date
- Title
- Story
- Add photo(s)
- Add audio clip
- Optional metadata: people, place, tags, emotions

**Tone**
- Gentle prompts: "What made this moment meaningful?"
- Encourages reflection over speed.

## 7) Ezra Guide Design (MVP1)
Ezra appears as a supportive, colorful companion.

### Ezra states
1. **Welcome Ezra**: introduces purpose and calm tone.
2. **Setup Ezra**: helps complete onboarding.
3. **Explorer Ezra**: helps navigate timeline and zoom.
4. **Reflection Ezra**: prompts deeper storytelling in cards.

### Ezra UX rules
- Optional and dismissible.
- Short, supportive microcopy.
- Never intrusive; appears contextually.

## 8) Interaction Model for Zoomable Timeline

### Zoom levels
- **Level 1 (Far):** years only, memory density hints.
- **Level 2 (Mid):** years + visible memory circles.
- **Level 3 (Near):** exact dates and card previews.

### Navigation
- Mousewheel/pinch for zoom.
- Click-drag for pan.
- "Jump to year" quick input.
- "Today / Current age" shortcut.

## 9) Design Language
- Calm dark or soft neutral background.
- Colorful circle system for emotional warmth.
- Rounded geometry and spacious layout.
- Minimal chrome, focus on timeline canvas.
- Gentle motion and microinteractions.

## 10) MVP1 Non-Goals
- No social sharing feed.
- No algorithmic engagement loops.
- No "import every photo automatically" setup.
- No multi-user collaboration in MVP1.

## 11) Suggested MVP1 Success Metrics
- Onboarding completion rate.
- % users who create first memory card.
- Median memories added in first 7 days.
- Return rate for reflective sessions (Day 7/Day 30).
- Time spent in card writing vs. upload-only behavior.

## 12) Future Directions (Post-MVP)
- Family vault / shared history modes.
- Guided reflection journeys by life stage.
- Voice-to-memory transcription.
- Print-ready timeline exports.
- Prompt packs (childhood, school years, travel, family stories).

## 13) Draft Microcopy
- "Start your timeline"
- "Add a meaningful memory"
- "What happened, and why does it matter to you?"
- "You don’t need everything—just what matters most."
- "Pick one memory for this year."

## 14) One-Sprint Prototype Plan
1. Build onboarding (name + DOB).
2. Generate year nodes from DOB year to current year.
3. Render horizontal year-circle timeline.
4. Add simple memory circles tied to year/date.
5. Build memory card modal with story + image/audio upload stubs.
6. Add basic Ezra helper bubbles for key moments.

---
This concept intentionally balances emotional storytelling with a modern, zoomable timeline interaction so memory-keeping feels like a mindful creative ritual.
