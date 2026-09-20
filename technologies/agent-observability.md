---
type: technology-review
status: verified-development
topics: [opentelemetry, genai, agents, tools, observability]
last_reviewed: 2026-09-20
---
# Agent and GenAI Observability

## Primary source
https://opentelemetry.io/docs/specs/semconv/registry/attributes/gen-ai/

## VERIFIED FACT
OpenTelemetry defines GenAI semantic concepts including agent identity, workflow naming, model/token usage and operations such as `create_agent` and `execute_tool`. Relevant GenAI semantic conventions remain in development/evolution and must be versioned when adopted.

OpenTelemetry's own demo demonstrates grouping an end-to-end agent run in a workflow span with child LLM/tool spans.

## Privacy boundary
Prompt/completion/tool content can contain sensitive data. Recording content must be explicit and governed; metadata-level observability should not imply unrestricted prompt capture.

## Proposed telemetry model
`user/request → agent/workflow → model call → tool call → external system → result`

Capture where appropriate:
- agent/workflow identity;
- model/provider;
- tool identity;
- latency/error;
- token/resource usage;
- trace/correlation ID;
- policy/approval outcome;
- evidence references.

## HYPOTHESIS
Agent observability should be a Quality Gate for production agentic workflows, especially when tools can mutate external systems.
