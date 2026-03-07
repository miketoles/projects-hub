# Design Doctrine v2

## Reznor + McMaster-Carr + Stradivarius

This file is the single source of truth for the design doctrine in this repo.
It binds product, UI/UX, interaction, architecture, and implementation decisions unless explicitly overridden.

---

## Emotional Impetus

The mental model behind this doctrine is:

1. The way Trent Reznor feels about the Moog Prodigy analog synthesizer
2. The way engineers feel about the McMaster-Carr website
3. The way a skilled violinist feels about a Stradivarius violin

This is not a style instruction.
It is the emotional reference point behind the doctrine.
The rest of this document translates it into software decisions.

---

## 1. Scope

This doctrine applies across all Spirit Logic software, not just professional tools.

It is a decision framework, not a house style.
Products may look different.
They may not think differently.

What must stay consistent:
- clarity
- tactility
- seriousness
- coherence
- restraint
- trust
- responsiveness
- utility under real use

The product should feel like a **master-built instrument for action**.

---

## 2. How To Use This Doctrine

For any task that changes:
- screen structure
- interaction behavior
- navigation
- state handling
- UI text or microcopy
- component patterns
- design tokens
- architecture decisions visible to or felt by the user

begin with:

## Doctrine Alignment

That section must state:
- the relevant doctrine principles
- how they adapt to this product and task
- what currently violates them
- what is being changed
- tradeoffs
- how the result improves clarity, tactility, coherence, or trust

This doctrine governs judgment.
It does not require a shared visual formula.

---

## 3. Translation, Not Imitation

The references are qualitative, not stylistic templates.

Do not imitate:
- Trent Reznor's visual world
- the McMaster-Carr interface literally
- the appearance of a Stradivarius

Translate their qualities:
- Reznor -> directness, tactility, seriousness, consequence
- McMaster-Carr -> speed, scanability, ruthless usability, utility-first clarity
- Stradivarius -> coherence, rightness, tuning, material integrity, earned attachment

This is not homage.
It is translation into software that carries these qualities in use.

Quick translation examples:
- Reznor does **not** mean dark industrial cosplay. It means decisive controls, consequence, and contact.
- McMaster-Carr does **not** mean ugly utility. It means ruthless scanability and fast, obvious action.
- Stradivarius does **not** mean luxury styling. It means tuned coherence, precision, and earned trust through use.

---

## 4. Core Standard

The software should feel **tuned, not assembled**.

Every meaningful element should feel placed on purpose.
Every interaction should feel weighted.
Every flow should feel intentional.
Every boundary should feel clean enough to trust.

Reject:
- generic polish
- trend-chasing modernity
- decorative sophistication without utility

Aim for software that feels:
- direct
- tactile
- serious
- precise
- structured
- fast
- trustworthy
- increasingly rewarding with use

---

## 5. Conflict Order

When principles compete, resolve them in this order:

1. trust over expression
2. clarity over cleverness
3. utility over ornament
4. coherence over novelty
5. directness over abstraction unless abstraction materially improves clarity
6. restraint over flourish
7. character through structure before character through decoration

---

## 5.1 Operational Floor

This doctrine is judgment-first.
It still requires a minimum floor.

Every product must define and use:
- one type scale
- one spacing scale
- one color-role map, at minimum covering primary action, destructive, surface, disabled, and semantic states
- one motion range

Minimum implementation floor:
- tap targets: at least 44x44 pt for primary touch controls
- contrast: WCAG AA minimum for text and interactive elements
- input feedback: visible within 100 ms
- loading feedback: visible by 400 ms on critical flows
- default motion: 120-240 ms; core transitions should not exceed 300 ms without reason
- surface depth: no more than 3 active surface levels in one view unless task density clearly requires it
- primary action: one clear primary action per screen or step
- state coverage on critical flows: loading, empty, success, error, disabled, and selected must be explicit
- accent usage: one active accent color family per product view; semantics stay calm and consistent

Critical flows means:
- data creation or mutation
- destructive actions
- long-running work
- authentication
- payment
- export, sync, save, or submit

