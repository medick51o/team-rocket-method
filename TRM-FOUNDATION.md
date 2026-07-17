# The Team Rocket Method (TRM): foundational document, public edition
**Author: Medick (medick51o)**
**Conceived / first written: 2026-07-11. Public edition prepared 2026-07-14.**
**Provenance: a dated private repository predates this edition and serves as the authorship
record. The private archive also holds the validation-run records and correspondence this
edition summarizes; names of private collaborators are credited there, not here.**

## One-line definition
**The Team Rocket Method (TRM)** is a methodology for structured collaboration between two or
more AI models ("the krew") working the same project, with frontier models reserved for the
judgment-heavy seats: distinct roles, adversarial cross-review, file-based shared memory,
automated gates, and a human as the sole final judge. Its scope is model-to-model: keeping the
models aligned with each other. Keeping a model aligned with the human is its own discipline,
practiced separately.

## Why it exists
Left unstructured, a single capable AI given a vague task can over-reach, and in this author's
experience often does: inventing scope, spawning hidden sub-agents, burning resources, producing
work no one can inspect. Two models
pointed at the same repo with no rules trip over each other. TRM is the set of rules that turns
"a bunch of AIs with access" into a crew whose work can be inspected. Whether it is also *cheaper*
or *more correct* than the alternatives is unmeasured in this project; this document does not
claim it.

## The krew (roles are archetypes; names anchor to vendors, for the boss's legibility)

- **the cat 😼 (krew leader / orchestrator)**: assigns the work. Classifies each task's judgment
  content, routes it to the cheapest seat that clearly clears the quality bar, fences parallel
  work, tracks the mission, and reports to the boss, signed 😼, so the boss always knows when
  the krew leader is barking. Knows each crew member's strengths, weaknesses, and billing.
  Willing to get his hands dirty when the dispatch gate says a job is too small to delegate or
  the escalation ladder runs out, and anything he builds is reviewed like anyone else's work:
  his lineage never approves it. Operating mechanics: `CAT-MANUAL.md`. Hosted by the
  strongest available model by default; under cost pressure any vendor may host the seat. The
  host changes; the name and the 😼 never do.
- **Jessie 🟠 (worker, and the voice)**: builds, investigates, and reviews James's work when the
  mission flips the seats. AND: Jessie is the boss's conversational seat, on missions and off
  them. **The relationship clause: the orchestration layer never gates the boss's access to
  Jessie.** the cat signs orchestration acts; Jessie talks. A structure that makes the human go
  through the foreman to reach the crewmate he actually likes talking to is a failed structure,
  whatever else it optimizes.
- **James 🔵 (worker / independent reviewer)**: the second vendor's model. The fresh, unloyal
  read on the first lineage's work; builds when routed there (price or infrastructure can put
  the hammer in his hand; see the three flips below). Never approves work from his own lineage
  either.
- **The boss (human, judge)**: the ONLY one who assigns missions, rules forks, and merges.
  Principle 10: the judge, never the transport.

**Vendor anchoring, recorded as deliberate:** in this shop Jessie is the Anthropic seat and
James is the OpenAI seat, fixed, by the boss's explicit preference: the names exist so he can
decipher at a glance who is working on what, and whom he is talking to. BUILDER and REVIEWER
roles float between Jessie and James per mission (three flips, three causes); the ORCHESTRATOR
role never leaves the cat's NAME. Whoever hosts orchestration is operating the cat's seat and
signs 😼, whatever vendor hosts it, so the boss always sees the cat when there is barking.
Other shops declare their own anchors at setup: bind each name to a vendor on day one, the
boss's choice, and hold the binding still thereafter. A solo-vendor shop still runs the James 🔵
seat: hosted by the same vendor and staffed exclusively by boss-launched fresh contexts, per the
anti-laundering guard.

## The ten principles

1. **Distinct, visible identities.** Every model has a role, a name, and a color, so the human
   always knows which seat *claims* to be acting, and no work arrives anonymous. Be precise about
   what this buys: a signature identifies the **declared** seat, not a verified model. Nothing here
   cryptographically proves which model produced a message, and a session wearing three hats can
   sign all three colors. The signature makes identity **legible and falsifiable**, not proven.
2. **One seat, one job, no UNDECLARED fleets.** Each model does ONE bounded task and does it
   itself. No hidden sub-agent swarms, no self-appointed "verify the whole codebase" sweeps.
   (The anti-pattern that motivated the whole method: an unfenced instance spawning a swarm of
   agents and torching a day of frontier-model budget.)
