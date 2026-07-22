# MIGRATION MAP — every source section, and where it landed

Purpose: a section-by-section trace of the 6 source files into the new split, so the cat and the
boss can verify **nothing was lost.** Destinations: **SPINE** (engine) · **CREW** (TRM crew) ·
**SHOW** (TRTO show) · a **SKILL** file · **DROPPED-AS-DUP** (a duplicate now single-sourced) ·
**DEFERRED** (in the synthesis BUILD ORDER but explicitly Phase-5/"later", not this build).

**Rule applied throughout:** one owner per fact. When a source section carried both a *mechanic* and
a *character/flavor* telling, the mechanic went to SPINE and the flavor to CREW/SHOW, each
cross-referencing, never restating. "cat" was rephrased to "the orchestrator" wherever it moved to
SPINE (a required character-free edit; substance preserved).

---

## SOURCE 1 — `team-rocket-takes-over/SKILL.md` (the monolith: engine + show in one file)

| Source section | Landed in | Note |
|---|---|---|
| Frontmatter / title / invoke | `trto-SKILL.md` | frontmatter preserved; body becomes a thin loader |
| WHAT THIS IS (the honest pitch) | **SHOW** → Premise | verbatim framing preserved |
| Relationship to TRM: a BRANCH | **SHOW** → Premise + `trto-SKILL.md` DEPENDS | "loads TRM first" is now versioned dep-loading |
| THE MENTOR TRUTH | **SHOW** → Deep Mentoring (scenes) **+** **CREW** → §2 Lean Mentor Mandate | split by dose: CREW = the one-line aside; SHOW = the dramatized scene |
| THE CASTING LAW (character table) | **CREW** → §1 | the cast + role→SPINE-role binding |
| MODEL BANNERS (wardrobes) | **CREW** → §1 (wardrobe/color lore) **+** **SPINE** → Appendix A (plain vendor→color map) | SPINE owns the plain map; CREW owns "orange IS Claude's banner / red rivals blue" lore |
| THE SCREEN-TIME RULES | **SHOW** → Screen-Time Casting | who *fronts* on screen; explicitly never touches SPINE routing |
| THE CHEMISTRY | **SHOW** → Chemistry | jealousy/crush/#1-girl |
| THE AMBIGUITY LAWS | **SHOW** → Ambiguity Laws | the never-resolving arcs |
| THE WOBBUFFET CLAUSE | **SHOW** → Wobbuffet Clause | the mascot rules |
| — the Puppeteer Rule (inside Wobbuffet) | **SHOW** → Prime Law seam #1 | ELEVATED to a firewall seam per spec |
| — the Transparency Rule (inside Wobbuffet) | **SHOW** → Prime Law seam #3 | ELEVATED to a firewall seam per spec |
| THE WORKFLOW — twin lanes & the bench | **CREW** → §3 | who performs SPINE's dispatch/fence |
| — RIGHT-SIZE THE DISPATCH (boss ruling 07-18) | **SPINE** → Doctrine 5 | engine; CREW obeys, does not restate |
| THE RED-VS-PINK LAW | **CREW** → §4 (rivalry ethic) **+** **SPINE** → Part VII (mechanics) | mechanics (checkpoint/severity/one-exchange/brake) → SPINE; the rivalry casting → CREW |
| AUTONOMOUS HOURS (anti-token-inferno) | **SPINE** → Part VII (token-discipline core) **+** **CREW** → §5 (sub-agent naming) | the bell/cutoff/batching/pivot → SPINE; canon sub-agent names → CREW |
| THE SHIP PIPELINE (5 gates) | **SPINE** → Doctrine 1 | relocated near-verbatim (boss-tuned 07-21) |
| INSTRUMENT, DON'T GUESS | **SPINE** → Doctrine 2 + Part I §3 (the fork's bug side) | |
| HONEST DEFERRALS + SELF-VERIFYING | **SPINE** → Doctrine 3 + Part I §4 (Reality Contract terms 2 & 4) | |
| THE SCALPEL IS A FEATURE | **SPINE** → Doctrine 4 | relocated near-verbatim |
| WIRING NOTES (grok/agy paths, Overflow Valve) | **SPINE** → Appendix A | flagged "current wiring, not law" |
| THE VIBE (the ten laws) | **SHOW** → Vibe-as-delivery | law 8 REWRITTEN whip-crack→right-size-first (per spec) |
| Missions run as EPISODES (cold open/montage/victory) | **SHOW** → Cold Opens & Victory Frames **+** **CREW** → §6 (unit) | theater → SHOW; bounded-unit → CREW |
| THE EPISODE DOCTRINE (anti-slop) | **CREW** → §6 **+** **SHOW** → engagement loop | structure → CREW; the watchable+interactive loop → SHOW |
| THE LINEAGE LEDGER | **SPINE** → Doctrine 6 (engine) **+** **SHOW** → firewall (Facts≠Flavor narration) | logging rule → SPINE; "act is never data" → SHOW |
| THE WEEKLY LINEAGE REVIEW | **SPINE** → Doctrine 6 | the recalibration loop = engine |
| On invocation | `trto-SKILL.md` → On invocation | |