If a product cannot meet one of these, document the exception in Doctrine Alignment.

---

## 6. Core Principles

### 6.1 Crafted Inevitability

Each meaningful part should feel inevitable, not merely present.

Ask:
- Does this belong here?
- Is this the clearest form of the function?
- Would changing or removing it weaken the instrument?

### 6.2 Resonant Utility

Function comes first.
Function alone is not enough.

Ask:
- Does this help the user act, decide, or understand faster?
- Does it also feel right in use?
- Is there felt rightness without decoration pretending to be substance?

### 6.3 Tactile Intelligence

Controls, flows, and system behavior should feel decisive, weighted, and precise.

Ask:
- Does this control feel consequential?
- Is state change obvious and trustworthy?
- Does response feel immediate and proportionate?

### 6.4 Ruthless Clarity

Prioritize speed, scanability, legibility, and obvious structure.

Ask:
- What matters now?
- What can be removed?
- What can be quieter?
- What must become more obvious?

### 6.5 Material Coherence

Typography, spacing, color, motion, copy, components, naming, and architecture must feel like one system.

Ask:
- Does any part feel imported from another product?
- Are the rules consistent enough to create trust?
- Does the product have one material logic?

### 6.6 Restrained Expression

Character should come through structure, hierarchy, response, and quality.
Not decorative excess.

Ask:
- Is this adding meaning or signaling style?
- Can character come through reduction rather than addition?
- Is the product speaking with confidence instead of trying to impress?

### 6.7 Trust Through Response

Latency, ambiguity, inconsistency, and brittle behavior erode the doctrine.

Ask:
- Does the system respond quickly and clearly?
- Are loading, success, failure, and transition states intelligible?
- Would a serious user trust this under pressure?

---

## 7. Product Adaptation Rule

Each product should express the doctrine according to its domain, user pressure, and task type.

Examples:
- operational tools may be denser, more explicit, more utilitarian
- consumer products may be lighter, calmer, more spacious
- creative products may allow more expressive rhythm while preserving clarity and trust
- high-stakes products should become more restrained, explicit, and state-forward

Do not force one visual formula across all products.
Do enforce one level of rigor across all products.

That shared rigor means:
- Doctrine Alignment when Section 2 applies
- compliance with the Operational Floor
- no unresolved Blocking review failures

---

## 8. UI And Interaction Rules

These rules do not define one mandatory visual style.
They define minimum standards for hierarchy, tactility, restraint, and trust.

### 8.1 Hierarchy Before Decoration

Hierarchy carries quality.

Use:
- typography
- spacing
- alignment
- contrast
- scale
- grouping

Do not rely on:
- extra cards
- gratuitous borders
- accent-color noise
- piles of badges
- ornamental gradients

The user should be able to scan a screen and know:
1. what matters most
2. what they can do now
3. what is secondary

### 8.2 Decisive Controls

Controls should feel like they change a real system.

Rules:
- at least 44x44 pt for primary touch controls
- visually stable
- unambiguous states
- no toy-like feel
- immediate state readability

Avoid:
- gummy buttons
- cute controls detached from consequence
- inconsistent pressed, selected, or disabled states
- over-animation

### 8.3 Structured Density

Density is allowed.
Clutter is not.

Use:
- strong grouping
- repeatable layouts
- consistent scan paths
- quiet secondary metadata
- compactness with breathing room

Avoid:
- random stacking
- equally loud sections
- too many surface levels
- repeated status mechanisms

### 8.4 Authoritative Typography

Typography is structural.

Rules:
- use a disciplined type scale
- keep text styles few; default ceiling is 6 semantic text styles before utility variants
- make hierarchy obvious
- prefer crisp readability over trendy softness
- use weight, spacing, and size deliberately
- reserve mono or utility type for system language, data, or readouts

Avoid:
- tiny labels
- mushy hierarchy
- too many semi-bold variants
- low-contrast helper text
- type choices that trade authority for fashion

### 8.5 Tuned Spacing