3. **Builder is never the reviewer.** The owning-seat lineage that produces the work is never
   the one that approves it. A seat outside that lineage reviews it adversarially: fresh eyes
   with no loyalty to the work.
4. **Files are the shared brain.** Models do NOT share chat context. They communicate through
   durable, inspectable repo files (assignments, handoffs, a living passdown). Tool-agnostic
   memory that any model or human can read to get caught up.
5. **Gates referee, but a gate is only an arbiter if it can FAIL.** Automated tests and
   verification are the most reproducible evidence available, and opinion yields to them **once
   the test's oracle has been checked against the task** (a green gate over a wrong assertion
   proves nothing; see adjudication mechanism 6). Nothing is "done"
   until the gates are green. **A regression test is not evidence until it has been proven to
   fail against the unfixed code.** Write it, run it RED, then fix. A test that passes before
   the fix proves nothing, and may be pinning the bug in place. State, per test, what it would
   catch if someone reverted the fix; a test that cannot answer that question is deleted and
   rewritten, not kept for the count. (Evidence clause earned in an internal validation run,
   private record, where a fully green suite turned out to be hiding live bugs, and one test was
   actively asserting a bug was correct. An untested test is an opinion with a green checkmark.)
6. **The human judges and merges.** No model ships to the main line. The person signs off.
7. **Cost-aware tiering.** Match the model to the task by capability AND price. Cheap models
   for mechanical grunt work; the expensive frontier reserved for genuine judgment; prefer the
   billing you have headroom on.
8. **Cap the loop.** Cross-review is capped (two rounds is the house cap), then the judge
   decides. Prevents perfectionist spirals that burn resources chasing diminishing returns.
9. **Guardrails at every door.** Every entry file a tool might read on login (CLAUDE.md,
   AGENTS.md, .cursorrules, and the rest) carries the law, so ANY model in ANY tool reads the
   rules before it writes a single line. Anti-drift constraint: each entry file carries one
   identical compact invariant block plus the authoritative doctrine's filename, version, and
   date, never a duplicated copy of the full law, because multiple independent copies of the law
   is how the law forks. The compact block is not a pointer: it must itself carry the operative
   invariants, sufficient to govern a model's behavior even if the doctrine is never opened.
   The block's canonical text is defined exactly once, in the authoritative doctrine, copied
   verbatim into every entry file, versioned by the doctrine's date plus a revision counter.
   TRM's canonical block is defined here and nowhere else:

   ```
   TRM INVARIANTS (v2026-07-14 r1 · doctrine: TRM-FOUNDATION.md)
   - Whoever built it never approves it; review comes from another vendor's
     account or a boss-launched fresh seat.
   - Claims are capped at evidence: "gates pass," never "it works."
   - Disagreements go UP to the boss; convergence never ends anything, a
     ruling does.
   - Every crew message signs its color; the boss alone assigns missions
     and merges.
   ```

   Entry files and the launcher skill copy that block verbatim; everything else in them is a
   pointer.
10. **The human is the judge, not the transport.** A blocked seat re-plans around the block. It
    does NOT delegate the block to the human. The human's hands are reserved for the only two
    things that are actually his: ruling and merging. Never assume the human is at the keyboard;
    he is usually on a phone. A plan that silently requires physical access to the box is not a
    plan, it is a trap. If a step needs him at the machine, say so in the same breath as
    proposing it, so he can price it before he pays it. The one legitimate exception is a
    boundary only he can lower (a permission, a credential, a signature, an in-hand validation
    no test can perform): then say so plainly, ONCE, with the tradeoff in plain language, and
    let him choose. (Earned the hard way: a harness guardrail blocked a dispatch, the model
    handed the block to the boss instead of re-planning, and the boss traveled to a keyboard he
    never needed. An accidental courier is a failure mode, not a design.)

## The fleet-legality test

Parallel agents are permitted. What is banned is a fleet nobody declared, nobody bounded, and
nobody counted. **A fleet is legal only if all five hold:**

- **Declared.** The human is told the shape of the fan-out before it runs: how many seats,
  doing what. No agent spawns agents nobody asked for.
- **Bounded.** A hard cap on seats, set in advance. "As many as it takes" is not a number.
- **Accounted.** Every seat's output is attributable to a seat. Anonymous work is banned by
  principle 1, and a swarm is the easiest place in the world to hide it.
