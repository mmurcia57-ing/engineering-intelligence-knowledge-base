# Master Research Inventory

> KB Recovery & Corpus Migration v1
>
> Purpose: recover the complete research corpus accumulated before and during the Engineering Intelligence & Execution Framework project. This inventory is the control document for migration; an item appearing here does **not** automatically mean its claims are verified.

## Evidence semantics

`REFERENCE ≠ VERIFIED FACT ≠ HYPOTHESIS ≠ DECISION`

- **REFERENCE** — source/project was encountered and is relevant.
- **VERIFIED FACT** — claim checked against a primary or authoritative source.
- **HYPOTHESIS** — plausible interpretation or proposed application requiring validation.
- **DECISION** — explicitly adopted project/framework choice.
- **PENDING** — source or claim still needs recovery/verification.

## Recovery status

This inventory intentionally separates **corpus recovery** from **claim verification**. The first objective is to stop losing research context. Each high-value item will later receive an evidence-backed project/technology/pattern record.

## A. Graph, knowledge and context intelligence

| Item | Type | Recovery state | Verification state | Intended KB destination |
|---|---|---:|---:|---|
| Graphify / Graphify Labs | OSS project | RECOVERED | PARTIALLY VERIFIED | project-reviews/graphify |
| Microsoft GraphRAG | OSS/research | RECOVERED | REVERIFY | technologies/graph-rag |
| Neo4j GraphRAG | OSS/product ecosystem | RECOVERED | REVERIFY | technologies/graph-rag |
| Knowledge Graphs | concept | RECOVERED | FOUNDATION | technologies/knowledge-graphs |
| Temporal Graphs | concept | RECOVERED | RESEARCH REQUIRED | technologies/temporal-graphs |
| Entity Resolution / Canonical Identity | concept/pattern | RECOVERED | RESEARCH REQUIRED | patterns/entity-resolution |
| GraphRAG | pattern | RECOVERED | RESEARCH REQUIRED | patterns/graph-rag |
| Code Knowledge Graph | pattern | RECOVERED | RESEARCH REQUIRED | patterns/code-knowledge-graph |
| Shared Agent Memory / AI Brain | visual/concept reference | RECOVERED | HYPOTHESIS | patterns/shared-agent-memory |
| Obsidian + graph-based knowledge workflows | tool/pattern | RECOVERED | REVERIFY | technologies/knowledge-management |

## B. Runtime topology, observability and SRE intelligence

| Item | Type | Recovery state | Verification state | Intended KB destination |
|---|---|---:|---:|---|
| Toise | OSS project | RECOVERED | REVERIFY | project-reviews/toise |
| OpenTelemetry | standard/ecosystem | RECOVERED | PARTIALLY VERIFIED | technologies/observability |
| OTel Entity Data Model / Entity Events | standard/research | RECOVERED | REVERIFY | technologies/observability |
| OTel GenAI semantic conventions | standard | RECOVERED | REVERIFY | technologies/agent-observability |
| Dynatrace Smartscape / Grail topology | product/reference | RECOVERED | REVERIFY | project-reviews/dynatrace-topology |
| Backstage Catalog Graph | OSS platform | RECOVERED | REVERIFY | project-reviews/backstage-catalog |
| OpenSRE | OSS project | RECOVERED | REVERIFY | project-reviews/opensre |
| Aurora SRE | OSS/project reference | RECOVERED | REVERIFY | project-reviews/aurora-sre |
| RCA Agent | OSS/project reference | RECOVERED | REVERIFY | project-reviews/rca-agent |
| ServiceRadar | OSS/project reference | RECOVERED | REVERIFY | project-reviews/serviceradar |
| Apache SkyWalking Horizon UI | OSS/reference | RECOVERED | REVERIFY | project-reviews/skywalking-horizon |
| RCAEval | research/benchmark | RECOVERED | REVERIFY | research/causal-rca |
| TCRCA | research | RECOVERED | REVERIFY | research/causal-rca |
| CIRCA | research | RECOVERED | REVERIFY | research/causal-rca |
| Graph-assisted RCA | pattern | RECOVERED | HYPOTHESIS | patterns/graph-assisted-rca |
| Temporal operational graph | pattern | RECOVERED | HYPOTHESIS | patterns/temporal-operational-graph |
| Living representation of system for humans + agents | architecture pattern | RECOVERED | HYPOTHESIS | patterns/living-system-graph |

## C. Agent systems, orchestration and automation

