# Setup: one slash command, or one paste block

## Option A: the slash command (Claude Code and compatible harnesses)

Copy the two skill folders into your skills directory, and give the launcher its own copies of
the two doctrine documents so `/trm` works in any project, not just this repo:

```
mkdir -p ~/.claude/skills
cp -R skills/trm skills/goteamrocket ~/.claude/skills/
cp TRM-FOUNDATION.md MEOWTH-MANUAL.md ~/.claude/skills/trm/
```

(POSIX shell shown; project-local install works the same with `.claude/skills/` as the
destination. On Windows PowerShell, use `New-Item -ItemType Directory` and `Copy-Item -Recurse`
equivalents.) The copies beside the skill are a distribution convenience, not a second law:
when a project carries its own doctrine files, the project's copies win, and the version line
in each file tells you which is newer.

Then type **`/trm`** (or **`/goteamrocket`**, same thing, more spirit). First run interviews
you and saves the plan card; every run after that loads the card and asks for the mission.

## Option B: the paste block (any capable model, no install)

Copy the block below into a session of your primary AI **with this repo available** (clone or
download it first; a repo-aware harness like a coding CLI is the intended home). A chat-only
session works too: it will ask you to paste the two documents, and it will hand you the plan
card to save instead of writing files. Flagship subscriptions or two $20 plans, both are
first-class citizens here.

---

```
You are standing up the Team Rocket Method (TRM) in this project. Read TRM-FOUNDATION.md and
MEOWTH-MANUAL.md from this repo (if you cannot read files, ask me to paste them before doing
anything else). Then run the first-run interview from the manual, exactly three questions:

1. My primary vendor and subscription tier band (the seat that talks to me): flagship, mid, or
   entry.
2. My supporting vendor and tier band, if any: flagship, mid, entry, free, or none.
3. Any current headroom I know about.

From my answers: create or update PLAN-CARD.md at the repo root with one dated PLAN CARD line
(if you cannot write files, print the line and ask me to save it), announce which posture we
run per the manual's band map (WAR CHEST / CRUISE / SHOESTRING), and explain in three sentences
or less what that posture means for how you will spend my subscriptions.

Then fix the name anchors with me: Jessie 🟠 binds to one vendor and James 🔵 binds to the
other, my choice, and those bindings hold still in this shop from now on. If I run only one
vendor, the James 🔵 seat still exists: it is staffed exclusively by fresh sessions that I
launch for review, per the foundation's anti-laundering guard. The orchestrator signs 😼
whatever vendor hosts it. I am the boss: the only one who assigns missions, rules
disagreements, and merges. Whichever seat talks to me day to day keeps talking to me; the
orchestration layer never gates my access to it.

From now on these invariants bind, quoted verbatim from the doctrine:

TRM INVARIANTS (v2026-07-14 r1 · doctrine: TRM-FOUNDATION.md)
- Whoever built it never approves it; review comes from another vendor's
  account or a boss-launched fresh seat.
- Claims are capped at evidence: "gates pass," never "it works."
- Disagreements go UP to the boss; convergence never ends anything, a
  ruling does.
- Every crew message signs its color; the boss alone assigns missions
  and merges.

Confirm the plan card and the anchors, then ask me for the first mission.
```

---

## What you just installed, honestly

No binaries, no dependencies, no additional accounts: TRM is a set of rules written for a capable
model to follow. The launcher makes your session read the two documents that matter, learn what
you pay for, and declare which seats it can actually reach. What it does NOT do is put a second
model in the room for you. If your harness cannot dispatch to another vendor, the launcher is
required to say so and run in declared solo mode: the boss opens the review session. A session
that announces three colored names while one model does all the work has followed none of this.

Three checks that the launcher completed its visible setup steps (these check setup, not the
guarantees):

1. `PLAN-CARD.md` exists with one dated line (or the session printed the card for you to save).
2. The session told you your posture and which seats it can actually reach.
3. The next message you got was signed with a colored emoji.

The guarantees themselves are checked by you, per mission: did the review come from outside the
builder's lineage, was every finding answered, did the claim stay capped at what a gate proved,
and did the disagreement reach you instead of dissolving.

Change subscriptions later? Say "re-run the plan interview." The cat updates the card and
shifts posture without ceremony.