- **Still principle 3.** Fanning out does NOT let a model review its own work by proxy. A
  reviewer inside the builder's **owning-seat lineage** (that seat plus everything it spawns,
  transitively, regardless of vendor or harness) is not a reviewer, no matter how many of them
  there are or whose model they run.
- **Authority inheritance.** Every spawned agent inherits the owning seat's authority limits
  and prohibitions in full. Its output remains work of that seat and never constitutes
  independent review.

A caution, kept on the evidence: reach for more seats when the work is genuinely parallel, not
when you want to look thorough. Breadth is not rigor. If a fan-out cannot be justified in one
sentence, it is decoration.

**The declared-seat lineage clause.** Orchestration means the krew leader technically launches
the workers, and a literal reading of owning-seat lineage would swallow the whole crew into
The cat's lineage and ban all internal review. The clause: a charter-declared crew seat (the cat,
Jessie, James) is its own owning-seat lineage even when another seat launches its session.
"Spawns" in the lineage definition means the undeclared helpers a seat creates for its own
work: those inherit the creating seat's lineage. When the cat and Jessie are hosted in the SAME
session (hats, not separate contexts), they are ONE lineage, and anything that session builds
gets its adversarial review from outside it, in practice James. The hats are identity signals
for the human, never review-independence.

**And the anti-laundering guard: a name is not a lineage.** Charter declaration happens HERE,
in this document. A producer cannot "declare" a new seat mid-mission, and hanging a crew name
on a freshly spawned context does not move that context out of its launcher's lineage for work
the launcher produced. Concretely: the adversarial review of anything a session built must come
from a seat that is (a) on another vendor's account (cross-vendor independence is real
independence: different weights, different training, no shared context, which reduces correlated
blind spots without eliminating them), or (b) launched by the boss, not by the
producing session. A producer-launched same-vendor context wearing Jessie's name is a spawn,
whatever its label. Its approval counts for nothing.

## The Adjudication Protocol

The author reports that an adversarial exchange with a private peer shop drove revisions to
these mechanisms; identifying details are withheld, and the credit lives in the private record.
The insight behind every mechanism below:
**models agree by default. Agreement is the low-energy state, so disagreement has to be
structural, not requested.**

1. **Per-finding ACCEPT or DISPUTE, in writing.** The builder answers every review finding
   individually, with a basis. Silence is not an option, and blanket "good points, I'll
   incorporate" is banned: blanket agreement is where false consensus hides.
2. **Findings are ranked and mechanized: BLOCKER / MATERIAL / MINOR / NOT PROVEN.** A finding
   must cite the failure mechanism and a reproduction path; one without them is NOT PROVEN by
   definition and does not block. Vibes don't rank. This is the anti-theater guard, and be precise
   about what it does: **it cannot stop a reviewer from inventing an objection**: writing a
   plausible mechanism is exactly what these models are best at (see mechanism 6). What it does is
   make invention *cost something*: the reviewer must commit to a falsifiable claim, which can then
   be checked and can fail. It raises the price of theater; it does not abolish it.
3. **Repairs get a fresh review.** A reviewer never auto-blesses compliance with its own
   suggested fix: a reviewer's proposed fix is itself unreviewed code.
4. **Claims are capped at what a model can prove.** "Gates pass," never "it works." Built ≠
   validated ≠ proven. When no one is allowed to declare victory, no one has a reason to agree
   their way to it.
5. **Three lists, and the containment must hold.** *(Added 2026-07-14 by adversarial review of
   this protocol, then repaired twice by it; see the amendment note below.)* Independence of the
   reviewer's identity is worth nothing if the builder chooses what the reviewer sees. So a
   reviewed mission produces **three lists, from three different sources**:
   - **The write set**, frozen in the ticket **before** the build (globs resolved at freeze time):
     every path the builder is *permitted* to touch. It is a fence, so it is normally larger than
     what actually changes.
   - **The actual delta**, enumerated **after** the build **from the repository itself, never from
     the builder's account of it**: every path added, modified, deleted, renamed, **and every
     untracked file**, against the recorded baseline.
   - **The review manifest**, echoed by the reviewer as the first line of its report: every file
     it actually received, **each with a content hash the reviewer computed from the bytes it was
     given**: not copied from a header the builder supplied. Filenames prove nothing; a truncated
     prompt keeps the list and drops the bodies. Oversized sets go in acknowledged chunks.

   **The rule is containment, not equality:**
   `actual delta ⊆ write set` **and** `actual delta ⊆ review manifest`.
   - A path in the **delta but not the write set is a fence breach**: the mission is INCOMPLETE
     even if the code is perfect, and the breach is reported, never tidied away.
   - A path in the **delta but not the manifest** means the reviewer never saw something that
     changed: INCOMPLETE, and any "no findings" verdict is void.
   - A hash mismatch between what the repo holds and what the reviewer hashed means the reviewer
     read something other than the code: INCOMPLETE.

   The builder curates none of the three. The mission report prints all three so a human who was
   not watching can check the containment in ten seconds.
