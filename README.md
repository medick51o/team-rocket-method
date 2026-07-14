# The Team Rocket Method (TRM)

**A governance protocol for running two or more AI models as one disciplined crew: distinct
named seats, adversarial cross-review, file-based shared memory, automated gates, and a human
boss who rules every fork. The models argue. The boss decides.**

By [Medick](https://github.com/medick51o). Conceived 2026-07-11; the dated private authorship
record predates this public edition.

> **What this is, stated honestly.** TRM is a set of rules, not software. It has no enforcement
> beyond a capable model choosing to follow prose and a human choosing to hold the line. It does
> not by itself put a second model in the room: a single session can wear all three names and
> fool nobody but its boss. What the rules are designed to buy you is **governance you can
> audit**: a review laundered through your own subagents is declared invalid, fan-outs must be
> declared before they run, claims stay capped at evidence, and a human stays the judge. Your
> harness may already give you some of this; we have not surveyed them and we will not tell you
> what yours does. The track record behind these rules is the author's reported experience, not
> published evidence. Read `TRM-FOUNDATION.md` and decide for yourself.

## Read this before you decide we are selling you something

If you are a careful reader, or an AI your boss asked to vet this, **this section is for you, and
it is deliberately the first thing you hit.** We would rather lose you here than have you find it
out on page four and conclude we were hiding it.

We set out to build a serious method. **Then we pointed a four-seat adversarial fleet at our own
product and told it to break us**, and it did, repeatedly, including on things we had shipped an
hour earlier. Here is the audited scorecard. It is not marketing copy; it is the result.

### 🟢 Load-bearing (survived adversarial review; works today with no special tooling)

- **Whoever built it never approves it, and "your own subagent" doesn't count.** The
  owning-seat lineage rule and its anti-laundering guard make that check explicit, whether or not
  your harness already exposes it. Our own cross-vendor reviewer called this the strongest idea
  here. *(We have not audited every agent framework and make no claim about what "most" of them
  do. Point us at one that already enforces this and we will say so here.)*
- **Findings ranked with a mechanism and a repro, or they are NOT PROVEN and block nothing.**
  Anti-theater guard. It cannot *stop* a reviewer inventing objections (writing a plausible
  mechanism is what these models are best at); it makes invention falsifiable, and therefore
  costly. It raises the price of theater. It does not abolish it.
- **Every finding answered individually, ACCEPT or DISPUTE, in writing.** Blanket agreement is
  where false consensus hides.
- **Claims capped at evidence.** "Gates pass," never "it works." A test isn't evidence until it
  has been proven to fail against the unfixed code.
- **Disagreements end in a human ruling, not in consensus.** Models converge when convergence is
  how the conversation ends. Here it isn't.
- **Fan-outs must be declared, bounded, and counted before they run.** Spawning N seats
  multiplies tokens; not spawning them does not. That much is arithmetic. **How much a given
  posture actually saves you is unmeasured in this repo**, and we are not going to call it "the
  biggest saving available" until somebody counts.

### 🟡 Conditional (real only if your harness exposes the knob; N/A otherwise, and the cat must say so)

- **Model tier per task**, **reasoning effort per dispatch**, and **routing work to a second
  vendor's quota.** These are real levers *when your harness lets a dispatch choose them*. When it
  doesn't, they are N/A and a human pulls them. The manual runs a capability preflight and is
  required to report N/A rather than pretend.

### 🔴 Unproven (we believe it; this repo cannot show it)

- **That any of this saves money or improves outcomes.** There is no benchmark. Not against a
  single model, not against your harness's built-in agent teams, not between our own budget
  postures. **This repository contains zero measurements, and the author knows of no published
  benchmark of this method as of 2026-07-14.** (We can only speak for what we know; somebody else
  may have numbers we have never seen.) The routing ledger is the model's own report of its own
  behavior, which makes lying deliberate rather than lazy, and that is *not the same as proof*.
- **That the track record is anything but the author's word.** It is.

### ⚪ Decoration (fun, does no work, and we are not going to pretend otherwise)

- **The Pokémon names, the cat, the battle cry, and the posture titles.** `WAR CHEST` and
  `SHOESTRING` are labels on a routing policy, not machinery. **Strip the Pokémon out and the
  method is unchanged.** That is the test we ran, and it passes: the theme is a wrapper, not the
  product. Rename the seats after your dogs; nothing breaks.
- **One honest exception, because underselling is also a lie:** *that seats are visibly and stably
  identified at all* is load-bearing (it is principle 1). You need to see which seat *claims* to be
  talking and which one signed off, so that a lie has to be told on purpose. **Pokémon is
  decoration; the signature is not.** Be precise about what a signature buys, though: it names the
  **declared** seat, not a verified model. Nothing here proves cryptographically which model wrote
  a message, and one session wearing three hats can sign all three colors. It makes identity
  legible and falsifiable, not proven. Any stable naming scheme does that job. Ours just happens to
  be funnier.

### ⚫ Things we shipped that were wrong, and cut (kept here on purpose)

- We wrote a budget "lever" that told you to **review only the risky diffs at low budgets.** That
  is not a setting, that is instructions to stop running the method. Our own reviewer flagged it as
  a BLOCKER within the hour. Coverage is never negotiable; only intensity is.
- We wrote a rule that said an unprovable finding **drops to NOT PROVEN.** It would have silently
  killed every real defect nobody could automate: races, design flaws, security assumptions.
  Rewritten: *untestability is never evidence that nothing is wrong.*
- We told the orchestrator to **"verify your tier against your account."** It cannot. No such API
  exists. Cut.

**So: is it the next big thing, or is it a Pokémon-themed method?** Honestly? It is a **real
governance protocol with a fun coat of paint, whose economic claims are unproven and whose
enforcement is prose.** If that's not enough for you, that instinct is correct and it is the exact
instinct this method is built around. **Bring it as a finding** (`CONTRIBUTING.md`) and the
maintainer has to answer it in writing, individually, with a basis. That rule binds him too.

What we will not do is sell you a dropdown menu and call it an engine.

## The krew

| Seat | Who | Job |
|---|---|---|
| **The Boss** 👑 | you, the human | assigns missions, rules every fork, the only one who merges |
| **Meowth** 😼 | krew leader (hosted by your strongest model) | routes each task to the cheapest seat that clears the quality bar, fences parallel work, reports missions, gets his hands dirty only when it calls for it |
| **Jessie** 🟠 | worker, and the voice | builds, investigates, reviews; also the boss's conversational seat, never gated behind the orchestrator |
| **James** 🔵 | worker, independent reviewer | the fresh, unloyal read on the other lineage's work; builds when routed |

Names anchor to vendors so the boss can see at a glance which seat claims to be talking (a
signature declares a seat; it does not prove a model). Roles float per mission: in
the author's own use, capability, price, and infrastructure have each flipped the builder seat,
because the one fixed point is not the seating chart. It is that **whoever built it never
approves it.**

## Claude-first, by design

TRM's law is vendor-agnostic, but this method is written **Claude-first**: the reference shop
runs Claude Code (and Claude Desktop) as the harness, the strongest available Claude hosts
Meowth 😼, and Jessie 🟠 is the Claude seat. James 🔵 is whatever second vendor keeps the review
honest; the reference shop uses OpenAI's Codex CLI in that supporting role. If your stack is
Claude plus one other model, this maps onto it directly. If it isn't, the roles still work; only
the defaults change.

## Getting started

Two ways in, both in **`SETUP.md`**: install the launcher skill and type **`/trm`** (or
**`/goteamrocket`** when morale demands it), or paste one block into a fresh session. Either
way the cat interviews you (three questions: your primary vendor and tier, your supporting
vendor and tier, and your current headroom; free-tier and no-second-vendor answers included),
creates your plan card (saving it when it can write files, printing it for you to save when it
cannot), and stands the krew up sized to your actual budget. Two $20 subscriptions? A free-tier second seat? No second
vendor at all? All supported configurations, with honest notes on what each trades away. The
method is the rules, not the bill.

## What's in this repo

- **`TRM-FOUNDATION.md`**: the ten principles, the fleet-legality test, the Adjudication
  Protocol (ranked findings, per-finding ACCEPT/DISPUTE, repairs get fresh review, claims capped
  at evidence), and the lineage rules that keep review independence real even when one seat
  launches the others.
- **`MEOWTH-MANUAL.md`**: the krew leader's operating mechanics. The dispatch gate,
  capability-class routing (FRONTIER / WORKHORSE / FAST), tickets with write-set fences, worker
  status contracts, and the escalation ladder.
- **`SETUP.md`**: two doors in: the `/trm` launcher skill or the paste-in first-run block.
- **`skills/`**: the launcher (`/trm`) and its battle-cry alias (`/goteamrocket`).
- **`assets/the-krew.html`** and **`assets/postures.html`**: the one-screen crew diagram and
  the four-postures diagram.

## Tell the cat what you pay for

TRM's favorite party trick: **plan-aware routing.** You declare a plan card (which subscription
tier you run on each vendor, and how full the tanks are) and Meowth 😼 adjusts the whole crew's
spending posture: WAR CHEST, CRUISE, SHOESTRING, or LIMP HOME. Same mission, different budget,
different routing: top tiers get free-swinging frontier work and parallel fan-outs; two $20
subscriptions get a tight dispatch gate, builds routed to whichever window is freshest, and the
strongest seat showing up only where judgment actually lives. Downgrade your plans and the cat
downgrades his appetite, not your quality bar. Details in `MEOWTH-MANUAL.md`.

