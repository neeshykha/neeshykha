# Aneesh Khan

Support operations leader who builds with AI. Ten years across IoT, SaaS, and hardware; the day job is running a globally distributed technical support team and putting AI into production support workflows.

Most of what's here shares one theme: deploy AI, then measure whether it actually worked. The measuring is the part that usually gets skipped.

[The portfolio hub](https://neeshykha.github.io/portfolio/) puts it all on one page, and anything marked live there runs in a browser with nothing to install. If you only open one thing, make it [kb-health-checker](https://neeshykha.github.io/kb-health-checker/).

## AI deployment and measurement

- **[deflection-audit](https://github.com/neeshykha/deflection-audit)**: your AI vendor reports 85% deflection. This audits what that number survives. It re-judges every AI-closed conversation from the transcript alone, at close time, then recomputes the rate crediting only the closures that hold up. On a 40-conversation labeled set: 80% claimed against 55% audited.
- **[scheduled-agent-detector](https://github.com/neeshykha/scheduled-agent-detector)**: a scheduled agent that hits a permission prompt can't answer it, so it skips the blocked write, exits 0, and reports that it finished. This judges every run on whether the artifact it owes actually moved, and never on the run's own report. Six verdicts, a named failure signature on each miss, and a closing section listing the tasks it can't vouch for. A folder it isn't allowed to read is reported unverifiable, never healthy. [See the demo report](https://neeshykha.github.io/scheduled-agent-detector/).
- **[skill-regression-harness](https://github.com/neeshykha/skill-regression-harness)**: agent skills are prompt-matched, not called, so a model upgrade can stop one from firing without an error anywhere. Static checks plus live dispatch tests of 23 frozen prompts, run under a tool denylist so the skills that reach Salesforce and Gmail can't touch either. 21 of 23 correct on the live run. The first safety control was an allowlist that didn't actually block Bash, and junk rows in the harness's own output are what exposed it.
- **[claude-eval-kit](https://github.com/neeshykha/claude-eval-kit)**: the eval machinery from the projects below, pulled out into something reusable. Blind classification, confusion matrices, ordinal miss-direction splits, and confusable-pattern trap audits.
- **[agent-ops-bench](https://github.com/neeshykha/agent-ops-bench)**: does a second agent pay for itself? Generalist, parallel specialists, and generalist-plus-QA-reviewer, each measured on accuracy, cost per ticket, and latency. Specialists fixed routing and left judgment flat; the QA layer ran $0.60 per net correction.
- **[claude-triage-simulator](https://github.com/neeshykha/claude-triage-simulator)**: an LLM triage classifier with a real eval harness. Confusion matrix, under- versus over-triage analysis, and hand-built edge cases where naive classification breaks.

## Working tools

- **[kb-health-checker](https://github.com/neeshykha/kb-health-checker)**: when a support copilot gives a wrong answer, the root cause is often the article, not the model. Paste a help-center article and get an AI-readiness grade across structure, answer clarity, self-containment, machine readability, and language quality, with a concrete fix for each finding. Every check is a failure mode I've had to diagnose in production. [Try it live](https://neeshykha.github.io/kb-health-checker/); it runs client-side, so the article never leaves your browser.
- **[sf-caseops-mcp](https://github.com/neeshykha/sf-caseops-mcp)**: read-only Salesforce case operations exposed as MCP tools an agent can call. Auth is delegated to the `sf` CLI keychain, so the server never touches credentials, and read-only is enforced by construction rather than by policy. Runs against a live org daily.
- **[claude-resume-pipeline](https://github.com/neeshykha/claude-resume-pipeline)**: job discovery and resume tailoring built on Claude Code. The interesting part is the instruction layer: ATS screening logic encoded as a CLAUDE.md the model executes.

## Outside work

- **[piedmont-bloom-planner](https://github.com/neeshykha/piedmont-bloom-planner)**: a native-plant planner for Atlanta that solves for unbroken bloom March through November and treats heavy clay as a real constraint rather than a footnote. [Open it in a browser](https://neeshykha.github.io/piedmont-bloom-planner/); there's nothing to install.
- **[mqd-calculator](https://github.com/neeshykha/mqd-calculator)**: MQD Runway projects your year-end Delta MQDs and prices out what closes the gap to each Medallion tier: more fare, card spend, or a mileage run. Every program rule is editable data, because loyalty programs change their math and hardcoded calculators go stale. [Live here](https://neeshykha.github.io/mqd-calculator/).
- **[peptide-evidence](https://github.com/neeshykha/peptide-evidence)**: evidence grading for research peptides. Each compound gets a standalone record under a fixed three-axis rubric, with every claim traced to a primary source. The axes are never averaged into one score, because a single number would hide the finding. [Read the records](https://neeshykha.github.io/peptide-evidence/).
- **[Stride-App](https://github.com/neeshykha/Stride-App)**: a native macOS habit and project tracker in SwiftUI, built around every-90-days maintenance that a weekday scheduler can't represent.

Elsewhere: Salesforce admin with 25+ production automations, 85% AI ticket deflection running in production, Atlanta.
