# Trawly — Future Features

**Status:** Deferred from MVP. Each feature listed with target timing and brief description.

---

## Post-Launch Roadmap

### 🎧 Audio Edition — Month 2 Post-Launch

A spoken version of the daily digest, generated via high-quality TTS. Subscribers can listen to their personalised digest during their commute, workout, or while making breakfast. Same editorial content, optimised for audio — shorter sentences, natural transitions, conversational delivery. Likely 8-12 minutes per episode.

**Dependencies:** Format workshop (to nail the written format first), TTS provider selection, audio hosting.

---

### 📚 Sunday Deep Trawl — Month 3

A weekly long-form edition that goes deeper on 2-3 topics from the week. Instead of the daily 5-minute scan, the Sunday edition is a 15-20 minute read with extended analysis, multiple perspectives, and "what to watch next" for each topic. Think of it as the magazine supplement to the daily newspaper.

**Dependencies:** Enough subscriber data to know which topics resonate most. Format workshop.

---

### 🤝 Shared Editions — Month 4

Send a curated edition to someone else. Not a referral link — an actual personalised digest you can gift. "I think my friend would love this." Trawly generates a one-off edition based on what the gifter knows about the recipient. A better viral mechanism than referral codes because it delivers immediate value.

**Dependencies:** Gifting UX design, one-off digest generation pipeline.

---

### 🔮 Prediction Tracker — Month 5

Trawly surfaces predictions from the content it curates ("Analyst X says BTC will hit $200K by Q4") and tracks them over time. Monthly, it reports back: "Here's how the predictions we flagged are holding up." Builds a track record of source reliability and gives subscribers a reason to stay long-term.

**Dependencies:** Prediction extraction in pipeline, tracking database, follow-up composition logic.

---

### ⏱️ Tempo Control — Month 6

Let subscribers choose their digest frequency and depth:
- **Daily quick** (current default — 5 min read)
- **Daily deep** (10 min read, more items, longer commentary)
- **3x/week** (Mon/Wed/Fri, slightly longer)
- **Weekly** (one big Saturday digest)

Each tempo has its own editorial approach — weekly isn't just 7 dailies stitched together.

**Dependencies:** Multi-depth composition templates, scheduling logic, cohort-based pipeline.

---

### 🎭 Voice & Tone Personas — Month 7

Choose how Trawly talks to you:
- **The Analyst** — data-driven, precise, minimal opinion
- **The Friend** — casual, opinionated, lots of personality (current default)
- **The Professor** — educational, explains concepts deeply
- **The Contrarian** — challenges every narrative, devil's advocate

Each persona changes the Opus composition prompt while keeping the same curated content.

**Dependencies:** Persona prompt library, A/B testing framework, preference UI.

---

### 🐰 Rabbit Hole Button — Month 8

A standalone feature (separate from the widget). When a subscriber clicks "Go deeper" on any digest item, Trawly generates an extended deep-dive — 10-15 minutes of reading on that specific topic, pulling from additional sources, academic papers, historical context. Delivered as a follow-up email within the hour.

**Dependencies:** On-demand generation pipeline, additional source fetching, cost management (each deep dive is an additional Opus call).

---

### 🎁 Year in Knowledge / Wrapped — End of Year 1

Annual summary of everything the subscriber read through Trawly:
- Topics they engaged with most
- How their interests evolved over the year
- Total time saved
- Most-clicked sources and authors
- Predictions that came true
- A personalised "Your Year in Knowledge" shareable card

Inspired by Spotify Wrapped but for intellectual curiosity.

**Dependencies:** 12 months of engagement data, shareable card generation, web page for sharing.

---

### 🎂 Birthday Briefs — Future

Pre-generate 365 birthday-themed digest templates (one for each day of the year), then serve the relevant one on the subscriber's birthday with Opus personalisation layered on top. A delightful surprise that shows Trawly knows them.

**Dependencies:** Birthday collection during onboarding, template library, scheduling logic.

---

### 💬 Quote Cards — After Format Sprint

Beautiful, shareable quote cards generated from the best lines in each digest. Subscribers can share them on social media with Trawly branding. Organic social growth mechanism.

**Dependencies:** Format sprint (to nail visual identity), card generation pipeline, social sharing infrastructure.

---

### 🔍 Source Scouting Report — After Format Workshop

A periodic report on the sources Trawly pulls from for each subscriber:
- Which publications appear most in their digest
- Source reliability scores
- New sources discovered this month
- Sources that are trending up/down in quality

Transparency about where the information comes from.

**Dependencies:** Source tracking database, reliability scoring model, format workshop.

---

### 📊 Monthly Wrap-Up (Detailed Design) — After Format Workshop

The monthly wrap-up email concept is confirmed for MVP (basic version), but the detailed design — visual layout, interactive elements, shareable components — is deferred until after the format workshop establishes the visual language.

---

## Removed Features (Not Coming Back)

These were explored and explicitly rejected:

| Feature | Why Removed |
|---------|-------------|
| **Scorecard** ("top 12% of readers") | Gamification doesn't fit brand; feels manipulative |
| **Versus Cards** (polls/voting) | Adds friction without clear value |
| **Cultural Passport** (reader identity profile) | Over-engineered; taste profile does this implicitly |
| **Mood Read** (choose news tone) | Too complex; editorial voice should be consistent |
| **Empty Inbox Brag** | Unnecessary; we just do smaller catches on quiet days |

---

### 🔕 Silent Pause Sequence — Future

**When:** Post-MVP (Month 2-3)

Instead of guilt-tripping inactive readers, automatically pause their digest and let them restart when ready. Proposed sequence: reduce frequency at 2 weeks, auto-pause at 3 weeks, gentle check-in at 6 weeks. Exact timing TBD. Builds trust and reduces real churn vs surface-level unsubscribes.

**Dependencies:** Engagement tracking, pause state in subscriber profile, re-activation flow.

---

### 📖 Glossary Layer — Future (Pending Format Workshop)

**When:** Post format workshop — needs to be prototyped to see if it feels natural

Inline parenthetical definitions for complex terms. Tracks which concepts each reader has encountered and stops explaining them over time. Reader gradually "levels up." Email-safe approach: parenthetical text, not hover tooltips.

**Dependencies:** Concept tracking in subscriber profile, Opus prompt engineering.