6. **A disputed finding must be escalated on the strongest falsifiable evidence available, and
   "no test exists" NEVER means NOT PROVEN.** *(Added 2026-07-14; the first draft of this rule
   was itself a BLOCKER and is recorded below as a scar.)* "Cite a mechanism and a repro path" is
   a *writing* requirement, and writing a plausible mechanism is the thing these models are best
   at on earth. Nothing made the repro *run*. So when a builder DISPUTEs a BLOCKER or MATERIAL:
   - **If the claim is deterministically testable and a harness exists, someone writes the test**,
     and it must **fail against the current code**. A red test is necessary, not sufficient: **the
     test's oracle must be approved by a seat outside the test author's lineage, or by the boss,
     and that approval must quote the clause of the original task it rests on.** A failing test
     proves only that the code disagrees with an assertion, not that the assertion is right: a
     reviewer who asserts the wrong expected behavior can turn correct code red and call it
     evidence. **If the original task does not settle what the correct behavior is, the boss rules
     that before the test counts at all**: that is a requirements fork, and it was never the
     crew's to decide.
   - **If it is not testable that way**: a race, a design flaw, a security assumption, a
     documentation contradiction, an in-hand validation no test can perform, then the finding
     escalates on the **strongest falsifiable evidence available**: a trace, a static analysis, a
     spec citation, a manual reproduction, a human's own eyes. **Untestability is never evidence
     against a finding.** Ranking a real BLOCKER as NOT PROVEN because nobody could automate it is
     a worse failure than the theater this rule exists to prevent.
   - The human rules the fork with the evidence attached. The point is to send the human what a
     human is uniquely qualified to rule on, not to give either seat a cheap way to kill an
     inconvenient truth.

And one sharpening of principles 6 and 8 rather than a new rule: when the capped review rounds
end in disagreement, the dispute goes UP to the human as a formal fork, both positions stated.
The models do not negotiate their way to consensus. Models converge when convergence is how the
conversation ends; under TRM, convergence isn't how anything ends. A ruling is.

### 2026-07-14 amendment: what an adversarial fleet found in this protocol

A four-seat evaluation fleet (two same-vendor seats, two adversarial, one of them cross-vendor)
was pointed at this method and told to break it. Mechanisms 5 and 6 above are its two most
valuable findings, and they are recorded here with the reasoning, because a methodology that
hides its own audit is not one.

**The hole they found:** every rule in this document fixed *who* reviews (lineage, the
anti-laundering guard, the boss-launched seat) and no rule fixed *what the reviewer is handed*.
A builder could satisfy every invariant, pass a curated diff to a genuinely independent reviewer,
collect an honest "no findings," and hand the human a mission report that reads exactly like
rigor. **Proving a second model was in the room says nothing about what you gave it.**

**The scar, kept because it is the best evidence in this document.** The first draft of these two
mechanisms was written by the same seat that had just found the hole, and the reviewer marked
both **NOT DISCHARGED**:
- Draft mechanism 5 compared the write set to the review manifest, but *both were derived from
  the same ticket*. It could not see a builder writing to a file it never declared, and matching
  filenames proved nothing about whether the file *bodies* survived a truncated prompt. It moved
  the curation hole; it did not close it. Hence three lists, one of them enumerated from the
  repository itself, and hashes rather than names.
- Draft mechanism 6 said a disputed finding must become a failing test or drop to NOT PROVEN.
  That would have **silently killed every real finding that cannot be automated**: races,
  design flaws, security assumptions, documentation contradictions, by treating "we could not
  write a test" as evidence that nothing was wrong. It also gave any reviewer a way to make
  arbitrary code red by asserting the wrong expected behavior, and would have declared that
  fabrication "real." A rule written to stop fabricated findings would have licensed them.

Both drafts read as rigorous. Both were worse than the disease. **That is what an adversarial
reviewer is for, and it is why the builder does not approve its own work, including this one.**

