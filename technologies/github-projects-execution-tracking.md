---
type: technology-review
status: verified-synthesis
topics: [github-projects, execution, delivery, issues, planning, tracking]
last_reviewed: 2026-09-20
---
# GitHub Projects for Execution Tracking

## Decision context
GitHub Projects is an organizationally selected platform for project/work tracking. The framework therefore does not perform a tool-selection comparison for this capability. Research focuses on how to implement the framework's execution-control model on GitHub Projects with minimum sufficient overhead.

## Primary sources
- Projects overview: https://docs.github.com/en/issues/planning-and-tracking-with-projects/learning-about-projects/about-projects
- Issues: https://docs.github.com/en/issues/tracking-your-work-with-issues/learning-about-issues/about-issues
- Fields: https://docs.github.com/en/issues/planning-and-tracking-with-projects/understanding-fields
- Issue fields: https://docs.github.com/en/issues/planning-and-tracking-with-projects/understanding-fields/about-issue-fields
- Parent/sub-issue progress: https://docs.github.com/en/issues/planning-and-tracking-with-projects/understanding-fields/about-parent-issue-and-sub-issue-progress-fields
- Roadmap: https://docs.github.com/en/issues/planning-and-tracking-with-projects/customizing-views-in-your-project/customizing-the-roadmap-layout
- Insights: https://docs.github.com/en/issues/planning-and-tracking-with-projects/viewing-insights-from-your-project/about-insights-for-projects
- Automation: https://docs.github.com/en/issues/planning-and-tracking-with-projects/automating-your-project

## Verified capabilities
GitHub Issues supports multi-level sub-issue hierarchy and blocking dependencies. Projects can expose parent issue and sub-issue progress.

Projects supports table, board and roadmap-oriented work views, typed/custom fields, date and iteration fields, filtering/grouping/sorting, linked pull-request metadata, built-in workflows, API/Actions automation and configurable charts.

Organization issue fields can provide consistent metadata across repositories/projects and become the issue-level source of truth. Project-local fields remain scoped to one project.

Project Insights supports current and historical charts; the default historical Burn up shows open/completed/not-planned work over time. Archived/deleted items are not included in Insights history.

## Framework mapping

### Work hierarchy
The framework's conceptual hierarchy is:
`Outcome → Initiative/Project → Capability/Epic → Feature → Work Package → Task/Subtask → PR/Test/Evidence`.

Do not force every conceptual level into an Issue. Use parent/sub-issue relationships only where decomposition materially improves ownership, dependency management, progress or traceability.

### Minimum tracking questions
The execution system must answer:
1. What work exists?
2. Who owns it?
3. What state is it in?
4. What blocks it / what does it block?
5. What delivery expectation currently exists?
6. What evidence proves completion?

### Minimal recommended metadata
Prefer a small stable set:
- Status;
- Type;
- Priority;
- Owner/Assignee;
- Parent;
- Dependencies;
- Target Date when supplied;
- Forecast Date when evidence supports it;
- Quality/Evidence status.

Additional Domain/Capability/Risk/Commitment Date fields are introduced only when the project needs them. Avoid duplicating metadata already represented by native GitHub relations/types/milestones.

## Suggested status model
`Backlog → Ready → In Progress → Validate → Done`

Exceptional state:
`Blocked` should preferably be represented by explicit blocking dependency plus visible status/field when operational visibility requires it.

Done means accepted completion evidence exists. Closing code work alone must not silently imply the framework's convergence/release gates passed.

## Views
- Execution Board — active work by Status.
- Work Breakdown — table grouped by Parent/Type.
- Dependency/Blocker view — blocked/blocking work.
- Roadmap — selected date/iteration fields for milestone-level planning.
- Validation view — items awaiting test/evidence/convergence.
- Management view — milestone/capability progress, blockers and forecast variance.
- Insights — burn-up and selected trend charts.

Views are projections of the same Issues/Project data, not separate trackers.

## Automation policy
Start with built-in workflows and native relationships. Add Actions/API automation only for repeatable controls that reduce manual error.

Candidate automations:
- auto-add matching issues;
- initialize Status;
- expose PR linkage;
- flag missing evidence before framework-level Done;
- synchronize selected evidence/gate metadata when deterministic;
- derive reporting data.

Automation must not invent estimates, forecast dates, gate evidence or approval.

## Limits/constraints to preserve
Projects currently supports a finite field budget; avoid field proliferation. Organization issue fields and project-local fields have different scopes and should not duplicate the same semantic concept without a migration reason.

## Framework disposition
**ORGANIZATIONAL PLATFORM DECISION + VERIFIED IMPLEMENTATION BASELINE.**

GitHub Projects is the execution-tracking substrate. The framework still defines work semantics, quality gates, evidence, forecasting and governance.
