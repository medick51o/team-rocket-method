<!-- Contributing to TRM means running TRM. See CONTRIBUTING.md. -->

## Class

- [ ] **AMENDMENT** (changes `TRM-FOUNDATION.md`, the law)
- [ ] **MECHANIC** (manual, skills, setup, readme, assets, templates)

## If AMENDMENT: file it as a finding

**Rank:** BLOCKER / MATERIAL / MINOR / NOT PROVEN
*(Vibes don't rank, and that rule binds the doctrine too. But rank by the severity you can
demonstrate. A real defect that resists automation (a race, a design flaw, two readers resolving
an ambiguity differently) still ranks by its evidence. **NOT PROVEN is for when the evidence is
genuinely insufficient, not for when the bug is merely hard to test.** "I couldn't write a repro"
is never evidence that nothing is wrong.)*

**Failure mechanism** (what concretely goes wrong under the CURRENT law, for whom, when):

**Reproduction path, or the strongest falsifiable evidence you have:**

## What changed

## Review independence (required, per principle 3, which applies to its own author)

- [ ] This change was reviewed by a seat **outside my lineage**.
      Reviewer seat (vendor/account, or "boss-launched fresh session"): `______________`
      Reviewer's report (paste or link): `______________`

## The three lists (adjudication mechanism 5)

**Write set**: what I was permitted to touch, declared *before* I started (globs resolved):

```
```

**Actual delta**: what actually changed, read from the repo and not from memory.
**Both commands, because `git diff` alone cannot see a file you never added:**

```
git diff --name-status <baseline>     # added / modified / deleted / renamed
git status --porcelain                # untracked files, which the line above will miss
```

```
```

**Review manifest**: what the reviewer echoed back. **Each entry needs a state and a hash the
reviewer computed from the bytes it actually received** (a filename list proves nothing: a
truncated prompt keeps the names and drops the bodies). Deleted paths carry the baseline hash and
a DELETED marker; a rename is a DELETED old path plus a PRESENT new one.

```
PRESENT  src/auth.py      sha256:....
DELETED  src/obsolete.py  sha256:.... (baseline)
```

- [ ] **Containment holds.** This is the check, not "the lists match": a permission fence is
      *supposed* to be bigger than the change.
      - `actual delta ⊆ write set`: I touched nothing I was not permitted to touch.
      - `actual delta ⊆ review manifest`: the reviewer saw everything that changed.
      - Every hash the reviewer computed matches the repo's after-state (or the baseline, for
        deletions).

*If a containment fails, **say so here rather than fixing the paperwork.** A fence breach reported
is a finding; a fence breach quietly tidied is a lie.*

## If this touches the canonical invariant block

- [ ] Revision bumped (`r1` → `r2`)
- [ ] `CHANGELOG.md` entry added
- [ ] Block re-synced **verbatim** in every place it appears, in this PR

## Claims cap

State what you can prove, not what you hope. "Gates pass," never "it works."