| Item | Type | Recovery state | Verification state | Intended KB destination |
|---|---|---:|---:|---|
| Model Context Protocol (MCP) | protocol | RECOVERED | PARTIALLY VERIFIED | technologies/mcp |
| LangGraph | framework | RECOVERED | REVERIFY | technologies/agent-orchestration |
| n8n | automation platform | RECOVERED | REVERIFY | technologies/automation |
| Agent memory | concept | RECOVERED | RESEARCH REQUIRED | technologies/agent-memory |
| Multi-agent systems | concept | RECOVERED | RESEARCH REQUIRED | technologies/multi-agent |
| Agentic architecture | pattern | RECOVERED | RESEARCH REQUIRED | patterns/agentic-architecture |
| Deterministic agent governance | pattern | RECOVERED | HYPOTHESIS | patterns/deterministic-agent-governance |
| AI Operating System / Command Center | UX/architecture pattern | RECOVERED | HYPOTHESIS | patterns/agent-command-center |
| Human → orchestrator → manager agents → worker agents | visual/orchestration pattern | RECOVERED | HYPOTHESIS | patterns/agent-hierarchy |
| Context Engineering | concept | RECOVERED | RESEARCH REQUIRED | technologies/context-engineering |

## D. Graph and technical visualization

| Item | Type | Recovery state | Verification state | Intended KB destination |
|---|---|---:|---:|---|
| ATSMATRIX Agent Graph | OSS/reference | RECOVERED | VERIFIED SOURCE | project-reviews/atsmatrix |
| ATSMATRIX Agent Visualizer / Collision Engine | OSS/reference | RECOVERED | VERIFIED SOURCE | project-reviews/atsmatrix |
| ATSMATRIX Agent Compound | OSS/reference | RECOVERED | REVERIFY | project-reviews/atsmatrix |
| ATSMATRIX Horizon | OSS/reference | RECOVERED | REVERIFY | project-reviews/atsmatrix |
| OpenGraph Intel (OGI) | OSS/reference | RECOVERED | REVERIFY | project-reviews/ogi |
| React Flow | frontend library | RECOVERED | REVERIFY | technologies/graph-visualization |
| Cytoscape.js | graph library | RECOVERED | REVERIFY | technologies/graph-visualization |
| Sigma.js + Graphology | graph/WebGL stack | RECOVERED | REVERIFY | technologies/graph-visualization |
| Reagraph | graph/WebGL library | RECOVERED | REVERIFY | technologies/graph-visualization |
| D3 / Canvas / WebGL / Three.js | visualization stack | RECOVERED | FOUNDATION/REVERIFY | technologies/graph-visualization |
| ForceAtlas2 / worker layout | graph layout | RECOVERED | REVERIFY | technologies/graph-visualization |
| Large-graph cases: dhaga, LumaWeave, brain-nexus | references | RECOVERED | REVERIFY | research/large-graph-ui |

## E. AI-assisted engineering, design and self-hosting

| Item | Type | Recovery state | Verification state | Intended KB destination |
|---|---|---:|---:|---|
| Penpot | OSS design platform | RECOVERED | REVERIFY | technologies/design |
| Ollama | local AI runtime | RECOVERED | REVERIFY | technologies/local-ai |
| yt-dlp | OSS tool | RECOVERED | REVERIFY | technologies/self-hosted |
| Whisper | model/tool | RECOVERED | REVERIFY | technologies/self-hosted |
| Fooocus | OSS image UI | RECOVERED | REVERIFY | technologies/self-hosted |
| Plausible Community Edition | OSS analytics | RECOVERED | REVERIFY | technologies/self-hosted |
| AppFlowy | OSS workspace | RECOVERED | REVERIFY | technologies/self-hosted |
| AI-assisted design → React → Git → deploy workflow | pattern | RECOVERED | HYPOTHESIS | patterns/ai-assisted-delivery |

## F. Creators, visual references and inspiration corpus

These are **references**, not automatically authoritative technical evidence.

| Reference | Source type | Recovery state | Notes |
|---|---|---:|---|
| @benjamlns / Benjamin Fowler | social/reference | RECOVERED | visual agent organization/hierarchy |
| @atsmatrix | social + GitHub | RECOVERED | agent graph / futuristic technical UI |
| @pranathi.rai | social/reference | RECOVERED | AI systems, Claude Code, automation, design-to-code |
| @bennett.spooner | social/reference | RECOVERED | AI OS / command-center concepts |
| @matias_costas | social/reference | RECOVERED | agent automation / n8n / integrations |
| @brunobracaioli | social + technical references | RECOVERED | shared memory, Graphify, agentic infrastructure |
| @pauberenguerai | video/social | RECOVERED | agents, n8n, MCP, memory |
| @iclosegreen | social/reference | RECOVERED | visualization/automation; claims need verification |
| @aianykey | social/reference | RECOVERED | PENDING INSPECTION |
| @tracktor_inovacao | social/reference | RECOVERED | PENDING INSPECTION |
| Ingenia.AI neural-network visual | visual reference | RECOVERED | illustrative only; not literal ChatGPT architecture |
| Cinthya Sanchez AI OSS carousel | social/reference | RECOVERED | self-hosted/open-source tool discovery |
| Andromeda X AI / Bóveda | website/reference | RECOVERED | PENDING INSPECTION |
| SL-SP / Jarvis | website/reference | RECOVERED | identity/implementation still requires verification |