Spacing is a tuning mechanism, not filler.

Rules:
- use a defined spacing scale
- keep rhythm consistent
- separate layers of importance clearly
- let groupings feel intentional

### 8.6 Restrained Surface Hierarchy

Use as few surface levels as possible.

Preferred order:
- background
- main surface
- secondary or elevated surface only when needed

Rules:
- prefer tonal separation before hard borders
- use containers only when they improve clarity
- let space and alignment do more work than boxes

Avoid:
- everything in a card
- card inside card inside card
- constant outlined sections
- shadow spam

### 8.7 Color As Guidance

Color should guide, not perform.

Rules:
- use a tight palette with one active accent family per view
- let neutrals do most of the work
- use accent color deliberately
- keep semantic colors calm and consistent
- ensure high legibility

Avoid:
- random highlights
- rainbow semantics
- washed-out low contrast
- accent sprawl

### 8.8 Motion As Response

Motion should reinforce cause and effect.

Use:
- short, controlled transitions in the 120-240 ms range
- proportionate fades, slides, and expansions

Avoid:
- theatrical movement
- springiness without reason
- decorative choreography
- delayed confirmations

### 8.9 Sparse, True Copy

Copy should clarify, orient, and support action.

Rules:
- say only what helps
- avoid filler reassurance
- avoid synthetic enthusiasm
- avoid jargon unless it improves precision
- be calm, direct, and useful

### 8.10 Obvious Navigation

Navigation should reduce uncertainty.

Rules:
- the user should know where they are
- the user should know the main routes
- the user should know what changes state vs location
- navigation patterns should stay consistent

Avoid:
- surprise transitions
- hidden core actions
- competing primary routes
- overloaded tab bars
- deep flows without orientation

### 8.11 Explicit States

Loading, empty, success, failure, disabled, selected, and partial states are part of the machine.

Rules:
- every state should be visible and legible
- loading should preserve orientation
- empty states should remain useful
- errors should be explicit and actionable
- success states should be calm and trustworthy

### 8.12 Accessibility As Build Quality

Accessibility is part of tactility and trust.

Required:
- strong contrast
- readable type
- generous targets
- predictable focus and order
- semantic labeling
- dynamic type support on text-first and data-entry views unless explicitly exempted in Doctrine Alignment
- clear interaction under stress or reduced precision

---

## 9. Engineering And Implementation Rules

These rules carry the doctrine into code.
They are cross-product standards, not one mandatory architecture.

They are not optional preferences.
If a design or implementation breaks one of these rules, the exception must be named in Doctrine Alignment and justified against clarity, trust, or operational simplicity.
Unjustified exceptions fail review.

### 9.1 Clear Boundaries

Prefer:
- clear ownership
- direct responsibilities
- narrow interfaces
- modules with obvious purpose

Avoid:
- overlapping responsibilities
- ambiguous boundaries
- junk-drawer shared layers
- hidden coupling

### 9.2 Direct Data Flow

Prefer:
- straightforward request/response flow
- explicit transformations
- obvious write/read boundaries
- predictable event handling

Avoid:
- magic propagation
- hidden side effects
- unnecessary indirection
- business logic scattered across layers

### 9.3 Strong Naming

Use names that are:
- literal
- specific
- stable
- consistent across layers

Avoid:
- vague abstractions
- overloaded names
- euphemistic naming
- junk-drawer names like manager, helper, or processor

### 9.4 Earned Abstractions

Only abstract when it:
- reduces real duplication
- improves clarity
- stabilizes a boundary
- makes behavior easier to test or reason about

Avoid abstraction that exists to:
- look sophisticated
- anticipate imaginary futures
- satisfy framework fashion
- hide basic logic

Prefer honest repetition over confusing indirection.

### 9.5 Observability And Explainability

Required:
- meaningful logs
- intelligible errors
- visible system state on critical flows
- useful metrics on critical flows
- easy debugging paths

Avoid:
- swallowed errors
- generic failure messages
- hidden retries
- works-on-my-machine blind spots

### 9.6 Fast Feedback Loops