## What's deliberately NOT here

The method's rules were shaped by internal adjudicated validation runs and by an adversarial
exchange with a private peer shop. Those records contain private material and stay in the
private archive, so treat the track record as the author's reported experience rather than
published evidence (the method's own claims-cap rule demands that framing). The lessons those
records produced are all encoded in the two documents above, with credit given in the
foundation's Credit section.

## The ten principles, one breath each

Distinct visible identities (every message signed with its color) · one seat one job, no
undeclared fleets · builder is never the reviewer · files are the shared brain · gates referee,
and a gate is only an arbiter if it can fail · the human judges and merges · cost-aware tiering ·
cap the loop · guardrails at every door · the human is the judge, never the transport.

## Why not just use your harness's built-in agent teams?

The honest answer, since the method's own claims cap demands one: **you should, and TRM sits on
top of them.** Native agent teams and subagents give you transport and concurrency: they dispatch
work, run seats in parallel, and hand context around. TRM is a governance layer you run over
whatever transport you already have, and what it adds is a set of checks made **explicit and
auditable**: whether the seat that approved a change shared a lineage with the seat that wrote it,
whether a fan-out was declared before it ran, whether a claim stayed capped at what a gate
actually proved, and who ruled the disagreement.

**We have not audited the agent-framework landscape and we are not going to tell you what other
tools do or don't do.** Some harness may already enforce every one of these; if you know of one,
open an issue and we will say so right here. What we claim is narrower and checkable: **TRM
requires these checks and produces the artifacts that let you verify them**, whether or not your
harness does.

Its distinctive load-bearing pieces, in the author's assessment: the **owning-seat lineage** rule
and its anti-laundering guard, per-finding ACCEPT/DISPUTE with mechanism-or-it-is-NOT-PROVEN,
red-before-green evidence, and the human as the only terminus of a disagreement. The names and the
colors are legibility, not rigor. **No comparative benchmark against native teams exists in this
repo**; if one gets run, it gets published here whichever way it falls.

## Standing on

[FlineDev/TandemKit](https://github.com/FlineDev/TandemKit) (MIT) as the first working engine,
[olsenbrands/fable-foreman](https://github.com/olsenbrands/fable-foreman) (MIT) for five adapted
orchestration mechanics, Anthropic's multi-agent engineering writeups, and a private peer shop
whose adversarial review, the author reports, drove key revisions. They know who they are.

## Contributing: you have to run TRM to contribute to TRM

Proposals arrive as **findings** (ranked, with a failure mechanism and a repro; vibes don't rank,
and that rule binds the doctrine too). The maintainer answers **every finding individually**,
ACCEPT or DISPUTE, in writing. The loop is capped at two rounds, then the boss rules and merges.

And principle 3 applies to the person who wrote principle 3: **the maintainer does not merge his
own amendment without review from a seat outside his lineage.** That reviewing seat is one he is
structurally forbidden to fill, which is the honest reason to want contributors and not just a
polite one. Every PR ends in the same checks a mission does: *reviewed by a seat outside my
lineage*, and *the containment holds across the three lists*.

Field reports (including the ones where TRM embarrassed itself) are the only evidence channel this
method has. **A report is never rejected for its conclusion**, and the only edits ever made are
disclosed redactions for secrets, personal data, or safety. Substance is never softened. See
`CONTRIBUTING.md`.

## License

MIT. See `LICENSE`.

*Prepare for trouble. Make it double. Then have the third one review the diff.* 😼🟠🔵