## G. Engineering execution methodology corpus

| Foundation | Recovery state | Verification state |
|---|---:|---:|
| PMI / PMBOK / WBS | RECOVERED | PRIMARY RESEARCH REQUIRED |
| PRINCE2 7 | RECOVERED | PRIMARY RESEARCH REQUIRED |
| Scrum | RECOVERED | PRIMARY RESEARCH REQUIRED |
| Kanban | RECOVERED | PRIMARY RESEARCH REQUIRED |
| Lean | RECOVERED | PRIMARY RESEARCH REQUIRED |
| WSJF / Cost of Delay | RECOVERED | PRIMARY RESEARCH REQUIRED |
| RICE | RECOVERED | PRIMARY RESEARCH REQUIRED |
| Design Thinking | RECOVERED | PRIMARY RESEARCH REQUIRED |
| Lean Startup | RECOVERED | PRIMARY RESEARCH REQUIRED |
| Opportunity Solution Tree | RECOVERED | PRIMARY RESEARCH REQUIRED |
| GitHub Spec Kit / SDD | RECOVERED | PRIMARY RESEARCH REQUIRED |
| C4 Model | RECOVERED | PRIMARY RESEARCH REQUIRED |
| arc42 | RECOVERED | PARTIALLY VERIFIED |
| ADR | RECOVERED | PRIMARY RESEARCH REQUIRED |
| NFR / Quality Attributes | RECOVERED | PRIMARY RESEARCH REQUIRED |
| UML | RECOVERED | PRIMARY RESEARCH REQUIRED |
| BPMN | RECOVERED | PRIMARY RESEARCH REQUIRED |
| ArchiMate / TOGAF | RECOVERED | PRIMARY RESEARCH REQUIRED |
| SysML | RECOVERED | PRIMARY RESEARCH REQUIRED |
| Event Storming | RECOVERED | PRIMARY RESEARCH REQUIRED |
| Threat Modeling / STRIDE | RECOVERED | PRIMARY RESEARCH REQUIRED |
| SRE | RECOVERED | PRIMARY RESEARCH REQUIRED |
| DORA / DevOps | RECOVERED | PRIMARY RESEARCH REQUIRED |
| Critical Path / PERT | RECOVERED | PRIMARY RESEARCH REQUIRED |
| Monte Carlo forecasting | RECOVERED | PRIMARY RESEARCH REQUIRED |
| Throughput / Cycle Time / Burn-up / CFD | RECOVERED | PRIMARY RESEARCH REQUIRED |

## H. Experiments already proposed

1. Graphify context benchmark — same repository/task with and without Graphify.
2. Temporal topology lab — OTel entity events → durable event log → temporal graph.
3. GraphRAG comparison — LLM-only vs RAG vs GraphRAG.
4. Agent observability lab — agent/tool/memory spans using OTel GenAI semantics.
5. SRE RCA lab — topology + telemetry + change events + causal candidates + agent explanation.
6. Graph UI scale lab — React Flow vs Cytoscape vs Sigma/Graphology/Reagraph at increasing node counts.

## I. Open recovery queue

The following still need exact URLs/IDs recovered or reverified before promotion to VERIFIED FACT:

- Original Instagram Reel/post URLs and unresolved TikTok/YouTube Shorts.
- Exact repositories for OpenSRE, Aurora SRE, RCA Agent, ServiceRadar and large-graph examples.
- Exact OGI repository and feature verification.
- Exact Toise repository/current architecture.
- Bruno Bracaioli repositories/specs and the provenance of the shared-memory visual.
- Pau Berenguer Pixel Agents reference.
- Bennett Spooner/Merydian repositories and architecture claims.
- SL-SP Jarvis implementation.
- Andromeda X AI / Bóveda.
- Claims from the Graphify + Obsidian guide that exceed upstream documentation.
- Research-paper metadata and benchmark figures for RCAEval/TCRCA/CIRCA.

## J. Promotion rule

An item leaves this inventory and becomes a durable KB record only after:

1. source identity is established;
2. source URL is persisted;
3. relevant claims are separated into fact vs inference;
4. primary source is preferred where available;
5. last-reviewed date is recorded;
6. potential use in the framework/SRE is labeled as **hypothesis** until tested;
7. decisions are recorded separately from research.

This document remains the corpus-level completeness checklist.


## K. UX, frontend/backend contracts, identity and application security