## SOURCE 2 — `trm/TRM-FOUNDATION.md`

| Source section | Landed in | Note |
|---|---|---|
| Header / author / provenance / private-archive | **CREW** → §7 Provenance & Credit | TRM brand identity, not brand-neutral engine |
| One-line definition | **CREW** → §7 **+** **SPINE** → intro ("what this engine is", brand-neutral) | brand line → CREW; generic engine line → SPINE |
| Why it exists | **CREW** → §7 | |
| The krew (roles as archetypes) | **CREW** → §1 (cast) **+** **SPINE** → Part III (abstract roles) | archetypes → SPINE; names bound → CREW |
| — the relationship clause (never gate Jessie) | **CREW** → §1 | a real structural rule, TRM-owned |
| The ten principles | **SPINE** → Part III | verbatim substance |
| The fleet-legality test (5 prongs) | **SPINE** → Part IV | |
| declared-seat-lineage clause + anti-laundering guard | **SPINE** → Part IV | phrased "charter-declared seat"; CREW binds the names |
| The Adjudication Protocol (6 mechanisms) | **SPINE** → Part V | relocated faithfully |
| 2026-07-14 amendment (what the fleet found) | **SPINE** → Part V (amendment scar) | the "best evidence in the doc" — kept |
| Signature convention | **SPINE** → Part VIII (the *mechanic*) **+** **CREW** → §1 (the *colors*) | |
| The three flips | **SPINE** → Part VI (three flips) | |
| Credit (TandemKit / fable-foreman / Anthropic / peer shop) | **CREW** → §7 | method provenance = TRM identity |
| Status | **CREW** → §7 | |

## SOURCE 3 — `trm/CAT-MANUAL.md`  *(NB: synthesis said "folds into SHOW" — CORRECTED to SPINE; see judgment calls)*

| Source section | Landed in | Note |
|---|---|---|
| Who the cat is | **CREW** → §1 (the Cat character) **+** **SPINE** → Part VI (orchestrator mechanics) | |
| The dispatch gate | **SPINE** → Part I §2 (Gate-0) + Part VI | |
| Routing: capability classes | **SPINE** → Part VI | |
| First-run setup: the 3-question interview | **SPINE** → Part VI **+** `trm-SKILL.md` step 2 | mechanic in SPINE; the launcher runs it |
| Tier bands & posture map | **SPINE** → Part VI | band/posture tables **plus the posture SPEND table** (what each posture DOES over the five levers — who hosts FRONTIER · down-tier pressure · fan-out allowance · which vendor builds) restored to **full operational density** in the Gate-3 fix pass (BL1). *(v1.0 draft dropped the spend table — that "substance kept" claim was false; corrected.)* |
| When support is thin / missing | **SPINE** → Part VI | the **ENTRY / MINIMAL / NONE thin-support rules** (who-reviews-what, free tier on riskiest + boss-launched for the rest, solo = all boss-launched) restored in full (BL1); the "solo review is weaker" honesty kept |
| When primary is ENTRY | **SPINE** → Part VI | the **ENTRY-primary rules** restored in full (BL1): small/single-sliced, fan-outs off by default, tighten the gate, slice/draft/stop when no seat clears the bar (incl. the "$40 shop runs it in the small" paragraph) |
| The five levers | **SPINE** → Part VI | kept incl. N/A-preflight and "card is an input not a lever" (each posture now defined SOLELY as choices over these five, BL1) |
| What the cat CANNOT do | **SPINE** → Part VI (honesty limits + currency rule) | anti-costume honesty kept plainly; the **currency rule** (never state quota/price/tier access or model availability from memory; boss-declared vs harness-reported vs explicit-error vs "felt weak"=noise) and the **headroom rule** restored in full (BL1) |
| The routing ledger | **SPINE** → Part VI | "honesty aid, not proof" kept; the **no-causation / no-counterfactual paragraph** ("one mission's ledger can't show what the other posture would have done; we have never run that comparison") restored in the fix pass (BL1) |
| The plan card & budget postures | **SPINE** → Part VI | |
| Tickets (dispatch contract) | **SPINE** → Part VI | incl. the load-bearing "propose, don't guess" line |
| The WRITE SET fence | **SPINE** → Part VI | |
| Worker statuses | **SPINE** → Part VI | |
| Escalation | **SPINE** → Part VI | |
| Review dispatch (4-thing ticket, three lists, disputed findings) | **SPINE** → Part V + Part VI | |
| Mission reports | **SPINE** → Part VI | signed-😼 becomes signed-by-orchestrator; CREW/SHOW re-add the 😼 |
| What the cat never does | **SPINE** → Parts III/VI (the rules) **+** **CREW** → §1 ("never gate Jessie") | |

