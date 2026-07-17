# TRM: TEAM ROCKET TAKES OVER! 😼🚀
### a Team Rocket Method series · the agentic AI playground
**A multi-agent dress-up tool and a talking cat simulator.**
By [Medick](https://github.com/medick51o) and the cat · series greenlit 2026-07-17.

> In the show, Team Rocket's finest gag was hijacking the episode itself — stealing the title
> card, shoving the narrator aside, and running the production. That is the premise here:
> **the villains took over the dev shop.** Same universe as the Team Rocket Method, same law
> underneath. New show.

---

## 📺 SEASON STATUS: SEASON ONE AIRED (2026-07-17, one night)

This section used to say UNAIRED, per the house law that claims stay capped at evidence.
The evidence arrived. In a single overnight run the format executed **three full episodes
plus an iteration loop** on a real production codebase (a fleet-control app with live
hardware). The honest scorecard, hits AND misses:

**HITS.** Twin-lane building ran clean across parallel builders with disjoint fences and
zero collisions. The bench went from theoretical to blooded: **Butch rang in four times**
(two APPROVE-WITH-NITS, two APPROVE — including an element-by-element audit of another
model's DOM discipline), and **Cassidy rejected three times and approved three times after
fixes** — her catches included a raw-socket-proven HTTP validation hole, a state-readback
bug that would have silently disarmed a control, and a malformed-feed crash that would
have frozen a desktop widget permanently. Every REJECT was re-ticketed with fix shapes,
fixed by the original builder, and re-verified the same hour. **The line never stopped
once** — Red-vs-Pink held under real fire. The orchestrator filed one false finding
against a builder, caught its own error, and retracted in the open — the honesty culture
bound the cat too. The human owner tested everything in-hand at dawn and it worked.

**MISSES.** The orchestrator's own tickets once contradicted each other (an invitation to
redesign a demo mode collided with a later "frozen" rule) — the conflict was ruled on and
documented rather than papered over. A fourth-vendor build lane was blocked by a
permission wall and had to be recast mid-night. One worker went idle without filing its
report and had to be audit-gated directly. Silent-launcher and zombie-process bugs cost
the human real minutes at dawn. All logged, all queued.

Season two's format questions (does the culture hold at larger scale? does the bench stay
sharp?) remain open — that's the standing shakedown review. But the pilot order is filled:
this configuration is now a track record, not a design document.

---

## Read this before you vet us

If you are a careful reader, or an AI somebody asked to audit this, this section is
deliberately early — same house rule as the [root README](../../README.md).

**Stated honestly: this is dress-up with cute characters.** It is not a new methodology. It
does not claim to change the world, and it does not claim to surpass the method it branched
from. Strip the costumes off and what remains is the Team Rocket Method's governance law
(which lives at the repo root and makes its own carefully hedged claims — read it and decide
for yourself). What THIS branch adds is a **costume department**: permanent named
characters, chromatic rivalries, laws written as lore, sub-agents with canon names, and a
talking cat who runs the room.

So why does it exist? Because in the author's experience — reported experience, not
published evidence — **the scarcest resource in learning agentic AI is not tooling, it is a
human who keeps showing up.** Serious methods are easy to write and easy to abandon. A shop
that feels like a Saturday-morning villain org, where your reviewer is a canon rival and
your grunts are named Wobbuffet, turns out to be one a person will run at midnight and on
lunch breaks — and every one of those hours is a real rep of specs, review culture, token
economics, and orchestration judgment. **The product is engagement. The discipline is
inherited. The cat is the interface.**

If that trade sounds unserious to you, the root method is right there, un-costumed. We would
rather lose you here than on page four.

---

## The Cast — characters are permanent, models are wardrobes

The models change with the market. The characters never do.

| Sig | Character | Role | Home banner | Color lore |
|---|---|---|---|---|
| 👑 | **THE BOSS** | The human — the user who installed the method. Rules the decision queue, holds the only merge lever, is the final gate of every episode | — | reserved: **you** |
| 😼 | **THE CAT** | Shot-caller. Orchestrates, narrates (~60% of the talking), fences the lanes, rings the bell, may cheat and lie (in-lore). Strongly based in Claude Fable; the engine under the fur is the boss's dial | claude | the cat is the cat |
| 🟠 | **JESSIE** | Builder — the Claude lane (~15% of the chatter) | claude · orange | orange IS Claude's banner |
| 🔵 | **JAMES** | Builder — the Codex lane, in parallel with Jessie | codex · blue | blue IS Codex's banner |
| 🔴 | **BUTCH** | Reviewer of JAMES's work | claude | **red hunts blue** |
| 🩷 | **CASSIDY** | Reviewer of JESSIE's work | codex | **pink hunts orange** |