This corpus is **not limited to graph visualization**. A production engineering framework must cover the complete user-to-backend trust and interaction path.

| Area | Topics to research and persist | State |
|---|---|---|
| UX architecture | information architecture, journeys, task flows, navigation, progressive disclosure, empty/loading/error states, accessibility, responsive behavior, design systems | RECOVERED AS REQUIRED DOMAIN |
| Technical UI | dashboards, command centers, graph UX, tables/timelines, filtering, search, drill-down, real-time state, high-density interfaces | RECOVERED AS REQUIRED DOMAIN |
| Frontend architecture | SPA/SSR trade-offs, component boundaries, state management, routing, BFF patterns, performance budgets, frontend observability | RESEARCH REQUIRED |
| Frontend ↔ backend contracts | OpenAPI, JSON Schema, contract-first design, schema/version compatibility, validation, error contracts, idempotency, pagination, async APIs | RESEARCH REQUIRED |
| Contract assurance | consumer/provider contract testing, integration tests, E2E tests, schema checks in CI/CD, compatibility gates | RESEARCH REQUIRED |
| Authentication | OAuth 2.x, OpenID Connect, sessions, tokens, PKCE, BFF/token mediation, workload/service identity | RESEARCH REQUIRED |
| Authorization | RBAC, ABAC, ReBAC, policy-based access control, least privilege, resource/action modeling | RESEARCH REQUIRED |
| API/application security | OWASP ASVS, OWASP API Security, threat modeling, input/output validation, CSRF/CORS, secrets, rate limiting | RESEARCH REQUIRED |
| Identity lifecycle | provisioning, federation, session lifecycle, revocation, service accounts/workload identities, auditability | RESEARCH REQUIRED |
| Zero Trust boundaries | user/device/workload identity, trust boundaries, continuous verification concepts | RESEARCH REQUIRED |
| UX security | secure defaults, re-authentication, privileged actions, confirmation patterns, error/privacy leakage | RESEARCH REQUIRED |
| Observability across UI/API | correlation IDs, frontend telemetry/RUM, distributed tracing, user journey → API → service linkage | RESEARCH REQUIRED |

### Required assurance chain

```
User / Persona
  → UX Journey
  → UI State
  → Frontend Component
  → API Contract
  → Authentication
  → Authorization / Policy
  → Backend Use Case
  → Domain/Data Rules
  → Persistence / External Dependency
  → Response Contract
  → UI State
  → Telemetry / Audit / Evidence
```

The framework must be able to prove that critical requirements remain traceable across this chain.

### Candidate Quality Gates

- UX flow covers happy path, alternate paths and failures.
- UI does not invent backend capabilities absent from a contract.
- API implementation conforms to versioned contract.
- Consumer/provider compatibility is tested.
- Authentication mechanism is appropriate to client type and threat model.
- Authorization is enforced server-side; frontend visibility is not an authorization control.
- Privileged actions have explicit policy/audit requirements.
- Security controls and trust boundaries are represented in architecture.
- Critical user journeys are observable end-to-end.
- Accessibility and performance criteria are testable, not merely visual preferences.

### Research priority

Primary/authoritative sources should include standards and specifications where applicable (IETF OAuth, OpenID Foundation/OIDC, OWASP, OpenAPI/JSON Schema, W3C accessibility) plus implementation-pattern evidence. Product-specific authentication choices remain decisions, not universal defaults.


## L. Recovery closure — 2026-09-20

### Engineering baseline disposition
The material engineering domains required to start Framework v0.1 refinement now have primary-source-backed records in the KB, including UX/accessibility, frontend-backend contracts, browser authentication, authorization, application/API security, functional modeling, architecture/NFR, SDD, WBS/forecasting, testing/conformance, CI/CD gates, observability/SRE/RCA, graph/context technologies, agent orchestration/memory/MCP and agent observability.

### Remaining references
The unresolved social/visual items in section I are retained under `research/recovery-disposition.md` as **REFERENCE-ONLY**, **UNVERIFIED** or **DEFERRED**. They are not evidence dependencies for Framework v0.1 and therefore do not block the recovery gate.

Exact implementation claims for those items must not be promoted without source verification or reproduction.

### Reconciliation rule
Where an older row in this inventory still says `RESEARCH REQUIRED` but a dedicated verified record now exists under `methods/`, `technologies/`, `patterns/` or `project-reviews/`, the dedicated record is authoritative. This master inventory remains the recovery ledger, not the detailed evidence source.

### Recovery milestone
**KB RECOVERY & CORPUS MIGRATION v1: COMPLETE**

This means the corpus is sufficiently materialized to refine the framework. It does **not** mean every reference on the internet has been verified, every candidate technology has been selected, or every hypothesis has become a decision.