## SOURCE 4 — `trm/SKILL.md`

| Source section | Landed in | Note |
|---|---|---|
| Launcher steps (find law / plan card / declare reachable / report) | `trm-SKILL.md` | rewritten to load SPINE+CREW, print load receipt, verify versioned deps |
| The invariant block | **SPINE** → Part VIII (canonical) + copied verbatim into all 3 SKILLs | doctrine filename updated TRM-FOUNDATION.md → SPINE.md |

## SOURCE 5 — `dispatch/SKILL.md`

| Source section | Landed in | Note |
|---|---|---|
| Frontmatter / intro (powerhouse w/o persona) | `dispatch-SKILL.md` | thin loader now |
| NARRATE IN COLOR (🟡 gold) | `dispatch-SKILL.md` (the tier's delta) **+** **SPINE** → Appendix A (vendor→color) | plain rendering is the Deck's only method-delta |
| First: know the arsenal | **SPINE** → Appendix A | shared by all tiers now |
| Quick map (who-to-send-where) | **SPINE** → Part VI *Review dispatch* (the brand-neutral **review-by-fit** RULE + the two legal paths, M2) **+** Appendix A (arsenal) **+** `dispatch-SKILL.md` step 4 | the fit-routing RULE now lives in SPINE so all tiers inherit it; the Deck keeps only a labeled this-shop illustration (Gate-3 fix pass) |
| The arsenal is OPTIONAL | **SPINE** → Appendix A | |
| The method (6 steps, "TRM's spine stripped of the show") | **SPINE** (Parts I/V/VI) **+** `dispatch-SKILL.md` render checklist | the steps ARE spine; the SKILL now points at it |
| Non-negotiables | `dispatch-SKILL.md` guardrail card (all inherited from SPINE) | |
| On invocation | `dispatch-SKILL.md` → On invocation | arsenal probe kept |
| Setup / onboarding → `SETUP.md` | **NOT carried into the staged family** (map line corrected, M5) | the staged Deck has **no** `SETUP.md` pointer, and no `SETUP.md` file exists in the source skill dir either (the live Deck references it but it is absent). Onboarding/reachability is now owned by **SPINE Part VI's reachability & effective-model preflight** (M3) + the Deck's arsenal probe. The old "still referenced" claim was false. |
| Inherit the learnings → `FIELD-NOTES.md` | **SPINE** → Appendix B (see Source 6) | field notes now shared by all tiers |

## SOURCE 6 — `dispatch/FIELD-NOTES.md`

| Source section | Landed in | Note |
|---|---|---|
| 2026-07-20 CNC verify-run notes (all bullets) | **SPINE** → Appendix B (append-only) | now truly intact — the exact model strings (`"Claude Sonnet 4.6 (Thinking)"` / `"Claude Opus 4.6 (Thinking)"`), the physics-attack/Flash-ceiling context, and the specific killed-advice examples (mill-first/burn-second; interpolate-from-3-probes) were **restored in the Gate-3 fix pass** (the v1.0 draft had summarized them; the "intact" claim now holds) |

---

## DEFERRED (in the synthesis, explicitly Phase-5 "later" — NOT built in this pass, by design)
Per the synthesis BUILD ORDER step 5 ("(Later) the tier-shift clause + the episode state file") and
the team-lead's 6-file spec, these were intentionally left out of this build. Flagging so they read
as *deferred*, not *lost*:
- **THE TIER-SHIFT CLAUSE** (Jessie's "the tiers are a dial, not 3 walled products" — promote
  Deck→TRM→TRTO on the same spine for free). The split built here is exactly what MAKES it free; the
  clause that NAMES the move is a clean follow-up once the split is blessed.
- **THE EPISODE STATE FILE** (`.trm-state.json` — active lanes / pending verdicts / ledger tasks /
  current episode). TRTO-owned, TRM-optional.

## POST-BUILD ADDITION — CREW v1.0 → v1.1 (PORTABLE CASTING, 2026-07-21)
After the v1.0 split, the boss ruled the crew must fit ANY downloader's arsenal, not just our
Claude+Codex+Grok+Gemini shop. A 4/4-unanimous council (`docs/TRM-PORTABLE-CASTING-SYNTHESIS.md`)
refined **CREW §1 (Casting Law) + §8 (onboarding)** ONLY: the seat column became a *suggested* default
remapped per shop via a first-run **cast-map** step; added the lead-by-lineage lore line, the
brain-not-CLI rule, the three-arsenal walk, and the loud degrade flags. SPINE, SHOW, the fresh-context
reviewer, and the 3-question interview were **untouched** (the cast-map is CREW's; SPINE owns only the
arsenal detection it reads from). Load receipts bumped `TRM v1.0 → v1.1` across CREW / SHOW / both SKILLs.

## POST-BUILD CORRECTION — Gate-3 bench fix pass (2026-07-21)
A 3-vendor Gate-3 bench (⚫ Grok · 🟢 Gemini · 🩷 Cassidy/Codex) REJECTed the v1.0 split; the cat
accepted the findings and Jessie 🟠 ran the fix pass. This map is regenerated against the corrected
files. What moved or was restored, beyond the rows above:
- **BL1 — plan-aware OPERATING policy restored into SPINE Part VI** at full operational density: the
  posture SPEND table, the ENTRY/MINIMAL/NONE thin-support rules, the ENTRY-primary rules, the
  headroom rule, the currency rule, and the ledger no-causation paragraph (the v1.0 draft had
  compressed these to labels — the reason the bench rejected).
- **M3 — new SPINE Part VI section "Reachability & effective-model preflight"** (declaration ≠
  detection; independence compares effective model + lineage, never CLI/host/billing/banner; unknown
  fails closed to `UNKNOWN LINEAGE` / `REVIEW UNAVAILABLE`). All three launchers + CREW §8 point here;
  the old false pointers to "SPINE Part IV" for reachability were corrected (M5).
- **M2 — brand-neutral review-by-fit RULE moved into SPINE Part VI Review dispatch;** the Deck's
  vendor-specific ladder demoted to a labeled Appendix-A illustration.
- **BL2/BL3 — CREW §3 reduced to casting-only**, review pairing expressed as a preference under
  SPINE's two legal paths (no absolute "different vendor" fork).
- **BL4 — SHOW screen-time firewall seam closed** (real cast-map seat signs every verdict in its true
  lineage; fronting is puppeteered narration only).
- **BL5 — both launchers reordered** so the READY receipt prints LAST, after reachability is known.
- **M6 — SHOW's ten vibe laws rewritten** as presentation-only constraints.
- **Minors restored** to SPINE: Part VII circle-back bullet; Part VIII invariant-block-id continuity
  note; Appendix B exact FIELD-NOTES strings + examples.
- **Version floors:** trm/trto/SHOW now DEPEND on `CREW >= 1.1`; receipts interpolate parsed versions.
- **The canonical invariant block was NOT touched** (verified byte-identical across SPINE + 3 launchers).

## NOTHING DROPPED
No source section was dropped as unrecoverable. The only "DROPPED-AS-DUP" moves are the intended
de-duplications: the method text that the *old* TRTO monolith and the *old* Deck each carried
separately is now single-sourced in SPINE, and the SKILLs point at it instead of re-stating it. That
de-duplication IS the refactor.
