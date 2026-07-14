# The Team Rocket Method (TRM)

**A governance protocol for running two or more AI models as one disciplined crew: distinct
named seats, adversarial cross-review, file-based shared memory, automated gates, and a human
boss who rules every fork. The models argue. The boss decides.**

By [Medick](https://github.com/medick51o). Conceived 2026-07-11; the dated private authorship
record predates this public edition.

> **What this is, stated honestly.** TRM is a set of rules, not software. It has no enforcement
> beyond a capable model choosing to follow prose and a human choosing to hold the line. It does
> not by itself put a second model in the room: a single session can wear all three names and
> fool nobody but its boss. What the rules are designed to buy you is governance the harness
> does not give you: review that cannot launder itself through your own subagents, fan-outs
> that must be declared before they run, claims that stay capped at evidence, and a human who
> stays the judge. The track record behind them is the author's reported experience, not
> published evidence. Read `TRM-FOUNDATION.md` and decide for yourself.

## The krew

| Seat | Who | Job |
|---|---|---|
| **The Boss** 👑 | you, the human | assigns missions, rules every fork, the only one who merges |
| **Meowth** 😼 | krew leader (hosted by your strongest model) | routes each task to the cheapest seat that clears the quality bar, fences parallel work, reports missions, gets his hands dirty only when it calls for it |
| **Jessie** 🟠 | worker, and the voice | builds, investigates, reviews; also the boss's conversational seat, never gated behind the orchestrator |
| **James** 🔵 | worker, independent reviewer | the fresh, unloyal read on the other lineage's work; builds when routed |

Names anchor to vendors so the boss always knows who is talking. Roles float per mission: in
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
top of them.** Native agent teams and subagents are transport and concurrency: they dispatch
work, run seats in parallel, and hand context around. They do not tell you whether the seat that
approved a change was the same lineage that wrote it, whether a fan-out was ever declared,
whether a claim was capped at what a gate actually proved, or who ruled the disagreement. TRM is
the governance layer over whatever transport you already have. Its distinctive load-bearing
pieces, in the author's assessment: the **owning-seat lineage** rule and its anti-laundering
guard (which closes the "my own subagent reviewed me" loophole most team features ignore),
per-finding ACCEPT/DISPUTE with mechanism-or-it-is-NOT-PROVEN, red-before-green evidence, and
the human as the only terminus of a disagreement. The names and the colors are legibility, not
rigor. No comparative benchmark against native teams exists yet; when one does, it will be
published here whichever way it falls.

## Standing on

[FlineDev/TandemKit](https://github.com/FlineDev/TandemKit) (MIT) as the first working engine,
[olsenbrands/fable-foreman](https://github.com/olsenbrands/fable-foreman) (MIT) for five adapted
orchestration mechanics, Anthropic's multi-agent engineering writeups, and a private peer shop
whose adversarial review, the author reports, drove key revisions. They know who they are.

## License

MIT. See `LICENSE`.

*Prepare for trouble. Make it double. Then have the third one review the diff.* 😼🟠🔵
