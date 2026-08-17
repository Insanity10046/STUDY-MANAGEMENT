# STUDY-MANAGEMENT
![icon](https://github.com/Insanity10046/STUDY-MANAGEMENT/blob/main/icon.webp)
> A repository that treats **studying as a system to be engineered**, not a habit to be improvised.

This repo separates *what you use to study* (tools, methods, resources) from *how you actually run your studying* (rules, mechanisms, workflow). That split — **Study Stack vs. Study System** — is the core idea the whole repo is built around, and it maps almost one-to-one onto how you'd design any system: components at the bottom, governance rules in the middle, orchestrated processes running on top.

---

## 1. The Core Distinction

| | **Study Stack** | **Study System** |
|---|---|---|
| What it is | Your collection of tools/techniques | How you actually run your studying |
| Focus | Components | Process, sequence, rules, feedback |
| Example | Anki, Notion, Pomodoro, active recall | Plan in Notion → Anki reviews → 2 Pomodoros → practice problems → weekly review |
| Nature | Static, like an inventory | Dynamic, like a routine or workflow |
| Goal | Gives you capabilities | Produces consistent results |

**Analogy:** a stack is gym equipment + exercises you know. A system is your actual training plan — which exercises, on which days, in what order, with what progression. A stack alone doesn't guarantee results; the system is what makes the stack work.

---

## 2. Repository Structure

```
STUDY-MANAGEMENT/
├── STACK/                  # The component layer — raw capabilities
│   ├── README.md           # Defines what a "study stack" is
│   ├── TACTICS/            # Small, situational moves within a session
│   ├── TECHNIQUES/         # Specific applied methods for a purpose
│   └── METHODS/            # Full end-to-end learning approaches
│
├── SYSTEM/                 # The process layer — governance and mechanisms
│   ├── README.md           # Defines what a "study system" is
│   ├── PRINCIPLE/          # The cognitive-science rules that justify design choices
│   ├── PROTOCOLS/          # Pre-packaged emergency/specialized procedures
│   └── FRAMEWORKS/         # Meta-systems for managing skills/levels over time
│
└── TEMPLATES/              # The instantiation layer — blueprints to fill in
    ├── SYSTEM_DOMAIN.md    # Detailed, domain-specific system template
    └── SYSTEM_DOMAIN2.md   # Minimal, general-purpose system template
```

### TEMPLATES/ — instantiation
| File | Role |
|---|---|
| `SYSTEM_DOMAIN2.md` | **General-purpose template.** Minimal skeleton: Stack → Rules → Processes → Workflow. |
| `SYSTEM_DOMAIN.md` | **Domain-specific template.** Adds domain architecture, method configuration, and a procedure matrix on top of the general skeleton. |

---

## 3. The "How": Building Your Own Study System

The repo's templates are really a **layered system architecture applied to learning**. If you think in system design terms, each template layer corresponds to a familiar architectural layer:

| System design layer | Study system equivalent | Template section |
|---|---|---|
| Infrastructure / component layer | Study Stack | `1. STUDY STACK` |
| Business logic / governance layer | System Rules | `2. SYSTEM RULES` |
| Service layer (composed functions) | System Processes | `3. SYSTEM PROCESSES` |
| Orchestration / runtime loop | Workflow / Session Cycle | `4. WORKFLOW` |

This is deliberate. A study stack with no rules is just an inventory (components with no wiring). Rules with no processes are unenforced policy. Processes with no workflow never actually run. You need all four layers, in order, for the system to be real — the same reason a codebase needs libraries *and* business rules *and* services *and* a runtime loop before it does anything useful.

### Step-by-step: instantiating `SYSTEM_DOMAIN2.md`

**Step 1 — Define the Stack (component inventory)**
List, honestly, what you actually have access to and use — not an aspirational list. Three columns only: Tools, Methods, Resources. This is your dependency list. Keep it small; unused dependencies (apps you downloaded and never open) are dead weight, exactly like unused packages in a codebase.

**Step 2 — Write System Rules (the governance layer)**
Rules are constraints that make the stack behave consistently. In this repo they're sourced from `SYSTEM/PRINCIPLE/`:
- **Domain Structure Rule** ← `Levels Of Structure In Domains.md`
- **Knowledge Type Rule** ← `Type Of Knowledge.md`
- **Analogical Rule** ← `Analogical Learning.md`
- **Feedback Rule** ← `Feedback Loop.md`
- **Sequence Rule** — your own ordering constraint

A rule is only useful if it's falsifiable — "match technique to knowledge type" is checkable each session; "study smart" is not. Treat each rule the way you'd treat a validation constraint in a schema: it should be possible to point at a session and say whether the rule was followed.

**Step 3 — Define System Processes (the service layer)**
Each row here is a *function*: it consumes specific stack components and rules, and produces a specific output. This is where composability matters — reuse the same stack components across multiple mechanisms rather than inventing new tools per mechanism, the same way you'd reuse a shared library across services instead of duplicating logic.

```
Mechanism             Stack Used            Output
------------------------------------------------------------
Domain Mapping     →  Tools + Resources   →  Domain map
Case Exploration   →  Tools + Methods     →  Case notes
Cross-Case Compare →  Methods + Resources →  Analogical schemas
Feedback Calib.    →  Methods + Feedback  →  Error log
Synthesis          →  Tools + Methods     →  Integrated knowledge
```

**Step 4 — Define the Workflow (the orchestration loop)**
Pre-session → Active session → Post-session → Next session. This is the runtime loop that actually invokes the processes according to the rules, every cycle, without you having to re-decide the architecture each time you sit down. A system you have to redesign every session isn't a system — it's still improvisation.

### Going deeper: `SYSTEM_DOMAIN.md` (domain-specific instantiation)

Once the general skeleton works, `SYSTEM_DOMAIN.md` adds three things a mature system design needs that a minimal skeleton doesn't:

1. **Domain Architecture** — a config block that classifies the domain itself (structure level, dominant knowledge type, feedback delay, primary cognitive risk). This is the equivalent of specifying your system's non-functional requirements before choosing an architecture — you don't pick a caching strategy before knowing your read/write ratio, and you shouldn't pick a study method before knowing whether the domain is well- or ill-structured.
2. **Method Configuration** — the explicit ordering contract (`Component Order`) that the Procedure Matrix must satisfy. This is your interface contract: the steps below must run in this sequence, on these inputs.
3. **Procedure Matrix** — the concrete implementation, where each abstract mechanism from `SYSTEM_DOMAIN2.md` gets bound to an actual Tactic/Technique from `STACK/` (e.g., "Domain feedback → Debrief Session → Error log + delayed re-test"). This is dependency injection: the general system defines *what* needs to happen, the matrix wires in *which concrete stack component* does it.

### Worked example (Mathematics domain, abbreviated)

```
DOMAIN ARCHITECTURE
Domain Name:          Mathematics (Algebra)
Level of Structure:    Well-structured
Knowledge Dominant:    Procedural
Feedback Delay:        Immediate
Primary Cognitive Risk: Illusion of competence from pattern-matching without derivation

METHOD CONFIGURATION
Method Used:      Machine V2 Method
Components Used:  Schema Induction, Interleaved Retrieval, Feedback, Fading, Mastery Check
Component Order:  Induction → Interleave → Feedback → Fade → Mastery Check
Learning Focus:   Fluent procedural execution, not just recognizing the rule

PROCEDURE MATRIX (excerpt)
Step  Scope              Goal                Tactic              Technique
1     Whole domain       Map structure       Advance Forward     Concept map of operation types
2     Mixed problem set  Force discrimination Militarized Pomodoro Interleaved timed drills
3     Errors only        Calibrate judgment  Debrief Session     Error log + re-derivation
```

Notice the pattern: every row in the matrix is *traceable* back to a rule (why this step exists) and *composed* from stack components already defined (nothing invented ad hoc). That traceability is the whole point — if a session isn't working, you can find the broken layer instead of blaming "discipline."

---

## 4. Design Principles This Repo Follows

- **Separation of concerns** — stack (capability) is never mixed with system (process). You can swap Anki for Quizlet without touching a single rule.
- **Composability over duplication** — mechanisms are built by combining existing stack components, not by inventing a new tool per problem.
- **Domain-fit over one-size-fits-all** — `Levels Of Structure In Domains.md` and `Type Of Knowledge.md` exist specifically so the *same* template produces different concrete systems for algebra vs. law vs. tradecraft.
- **Tight feedback loops** — `Feedback Loop.md` treats error signal delay as a first-class design variable, the same way you'd treat latency in a system's critical path.
- **Explicit state, not implicit habit** — `Skillset Management System.md` models skills as a four-state machine (Active / Dormant-Warm / Dormant-Cold / Archived), so maintenance cost is a tracked variable instead of a vague worry.
- **Templates as contracts, not prose** — `SYSTEM_DOMAIN2.md` and `SYSTEM_DOMAIN.md` are fill-in-the-blank interfaces precisely so a new domain system can be stood up by instantiation, not by rewriting the architecture from scratch each time.

---

**Core Rule:**
The stack provides capability. The rules and mechanisms turn that capability into a system. The workflow keeps it running.