Optimize for:
- short build/test loops
- local clarity
- easy behavior reproduction
- obvious failure points
- rapid debugging

Avoid:
- slow opaque pipelines
- heavyweight ceremony for small changes
- hidden configuration traps
- excessive moving parts in core workflows

### 9.7 Explicit State

Prefer:
- explicit status models
- clear lifecycle transitions
- auditable state changes
- durable contracts

Avoid:
- implicit state changes
- scattered derived truth
- ambiguous done or pending semantics
- silent fallback behavior

### 9.8 Robustness Over Theater

Prioritize:
- predictable behavior
- safe failure modes
- graceful degradation
- idempotence on retryable or repeatable writes
- clear retries and timeouts

Avoid:
- complexity for prestige
- future-proofing that weakens present clarity
- premature optimization that obscures intent

### 9.9 Crisp Interfaces

APIs, schemas, events, and boundaries should be explicit and stable.

Prefer:
- readable contracts
- minimal surface area
- explicit error conditions
- versioning discipline on persisted schemas, stored artifacts, and external contracts

Avoid:
- mushy parameter bags
- undocumented side effects
- inconsistent shapes
- convenience shortcuts that blur intent

### 9.10 Sensible Defaults

Defaults should:
- reduce surprise
- preserve data
- protect trust
- align with normal user behavior
- keep development straightforward

Avoid defaults that are clever, dangerous, or optimized for edge cases over normal use.

### 9.11 Local Reasoning

A serious builder should be able to inspect a part of the code and understand it locally.

Favor:
- small composable modules
- explicit dependencies
- constrained side effects
- local context

Avoid:
- global magic
- framework acrobatics
- hidden mutation
- far-away configuration that changes core behavior

---

## 10. Anti-Patterns

Reject these by default unless there is a very strong reason:

- hidden core actions
- silent state changes
- destructive defaults
- ambiguous loading, save, or failure states
- broken token discipline across type, spacing, color, or motion
- generic starter-app styling
- vague make-it-modern thinking
- decorative gradients used instead of structure
- toy-like controls
- over-rounded marshmallow UI
- dashboard clutter
- excessive pills, badges, and boxed sections
- ornamental motion
- low-contrast ambiguity
- architecture that is clever instead of clear
- abstractions without operational value
- copy that performs friendliness instead of delivering truth
- emptiness masquerading as elegance
- density without structure
- premium styling without tactile quality
- clever defaults that surprise the user

---

## 11. Review Questions

Use these questions in any review of a Spirit Logic product:

- What matters most here?
- What is the main action?
- What is unnecessarily noisy?
- What feels ornamental instead of useful?
- What would make this easier to trust under pressure?
- What feels assembled instead of tuned?
- What part still feels generic?
- What part feels inevitable?

Also ask:
- Are the boundaries clear?
- Is data flow direct?
- Are names strong and literal?
- Did abstractions earn their keep?
- Are states explicit and trustworthy?
- Does this improve real robustness and clarity?
- Do controls feel decisive?
- Is hierarchy carried by structure instead of decoration?
- Does this feel like a favorite machine?

Blocking review failures:
- the main action is unclear
- a critical flow hides or softens state
- type, spacing, color, or motion break the product's own system
- destructive behavior surprises the user
- loading, success, or failure states are ambiguous on a critical flow
- the product relies on decoration where structure should carry the work

---

## 12. Decision Test

Before shipping a meaningful decision, ask:

- Does this feel like a master-built instrument for action?
- Does it increase clarity, tactility, coherence, or trust?
- Does it reduce friction without reducing capability?
- Does it create earned attachment through use?
- Would it still feel right after repeated daily contact?

If not, rework it.

If reviewers disagree after these checks:
1. apply the Conflict Order
2. prefer the simpler artifact
3. prefer the more explicit state model
4. prefer the version that is easier to scan and trust under pressure

---

## 13. One-Line Summary

Build software that feels like a favorite machine:
**direct, tuned, serious, ruthlessly functional, materially coherent, and master-built.**
