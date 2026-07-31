# Aneesh Khan

Support operations leader who builds with AI. Ten years across IoT, SaaS, and hardware; the day job is running a globally distributed technical support team and putting AI into production support workflows.

Most of what's here shares one theme: deploy AI, then measure whether it actually worked. The measuring is the part that usually gets skipped.

## AI deployment and measurement

- **[deflection-audit](https://github.com/neeshykha/deflection-audit)**: your AI vendor reports 85% deflection. This audits what that number survives. It re-judges every AI-closed conversation from the transcript alone, at close time, then recomputes the rate crediting only the closures that hold up. On a 40-conversation labeled set: 80% claimed against 55% audited.
- **[claude-eval-kit](https://github.com/neeshykha/claude-eval-kit)**: the eval machinery from the projects below, pulled out into something reusable. Blind classification, confusion matrices, ordinal miss-direction splits, and confusable-pattern trap audits.
- **[agent-ops-bench](https://github.com/neeshykha/agent-ops-bench)**: does a second agent pay for itself? Generalist, parallel specialists, and generalist-plus-QA-reviewer, each measured on accuracy, cost per ticket, and latency. Specialists fixed routing and left judgment flat; the QA layer ran $0.60 per net correction.
- **[claude-triage-simulator](https://github.com/neeshykha/claude-triage-simulator)**: an LLM triage classifier with a real eval harness. Confusion matrix, under- versus over-triage analysis, and hand-built edge cases where naive classification breaks.

## Working tools

- **[sf-caseops-mcp](https://github.com/neeshykha/sf-caseops-mcp)**: read-only Salesforce case operations exposed as MCP tools an agent can call. Auth is delegated to the `sf` CLI keychain, so the server never touches credentials, and read-only is enforced by construction rather than by policy. Runs against a live org daily.
- **[claude-resume-pipeline](https://github.com/neeshykha/claude-resume-pipeline)**: job discovery and resume tailoring built on Claude Code. The interesting part is the instruction layer: ATS screening logic encoded as a CLAUDE.md the model executes.

## Outside work

- **[piedmont-bloom-planner](https://github.com/neeshykha/piedmont-bloom-planner)**: a native-plant planner for Atlanta that solves for unbroken bloom March through November and treats heavy clay as a real constraint rather than a footnote. [Open it in a browser](https://neeshykha.github.io/piedmont-bloom-planner/); there's nothing to install.
- **[Stride-App](https://github.com/neeshykha/Stride-App)**: a native macOS habit and project tracker in SwiftUI, built around every-90-days maintenance that a weekday scheduler can't represent.

Elsewhere: Salesforce admin with 25+ production automations, 85% AI ticket deflection running in production, Atlanta.
