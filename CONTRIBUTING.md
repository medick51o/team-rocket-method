# Contributing to TRM

**Contributing to the Team Rocket Method requires running the Team Rocket Method.** That is not a
cute slogan; it is the whole design. A method that cannot survive its own protocol has no business
telling you to run it on your code.

So: proposals arrive as **findings**, findings carry a **mechanism and a repro**, the maintainer
answers **every one individually** in writing, review comes from **outside the author's lineage**,
and disagreements end in a **ruling**, not in a consensus nobody believes. Same law you would run
on a bug.

---

## Two classes of change

| Class | Touches | Bar |
|---|---|---|
| **AMENDMENT** | `TRM-FOUNDATION.md`, the law itself | High. Requires a mechanism and a repro (below). |
| **MECHANIC** | `CAT-MANUAL.md`, `skills/`, `SETUP.md`, `README.md`, `assets/`, templates | Normal. A clear reason and a working change. |

A typo fix is a MECHANIC. Adding a principle is an AMENDMENT. If you are unsure, open an issue and
ask; guessing wrong costs you a round.

## An amendment is filed as a finding, in the method's own vocabulary

Rank it **BLOCKER / MATERIAL / MINOR / NOT PROVEN**, and cite:

- **The failure mechanism.** What concretely goes wrong, for whom, when, under the *current* law.
- **The reproduction path.** A mission (yours or a constructed one) where following TRM as written
  produced a bad outcome. Not a hypothetical you find distasteful: a path someone can walk.

**Vibes don't rank, and the rule binds the doctrine too.** An amendment with no failure mechanism
is **NOT PROVEN: it blocks nothing, and it is still wanted.** File it, ranked NOT PROVEN, and say
what you have. This is not a brush-off; it is the same anti-theater guard that protects your code
from a reviewer inventing objections to look rigorous, pointed at the law for the same reason. (It
cannot *stop* invention: a plausible mechanism is cheap to write. It makes invention falsifiable,
and therefore costly.)

**"I couldn't write a repro" is never evidence that nothing is wrong.** Some real defects cannot
be automated: a race, a design flaw, a security assumption, two readers resolving an ambiguity
differently. Those escalate on the strongest evidence available, exactly as they would in a
mission. A Field Report is a *different* channel (what happened when you ran TRM on real work),
not a lesser one and not a place we send inconvenient findings to die.

The strongest possible amendment is: *"I ran TRM at posture X. Here is the mission. Here is where
the law told me to do the wrong thing. Here is the artifact."*

## What the maintainer owes you

- **A per-finding answer: ACCEPT or DISPUTE, in writing, with a basis.** Every finding, individually.
  Blanket "good points, I'll incorporate" is banned here exactly as it is banned in a build, and for
  the same reason: blanket agreement is where false consensus hides.
- **A capped loop.** Two rounds of review on a PR, then the maintainer rules and merges.
  Convergence never ends a thread here. A ruling does.
- **A reason, if you are refused.** A DISPUTE cites the law or the evidence it rests on. "No" without
  a basis is not a ruling, it is a mood.

## Review independence binds this repository

**The maintainer does not merge his own amendment without adversarial review from a seat outside
his lineage.** Principle 3 applies to the person who wrote principle 3. In practice:

- A contributor's amendment is reviewed by the maintainer's crew.
- **The maintainer's own amendments are reviewed from outside his lineage**, which under the
  foundation means a seat on a different effective-model vendor and lineage, or one the boss launched fresh. That is the
  floor, and it is what keeps the project honest before anyone else shows up. (No bootstrap
  deadlock: a solo maintainer can still ship, and the reviewer's report is attached to the PR so
  you can check the review actually happened and read what it said.)
- **A human contributor's review outranks a model's, and for amendments to the law it is
  preferred.** A model reviewing a document about how models should be reviewed shares the blind
  spots of the thing it is reviewing. This is the seat the maintainer most wants filled, and the
  one he benefits least from filling himself.

That is the deal on offer: not commit access as a favor, but the one seat where an outsider's
objection is worth structurally more than the author's own.

## Every PR ends in one checkbox

```
- [ ] Reviewed by a seat outside my lineage.
      Reviewer seat (vendor/account, or "boss-launched fresh session"): ______________
      Reviewer's report (paste or link): ______________
- [ ] The three lists check out:
      write set (declared before I started): ______________
      actual delta (from the repo, not memory, including untracked files): ______________
      review manifest (what the reviewer echoed back): ______________
      Delta is a SUBSET of the write set, and the reviewer saw everything in the delta.
      If not, say so here rather than tidying it: a fence breach reported is a finding;
      a fence breach quietly fixed is a lie.
```

An unchecked box is not a rejection. It is an **INCOMPLETE**: the PR sits until the review happens,
because a change to a method about review independence, merged without review independence, would
be the funniest possible way to prove the method wrong.

## Field Reports: the only evidence channel this method has

TRM's track record is currently the author's reported experience, which by its own claims cap is
not published evidence. **Field reports are how that changes.**

Open an issue with the `field-report` template and tell us: what you ran TRM on, at what posture,
with what seats; what the adversarial review actually caught (or embarrassingly failed to catch);
what it cost; and what you would change.

**Negative results are wanted more than positive ones, and a report is never rejected for its
conclusion.** The only edits ever made to a field report are redactions for secrets, personal
data, or safety, and any redaction is disclosed in the published report and cleared with you
first where practical. Substance is never softened. A method that only collects testimonials from
people it worked for is a marketing funnel, not a method.

Especially wanted, and the hardest thing to get anywhere in this space: **what a posture actually
cost you versus running your primary seat solo.** The author has never measured it, and knows of
no published number.

Accepted field reports are collected in `FIELD-REPORTS.md`.

## Versioning the law

Any accepted change touching the canonical invariant block (`TRM-FOUNDATION.md`, principle 9):

1. Bumps the block's revision (`r1` → `r2`).
2. Adds a `CHANGELOG.md` entry.
3. **Re-syncs the block, verbatim, in every place it appears, in the same PR.** A stale copy of the
   block anywhere in the tree is a BLOCKER on its own PR. The law forks through copies; that is the
   entire reason principle 9 exists, and this project has already forked its own law once, which is
   recorded in the foundation rather than hidden.

## Who rules

The repository owner is the boss (principle 6, applied to itself): the only one who merges. The
models argue. Contributors argue. The boss decides, and says why.

😼🟠🔵
