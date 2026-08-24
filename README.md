# The Team Rocket Method (TRM)

**A governance protocol for running two or more AI models as one disciplined crew: distinct named
seats, adversarial cross-review, file-based shared memory, automated gates, and a human boss who
rules every fork. The models argue. The boss decides.**

By [Medick](https://github.com/medick51o). Conceived 2026-07-11. Running engine: **`spine v2.6`**.

> *The name's a wink: an unnamed parody of a certain childhood cartoon's ever-scheming villain trio (the one with the pocket-sized monsters). We'll never print the show's name — if you know, you know.* 😏

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

Same spine underneath — each tier just adds a layer.

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

### What the crew learned to do lately (`spine v2.6`)

| | Feature | What it means at the table |
|:--:|---|---|
| 🔌 | **The seats remember** | Brief a seat once and continue that same conversation later. Reviewers stay blind on purpose — a fresh call is what independence requires. |
| 🟣 | **A bench of 200+ models** | One CLI reaches a whole roster, so the cat can cast a seat in a model you don't hold a subscription for. |
| 💳 | **Nobody spends without the boss** | A seat that *can* bill needs a recorded allowance first — a bound, with an expiry. No allowance, no spend. Free seats never ask. |
| 📊 | **The meter is read, not guessed** | Usage comes from each vendor's own billing endpoint. *"That's cheap"* is **"it works" wearing a hat.** |
| 🛡️ | **A read-only seat is really read-only** | Three genuine escape routes found and closed — including a read-only seat that escalated by getting *another seat* to do its writing. |
| ⚖️ | **The law was swept for contradictions** | A four-vendor blind council re-read the whole engine and found nine places two rules disagreed. All nine repaired. |
| 📜 | **History kept, not carried** | The war stories behind the laws moved to their own file, so they still exist without being re-read on every summon. |

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

## The seats REMEMBER — persistent MCP transports (2026-08-22)

The crew's vendor seats no longer have to be amnesia one-shots. Any CLI you actually have
(Codex / Grok / Gemini — vendors are suggestions, never requirements) can be registered into
Claude Code as a **persistent MCP seat**, opt-in and reversible with one command: brief a seat, get a session id back,
continue that exact conversation later with full context. Reviewers are still ALWAYS fresh calls
(fresh = blind, which independent review requires — though blind alone is *necessary, not
sufficient*: the reviewer also needs a different effective-model vendor than the build, or to
be human-launched); a reply-chained session stays in its
owning-seat lineage forever. Wiring, wrapper scripts, and the acceptance test:
[`mcp-seats/`](https://github.com/medick51o/andersons-dispatch-deck/tree/main/mcp-seats) in the
Anderson's Dispatch Deck repo. Doctrine is owned by [SPINE.md](SPINE.md) v2.0 (THE TRANSPORT LAW) and rendered for the crew in [CREW.md](CREW.md).

## The crew legend — v4 at a glance (full version in [CREW.md](CREW.md))

*😼🟠➤* the conductor wears the **➤ baton** · 🔨 building · 📝 reviewing (🔴 is Butch's jersey,
never an act) · ⛔ rejected/blocked/needs-boss · 🌈👥👥 council in session · 🚩 finding · 🧪 gates ·
🩺 doctor-first · 🚢 shipped · 👑🏁 boss-validated · 🟤 quiet hold. An episode reads as a timeline:
🩺 → 🌈👥👥 → 🟠🔨 → 🧪 → 🔵📝→⛔ → 🟠🔨 → 🧪 → 🚢 → 👑🏁 → 🟤

## The Council — the whole crew, one hard question

When the stakes justify it, the boss can convene **the council**: the cat brings the crew in at once — **a bounded set of eligible seats, one vendor each** (the cap is set before it runs, and a seat that would bill needs the boss's allowance first) — each giving an independent, *signed* read on the same question, each on a distinct lens. Four vendors, four sets of blind spots, so the council catches what any single seat would miss. The cat synthesizes best-of-breed, **names every disagreement**, caps the debate at two rounds, and hands you the verdict. It's the **special move** — adversarial review at full width — not the everyday default. **It never auto-fires:** a trivial ask stays a trivial ask (one seat, no token-eating dream team). *(Same engine move across the family: a plain panel in the [Dispatch Deck](https://github.com/medick51o/andersons-dispatch-deck), a full puppeteered set-piece in [Team Rocket Takes Over](https://github.com/medick51o/team-rocket-takes-over).)*

---

## Legacy

The original single-file edition — the `TRM-FOUNDATION` + manual form the method grew from — is archived
under **[legacy/](legacy/)** for provenance. It is superseded; the current method is the SPINE / CREW /
SHOW family above.