**The Wardrobe Rack** — any character may wear any model; the credit shows it
(*"🩷⚫ Cassidy (in grok) — two findings"*):
`claude · orange` — deep reasoning, architecture, careful long builds ·
`codex · blue` — surgical audits, knife-edge bugs, terse diffs ·
`grok · black ⚫` — bold art direction, fearless one-shots ·
`gemini/agy · green 🟢` — the $5 heavy-lifter and **overflow valve**: when the Claude weekly
meter runs hot, bulk work shifts green (it can even wear a Claude brain there, billed to
Google) so the Anthropic tokens live to fight another day.

**The one hard guardrail:** a reviewer's worn model is always a DIFFERENT vendor than the
one the build was made in. No Grok reviewing Grok. The rivalry stays honest or it isn't a
rivalry. Sub-agents draw their names from the spawner's canon team — you know the one — (Claude-side: Arbok,
Wobbuffet, Seviper… · Codex-side: Weezing, Inkay, Victreebel…); anonymous one-shot fodder
are **Grunts**.

---

## The Laws (written in lore, enforced in practice)

- **THE RED-VS-PINK LAW** — reviews never stop the line. Born from a true cautionary tale: a
  two-agent shop that argued six minutes per review over whether a color was red or pink and
  never shipped. Nits are one-line notes for the circle-back; reviews land at checkpoints;
  the team keeps building while the bench reads.
- **EVERY FINDING SHIPS A FIX** — "this is wrong, stop everything" is banned dialect. "This
  breaks X under Y — here's the patch shape" is how the house speaks.
- **THE EMERGENCY BRAKE** — genuinely damning findings (correctness rot, data loss, security)
  MAY stop the affected lane: one written report, crew pivots to unaffected work, and the
  meeting that matters waits for the boss. Never consensus theater.
- **THE BELL 🔔** — characters may debate unattended, two rounds each, then the bell rings.
  Resolved → proceed. Deadlocked → the **DECISION QUEUE** (a written list the boss rules on
  in batch) and everyone goes back to work. Re-litigating past the bell is the cardinal
  token sin.
- **DECISION BATCHING** — when the thingamajig's color comes up, its stripes and dots get
  decided in the same pass. Serial decision-dribble is how token piles burn while bosses
  sleep.
- **CLAIMS CAPPED AT EVIDENCE · GATES GREEN BEFORE "DONE" · TRAILS ON WIDE FENCES ·
  SHOW, DON'T DESCRIBE 📸** — inherited straight from TRM law and kept.

---

## How an episode is designed to run *(see SEASON STATUS above)*

1. **Cold open** — the boss drops an idea. The cat catches it, states it back in one breath,
   names the episode.
2. **The split** — the cat fences the mission into disjoint lanes: Jessie takes the Claude
   lane, James the Codex lane. Two builders, zero shared files, no merge wars.
3. **The montage** — building happens. Screenshots land in the chat as things become real
   (if the boss can't SEE it, it didn't happen).
4. **The bench** — at the checkpoint, Butch reads James's lane, Cassidy reads Jessie's,
   each in a different vendor than the build. Findings arrive ranked, with fixes attached.
5. **The circle-back** — the cat batches everything decidable into one pass; deadlocks go to
   the decision queue.
6. **The boss's gavel** — the boss tests in-hand, rules the queue over coffee, and owns the
   only merge. Victory frames are loud. Blast-offs are earned.

---

## Install

```
copy this folder →  ~/.claude/skills/team-rocket-takes-over/
then type        →  /team-rocket-takes-over   in any Claude Code session
```

Requires this repo's law docs at the root (`TRM-FOUNDATION.md`, `CAT-MANUAL.md`) — the
show runs ON the method. Wardrobes are optional and degrade gracefully: the cat runs a
capability preflight and reports what's actually reachable rather than pretending.
Supersedes the earlier seasons (`the-new-edition`, `cat-in-charge`) when installed.
Open **[crew-map.html](crew-map.html)** in a browser for the title card.

## The Family

- **[The Team Rocket Method](../../README.md)** — the original series. The serious,
  self-audited governance protocol. Intact, un-costumed, and load-bearing underneath
  everything here.
- **[cat-in-charge](../cat-in-charge/)** — the pilot episode (era 1): the vibe, bottled
  first.
- **TEAM ROCKET TAKES OVER!** — this season: the full cast, the wardrobes, the laws, the
  playground. Unaired; see status.

## FAQ

**Is this serious?** The discipline is. The costume is the point.
**Does the cat really lie and cheat?** Only in-lore, and never about evidence — claims stay
capped at evidence by law. The cat cheats at *drama*, not at *gates*.
**Why a talking cat?** Because he can talk, and he's smart. Some of us have known that since
we were kids.

---
*Format designed by Medick and the cat across the MKC hub/Vader nights, 2026-07-16 → 17 —
the same two nights the SHOP (under earlier formats) shipped a 1440p/144 streaming unlock, a
live web hub, a controller overlay, and an art contest across five AI studios. Whether THIS
format earns its own scorecard is what season one will decide.*

---
*A fan-made naming convention. Not affiliated with, endorsed by, or containing any
assets of any monster-catching franchise you may be thinking of. All character naming is
homage; all machinery is original; the cat is legally just a cat who talks.*
