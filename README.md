# The Team Rocket Method (TRM)

**A governance protocol for running two or more AI models as one disciplined crew: distinct named
seats, adversarial cross-review, file-based shared memory, automated gates, and a human boss who
rules every fork. The models argue. The boss decides.**

By [Medick](https://github.com/medick51o). Conceived 2026-07-11. **PRIVATE — working concept.**

---

## The family — one engine, three tiers

The method is split so the *discipline* lives in one place and the *personality* layers on top:

- **[SPINE.md](SPINE.md)** — the engine. The whole method, brand-neutral: routing, the five ship gates,
  cross-vendor review, the write-set fences, the ladder of truth. Every tier runs this.
- **[CREW.md](CREW.md)** — the crew. The permanent cast (Jessie 🟠 · James 🔵 · Butch 🔴 · Cassidy 🩷 ·
  the cat 😼), the casting law (incl. the full-vendor council), the rival review pairs, the mentor mandate.
- **[SHOW.md](SHOW.md)** — the show. The premise, chemistry, and vibe that make it a playground.

### The three tiers — thinnest to fullest

Each tier is its own repo — same engine, different amount of personality. **Go try the others:**

| Tier | Repo | Loads | What it is |
|---|---|---|---|
| 🟡 **Anderson's Dispatch Deck** | **[→ andersons-dispatch-deck](https://github.com/medick51o/andersons-dispatch-deck)** | SPINE | heavy multi-model orchestration, straight-faced — model names, no cast |
| 🟠 **Team Rocket Method** *(you're here)* | this repo | SPINE + CREW | the disciplined crew — named seats, rival cross-reviews |
| 🚀 **Team Rocket Takes Over** | **[→ team-rocket-takes-over](https://github.com/medick51o/team-rocket-takes-over)** | SPINE + CREW + SHOW | the full agentic-AI playground — cast, cat, episodes |

Same spine underneath — each tier just adds a layer. **[MIGRATION-MAP.md](MIGRATION-MAP.md)** traces how the
original single-file editions were split into this, section by section (nothing dropped).

---

## What the crew is capable of

TRM runs a **permanent cast** — the models are costumes, the roles never move:

| | Seat | What it does |
|---|---|---|
| 😼 | **The Cat** | orchestrates — reads each job, routes it to the right model, fences the builders apart, and *teaches you why* as it goes |
| 🟠 | **Jessie** | lead builder, and your conversational seat |
| 🔵 | **James** | second builder — the independent, unloyal read when the seats flip |
| 🔴 | **Butch** | reviews James's code — cross-vendor, never James's own vendor (default **Claude**); his signature *build* seat is **Grok ⚫** |
| 🩷 | **Cassidy** | reviews Jessie's code — cross-vendor (default **Codex**); her signature *build* seat is **Gemini 🟢** |
| 👑 | **The Boss** | you — assign the mission, rule every fork, merge |

What that buys you:

- **Parallel builds, fenced** — two builders work at once on *disjoint files*, never the same file in one pass.
- **Adversarial cross-vendor review** — a reviewer never shares the builder's vendor (different training, different blind spots, real catches); a review laundered through the builder's own lineage is declared invalid.
- **Gates before "done"** — claims capped at evidence: *"gates pass,"* never *"it works."* The human is the final gate and the only one who merges.
- **A mentor while it works** — the cat drops a one-line *why-this-route* at each real decision, so you get sharper at orchestration every session.

## Why this model, not that one

The cat routes by **strength, not loyalty.** The default arsenal:

| Model | Reach for it when you need… |
|---|---|
| 🟠 **Claude** | deepest reasoning, architecture, honest judgment — design, specs, root-cause, reviewing others |
| 🔵 **Codex** | precise bounded builds, and the sharpest code review (it *proves* bugs, cites sources) |
| ⚫ **Grok** | fearless one-shot visual work — UI, skins, concept pages |
| 🟢 **Gemini** | budget builds, image generation, overflow capacity, and an independent 4th vote |

Any character can wear any model — **these seats are strong defaults, not law.** The cat casts by the job (the *one* rule it never breaks: a reviewer is never the builder's own vendor), and the banner always shows the real vendor under it (*🟠🟢 = a Claude brain on the Gemini seat*).

---

## Legacy

The original single-file edition — the `TRM-FOUNDATION` + manual form the method grew from — is archived
under **[legacy/](legacy/)** for provenance. It is superseded; the current method is the SPINE / CREW /
SHOW family above.