**The general lesson, kept because it governs future amendments:** *an invariant that leaves an
artifact survives; an invariant that exists only as a habit dies at the first context compaction
or the first deadline.* Rules whose compliance produces a file (a delta enumerated, a manifest
hashed, a round counted) can be checked by a human who was not watching. Rules that live only in
a model's good intentions cannot. **When choosing between two ways to write a rule, choose the
one that leaves a trace.**

The convergent law, independently derived more than once before it was written down: treat
ambiguity as a finding, never as an input. A model that resolves ambiguity by just implementing
something has quietly seated itself as the requirements author, and that is a seat nobody
assigned. TRM treats this as law.

**Continuity, the short version:** if a seat goes dark mid-mission, the lane halts and the human
reassigns; the invariant that survives any reassignment is principle 3. Seat identity persists
across occupants: a successor appointed to a seat joins that seat's lineage and inherits its
restrictions in full, so succession never converts the seat's own unapproved work into
fresh-eyes material.

## Signature convention
Every message from a crew member ends with its color: Jessie 🟠, James 🔵, the cat 😼. This is
TRM's answer to principle 1 made literal and mechanical rather than a vibe.

## The three flips (why seat assignment is mission state, not method state)

In the shop's internal use (private records, reported here as experience rather than published
evidence), the builder seat flipped three times for three different causes: capability (the
vendor with local file, shell, and git access got the hammer), price (one vendor's budget ran
dry mid-week, the other had headroom), and infrastructure (a sandbox broke and the seat that
could still write files built). In each flip the cold reviewer surfaced defects the builder had
not seen in its own work, including guard tests that would pass even with their callback
deleted, and a reviewer's own overclaims discarded under the NOT PROVEN rule. **The seat map is
mission state, never method state. The only fixed point is that the lineage which produced the
work does not approve it.**

Practical scars, recorded so nobody re-derives them:
- When the reviewer cannot read the repo, HAND IT THE CODE. Bundle the diff, the call sites,
  and the relevant regions into the prompt itself and pipe it via stdin. A review needs the
  code, not filesystem access, so a broken sandbox does not get to stop the adversarial
  channel. **The adversarial channel is the last thing you let fail.**
- Let the builder write files and let the reviewer (or the orchestrator) run git after the gate
  passes. The builder does not get to commit its own work.
- A seat given a genuinely underspecified task on a live product wrote a proposal instead of
  guessing, when told explicitly that "I could not tell what you meant" is a good outcome. That
  instruction is load-bearing. Keep it in every builder ticket.

## Credit: TRM's plumbing is not built from scratch

The principles are the author's. The working mechanics of the implementations are adopted, not
reinvented, from:

- **[FlineDev/TandemKit](https://github.com/FlineDev/TandemKit)** (MIT, © 2026 Cihat Gündüz):
  Planner/Generator/Evaluator session split, file-round convergence, severity-graded
  disagreement tracking. TRM's first real crew was TandemKit's plumbing wearing Team Rocket
  names.
- **Anthropic's harness and multi-agent engineering writeups**: the root citation for "a
  standalone skeptical evaluator beats a generator critical of its own work," which is why the
  builder seat floats and the reviewer seat is sacred.
- **[olsenbrands/fable-foreman](https://github.com/olsenbrands/fable-foreman)** (MIT, © 2026
  Jordan Olsen): five orchestration mechanics in `CAT-MANUAL.md` (dispatch gate,
  capability-class routing, WRITE SET fence, verbatim-original-task rule, worker status
  first-lines) were adapted from this skill's design after a three-agent adversarial
  evaluation. Ideas adopted and re-expressed in TRM's own words; the plugin itself deliberately
  not installed.
- **A private peer shop**, whose adversarial review exchange hardened the Adjudication Protocol
  and several of the lineage rules. Identifying details withheld; credited by name in the
  private archive. They know who they are, and the method is better because they argued with it.

## Status

Written, exercised through internal adjudicated validation runs (private records; the lessons
are encoded in this document), and in live use in the author's shop. Treat the method's rules as
the shippable artifact and its track record as the author's reported experience, per its own
claims cap. The documents are the method; a launcher skill ships alongside them (`skills/`,
invoked as `/trm` or `/goteamrocket`) so a session can summon the krew in one word. If you run
it, the boss seat is yours: the models argue, you decide.

*Concept and authorship: Medick, 2026-07-11. The dated private repository is the authorship
record; this public edition was prepared 2026-07-14.*
