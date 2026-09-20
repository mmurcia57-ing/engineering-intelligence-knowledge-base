---
type: method
status: verified-synthesis
version: 0.1
topics: [product, ux, functional-design, interaction-design, information-architecture, accessibility]
last_reviewed: 2026-09-21
---
# Product, UX & Functional Engineering

## Objective
Transform an outcome/capability into a usable, testable and implementable experience without starting from screens.

## Evidence baseline
Primary/reference bases include WCAG 2.2/WAI guidance, established journey/task/process/state modeling already catalogued in this KB, React state guidance, frontend/backend contracts, application-security baseline, and validated project/reference repositories.

A visual repository or social reference is not evidence that a UX pattern is correct for the product. References are inputs to exploration; user goals, domain rules, accessibility, system capability and validation govern the design.

## Lifecycle
1. Outcome & capability framing
2. User/persona/job/context
3. Journey & task discovery
4. Information architecture
5. Functional model
6. Interaction model
7. Wireframe / low-fidelity structure
8. Prototype when interaction uncertainty warrants it
9. Visual/system design
10. State completeness
11. UX/accessibility validation
12. Engineering contract
13. Implementation assurance
14. Evidence & learning

This lifecycle is adaptive. Existing valid artifacts are inspected and preserved under NO-REDO.

## 1. Outcome and capability framing
Before screens, define:
- intended outcome;
- capability being enabled;
- actor/user;
- trigger;
- desired result;
- constraints/known policies;
- success evidence;
- known uncertainty.

If the problem, actor or desired result is materially unknown, do discovery rather than inventing UI.

## 2. Journey and task discovery
Model the user's context, entry point, goal, major steps, decisions, handoffs, exceptions and completion signal.

Choose only useful artifacts:
- journey map for cross-step experience/context;
- task flow for focused user goal;
- BPMN for formal human/system process;
- EventStorming for domain/event discovery;
- state machine for lifecycle/state complexity;
- decision table for rule-heavy behavior.

## 3. Information architecture
Define:
- information objects;
- hierarchy;
- navigation model;
- grouping;
- labels/terminology;
- search/filter/sort when needed;
- progressive disclosure;
- role/context-specific visibility.

Do not derive IA from backend tables or existing endpoints by default.

## 4. Functional model
For each capability/task capture:
- trigger/preconditions;
- inputs;
- actions;
- business/domain rules;
- decisions;
- state transitions;
- outputs;
- alternate paths;
- failure/recovery paths;
- permissions;
- audit/telemetry requirements;
- acceptance criteria.

## 5. Interaction model
For each meaningful interaction specify:
- user intent;
- control/action;
- immediate feedback;
- loading/progress;
- success;
- empty/no-data;
- validation error;
- system error;
- partial/stale data;
- permission denied;
- timeout/retry;
- destructive confirmation/undo where applicable;
- keyboard/focus behavior;
- responsive/adaptive behavior where applicable.

A happy-path screenshot is not a complete interaction design.

## 6. Wireframe and prototype
Wireframes answer structure, hierarchy and task flow before visual polish.

Prototype when uncertainty concerns navigation, interaction, comprehension, complex manipulation, progressive disclosure or critical workflow. Do not prototype solely because the framework has a prototype phase.

## 7. Visual/system design
Apply design-system primitives/tokens/components before one-off styling where a design system exists.

Evaluate:
- hierarchy and information density;
- scanability;
- consistency;
- typography;
- spacing;
- icon meaning;
- data visualization semantics;
- feedback/status;
- responsive behavior;
- accessibility;
- visual states.

Visual novelty is subordinate to task success and comprehension.

## 8. Accessibility baseline
WCAG 2.2 is the default external baseline for web experience unless organizational policy defines a stronger/different target. Relevant concerns include perceivable labels/instructions, keyboard operability and focus, predictable behavior, name/role/value, status messages, accessible authentication and error prevention/recovery.

Accessibility is designed and tested, not added after implementation.

## 9. Engineering contract
A protected interactive capability should be traceable through:

`Outcome/Requirement → Persona/Journey → Task/Functional Rule → UI State → Frontend Action → API/Event Contract → Authentication Context → Authorization Policy → Backend Use Case → Domain/Data Rule → Response/Event → UI State → Telemetry/Audit → Test/Evidence`

Not every low-risk feature needs a document for every node; the relation must be discoverable enough to control risk.

## 10. Design-to-engineering handoff
Before implementation, engineering must be able to determine:
- component/state behavior;
- data needed and ownership;
- API/event contract;
- validation location;
- authN/authZ behavior;
- errors/recovery;
- loading/async behavior;
- accessibility expectations;
- telemetry/audit;
- acceptance criteria;
- visual reference/tokens/assets;
- unresolved decisions.

A static mockup alone is not READY FOR IMPLEMENTATION for stateful software.

## 11. UX assurance
Validate at the appropriate level:
- requirement/capability coverage;
- journey/task completeness;
- alternate/error/recovery paths;
- state completeness;
- information architecture coherence;
- functional rules;
- backend feasibility/contract alignment;
- authorization behavior;
- accessibility;
- responsive behavior;
- visual consistency;
- usability/comprehension where uncertainty warrants user validation.

## 12. Reference/repository use
Classify references:
- VISUAL INSPIRATION — aesthetic/composition only;
- INTERACTION REFERENCE — candidate behavior to inspect;
- TECHNICAL PATTERN — source-backed implementation approach;
- COMPONENT/TOOL CANDIDATE — technology to evaluate;
- VERIFIED ENGINEERING EVIDENCE — may support framework decisions.

Never promote a visually impressive repository directly into product requirements or architecture.

## Gate: UX/FUNCTIONAL READY
PASS when the experience needed for current scope is sufficiently specified to implement without material invention by the coding agent.

Minimum, proportional to risk:
- actor + goal/outcome known;
- required journeys/tasks covered;
- functional rules and material states known;
- alternate/failure paths addressed;
- IA/navigation sufficient;
- UI behavior and data needs explicit;
- frontend/backend contract feasible;
- authN/authZ implications known;
- accessibility target/checks defined;
- acceptance evidence defined;
- material ambiguity resolved or SPEC-BLOCKER.

## Anti-patterns
- Screen-first product definition.
- Five mockups treated as five requirements.
- Backend-table-driven UX.
- Happy-path-only design.
- AI inventing missing domain rules.
- Visual reference treated as validated UX.
- design system compliance treated as usability proof.
- inaccessible custom interaction justified by aesthetics.
- handoff as screenshots without states/contracts.
