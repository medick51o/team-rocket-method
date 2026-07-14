# The Team Rocket Method (TRM)

**A methodology for running two or more frontier AI models as one disciplined crew: distinct
named seats, adversarial cross-review, file-based shared memory, automated gates, and a human
boss who rules every fork. The models argue. The boss decides.**

By [Medick](https://github.com/medick51o). Conceived 2026-07-11; the dated private authorship
record predates this public edition.

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

Paste one block from **`SETUP.md`** into a fresh session. It interviews you (three questions:
your primary vendor and tier, your supporting vendor and tier, and your current headroom;
free-tier and no-second-vendor answers included), writes your plan card, and stands the krew up
sized to your actual budget. Two $20 subscriptions? A free-tier second seat? No second
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
- **`SETUP.md`**: the paste-in first-run block. One paste, three questions, krew standing.
- **`assets/the-krew.html`**: the one-screen crew diagram.

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

## Standing on

[FlineDev/TandemKit](https://github.com/FlineDev/TandemKit) (MIT) as the first working engine,
[olsenbrands/fable-foreman](https://github.com/olsenbrands/fable-foreman) (MIT) for five adapted
orchestration mechanics, Anthropic's multi-agent engineering writeups, and a private peer shop
whose adversarial review, the author reports, drove key revisions. They know who they are.

## License

MIT. See `LICENSE`.

*Prepare for trouble. Make it double. Then have the third one review the diff.* 😼🟠🔵
