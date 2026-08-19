# TRADECRAFT — CONDITION-ACTION CHEAT SHEET (Phase 0)

**Source:** Course syllabus (expert-sourced schema) — 14-week tradecraft outline **Domain structure:** Ill-structured → rules are conditional selectors, not procedures. Each rule tells you _which pillar/mode to invoke_, not _how to execute it_. Execution fluency comes later via drills/simulations per the Knowledge Type principle. **Format:** `IF (condition/cue) → THEN (mode to invoke) — because (why)`

---

## PILLAR 1 — INFORMATION RECONNAISSANCE

_(Wk 4, 5, 9-offensive)_

| #   | IF (cue/condition)                                                                  | THEN (invoke)                                                                                                                               | Because                                                                              |
| --- | ----------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------ |
| 1.1 | You need info on a target with no direct contact                                    | Passive OSINT before any active method                                                                                                      | Passive collection carries near-zero exposure risk; always exhaust it first          |
| 1.2 | Standard search yields nothing useful                                               | Escalate to advanced search operators / dorking                                                                                             | Surface web indexing is incomplete; structured queries surface grey literature       |
| 1.3 | You have an image/photo of interest                                                 | Run reverse-image + EXIF/visual-clue check                                                                                                  | Verifies authenticity and can geolocate/timestamp without contacting anyone          |
| 1.4 | Target has multiple online aliases                                                  | Pivot on username/handle across platforms                                                                                                   | Persona reuse is the most common OPSEC failure — links otherwise-separate identities |
| 1.5 | You need physical/spatial context on a location                                     | Shift to GEOINT tools (satellite/mapping)                                                                                                   | Physical layout informs both recon and later physical tradecraft (Wk 12)             |
| 1.6 | Individual OSINT points don't cohere into a picture                                 | Apply mosaic theory — aggregate low-sensitivity fragments                                                                                   | Individually harmless data points can triangulate into sensitive conclusions         |
| 1.7 | You're about to cross into scraping/contacting/private data                         | STOP — check legal/ethical bound (ToS, GDPR) before proceeding                                                                              | Recon legality is jurisdiction- and platform-dependent, not assumed                  |
| 1.8 | If you need to expand a target's digital footprint from one information to another. | Username pivoting, email-based pivoting, reverse image search, directory mapping, searching, metadata extraction, GEOINT, and link charting | Because one information is not enough, you have to expand from it.<br><br>           |

---

## PILLAR 2 — INFORMATION PROTECTION

_(Wk 2, 8, 9-defensive, 12-exchange)_

|#|IF (cue/condition)|THEN (invoke)|Because|
|---|---|---|---|
|2.1|Starting any operation/persona|Run the 5-step OPSEC process (critical info → threat → vuln → risk → countermeasure) before acting|Reactive protection is always weaker than a planned baseline|
|2.2|Unsure what counts as sensitive|Ask "if aggregated with X, does this expose me?"|Mosaic theory applies to your own footprint just as much as a target's|
|2.3|Need to communicate sensitively|Choose channel by threat model, not convenience (Signal/PGP/out-of-band)|Different tools trade off metadata exposure vs. usability vs. forward secrecy differently|
|2.4|Verifying a contact's identity/key|Use out-of-band verification|In-band verification can be intercepted/spoofed by the same channel being verified|
|2.5|Noticing repeated contact-pattern anomalies (same accounts, timing)|Treat as possible surveillance/metadata exposure, not coincidence|Metadata analysis (who-contacts-whom) is often more revealing than content|
|2.6|Physically exchanging something sensitive|Apply meeting OPSEC (pre-arranged signals, route checks) before physical exchange methods|Physical exchange inherits digital OPSEC failure modes plus new physical-detection risk|
|2.7|Suspect you're being followed/tracked (digital or physical)|Run a detection route / check for technical anomalies before continuing normal behavior|Confirming surveillance changes the correct next action entirely|

---

## PILLAR 3 — INFORMATION CONSTRUCTION

_(Wk 3, 10)_

|#|IF (cue/condition)|THEN (invoke)|Because|
|---|---|---|---|
|3.1|Need to operate without linking to real identity|Build a persona proportional to the task's risk (not max-effort by default)|Over-engineered cover for a low-risk task wastes resources and adds inconsistency surface|
|3.2|Persona will be used more than once|Backstop it (consistent history, artifacts, timezone/typing patterns) before deployment|Legends fail at the seams — inconsistency, not lack of detail, is what gets caught|
|3.3|Choosing cover type|Match cover-for-status vs cover-for-action to what's actually being concealed|Wrong cover type leaves the _real_ vulnerability unprotected even if the persona looks solid|
|3.4|Persona/legend under scrutiny (Wk 11-style)|Check digital-physical consistency first (fingerprints, timezone, metadata)|These are the highest-yield discriminators for detecting fabrication|
|3.5|Long-running operation|Periodically audit persona for drift from baseline|Legends decay over time as the same "author" makes small inconsistent choices|

---

## PILLAR 4 — INFORMATION MANIPULATION

_(Wk 6, 7, 13-offensive)_

|#|IF (cue/condition)|THEN (invoke)|Because|
|---|---|---|---|
|4.1|Need info a target won't give directly|Use elicitation (flattery/feigned ignorance/bracketing), not direct questioning|Direct questions trigger conscious guardedness; indirect methods bypass it|
|4.2|Choosing an influence lever|Match Cialdini principle (authority/reciprocity/liking/etc.) to target's likely motivator|Wrong lever for the person's psychology reduces success and raises suspicion|
|4.3|Engaging virtually (LinkedIn/forums) vs. in person|Adapt classical HUMINT technique to platform norms, don't port it 1:1|Digital elicitation lacks tone/body-language cues; over-aggressive asks stand out more online|
|4.4|Distinguishing a manipulation attempt aimed at you|Slow down and check for pretexting/urgency/authority-pressure patterns|Social engineering relies on speed and emotional pressure to bypass scrutiny|
|4.5|Content (image/audio/video) seems too convenient or too clean|Treat as possible synthetic media until checked|AI-generated deception (Wk 13) is now a live category, not just human pretexting|

---

## CROSS-CUTTING LENSES — apply to _every_ pillar decision

|#|IF (cue/condition)|THEN (invoke)|Because|
|---|---|---|---|
|X.1|You default to a classical/physical technique|Ask what the digital-era equivalent is (and vice versa)|The syllabus's core throughline is classical↔digital translation (KGB Line X ↔ APTs, dead drop ↔ USB/BLE)|
|X.2|AI tool is available for a recon/manipulation task|Evaluate it as dual-use: does it help you, or could an adversary use the same class of tool against you?|Wk 13 frames AI as force-multiplier _and_ threat simultaneously, not sequentially|
|X.3|Any action feels effective but you haven't checked its legality|Stop and check jurisdiction/ToS/consent before executing|Legal/ethical bound is a hard constraint across all 4 pillars, not a pillar-specific concern|

---

## USAGE NOTE (per Type of Knowledge principle)

This table is a **conditional scaffold**, not a fluency tool. Per the repo's own failure-mode table: memorizing this without running it against cases will produce _rigid declarative knowledge_, not conditional wisdom. Use it during Phase 1 case work by asking, before each case: _"Which row applies, and why did I pick that row over the adjacent one?"_ — the discrimination between adjacent rules is where the real learning happens, not the rules themselves.