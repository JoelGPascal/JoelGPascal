# Joel Gabriel Pascal

I build and integrate AI-assisted systems for two practical needs: managing a job search and operating a real estate business. The work has three connected parts: JARVIS, a personal AI assistant and command centre; JOEL X, an AI career agent; and PDH business automation built around GoHighLevel (GHL). AI Workforce provides the agent coordination, task execution and human-review layer.

[Project engineering overview](PROJECTS.md) explains the components, technical work, evidence boundaries and public source examples.

## Projects

| Project | Engineering work | Scope |
| --- | --- | --- |
| JARVIS — Personal AI Assistant | Central dashboard for tasks, agent activity, career summaries, Gmail/Calendar access and human approvals; Python backend with a React/TypeScript HUD in development | Private local engineering pilot; integrated capabilities and deployment evidence are documented by branch |
| AI Workforce | Agent registry, restricted Claude/Ollama execution, model routing, task persistence, review queues and recovery mechanisms supporting JARVIS | Python service with JSON/JSONL state; newer integrated work remains in draft PRs |
| JOEL X — AI Career Agent | Python job-board discovery, eligibility/history checks, SQLite records, evidence-backed drafts and a later Next.js/model-tool interface | Private development system; drafts require review; automated submission is not implemented in the inspected workflow |
| PDH / GoHighLevel Business Automation | CRM data/workflow design for buyers, sellers and deals; source validation, property relationships, sanitized reporting and buyer/seller matching work | GHL is the third-party operational platform; custom code and prototypes are separate, with live integration status documented individually |
| [CRM Association Verifier](https://github.com/JoelGPascal/crm-association-verifier) | JavaScript Cloudflare Worker checking contact/opportunity/property relationships with fail-closed results | Public prototype and tests; live end-to-end deployment is not established |
| [PDH Revenue Intake Demo](https://github.com/JoelGPascal/pdh-revenue-intake-demo) | Pure Python normalization, source tracking, deduplication and review flags | Public synthetic-data demo; no CRM writes or outreach |

The private projects are not available as complete public deployments. Their local installations also depend on private state and configuration that are excluded from Git.

## How the systems fit together

JARVIS is the interface and assistant. AI Workforce manages agent tasks and review. JOEL X owns career records and draft preparation. GHL owns PDH business records and its native workflows. Custom adapters and reports connect selected information; this does not mean every planned integration is live.

**Technical work:** Python HTTP services, REST API integrations, Google Desktop OAuth, SQLite career state, JSON/JSONL task and audit records, JavaScript/TypeScript interfaces, deterministic validation, restricted model execution, isolated tests, and Windows startup/recovery tooling. The linked repositories distinguish merged code, development branches, prototypes and recorded runtime checks.

## Design and implementation approach

Work is prepared for human review. Uncertain source data stays uncertain; a draft or pipeline label is not treated as proof of a completed external action.

The projects use Python, JavaScript/TypeScript, local HTTP services, SQLite, browser interfaces and selected third-party APIs. Implemented capabilities differ by repository and branch; a model integration or agent definition alone does not establish autonomous operation.

I define workflow requirements and evidence/acceptance rules, direct and review AI-assisted implementation, integrate components and test results against the intended workflow. Repository history includes AI co-authorship.

Agent definitions and plugins reuse third-party collections. The private HUD has a separate upstream origin. Hermes and other model tools are components or historical foundations, not software I claim to have authored.

## Development record

As of 14 November 2026, JARVIS/JOEL X documentation is being reconciled with source, tests and draft branches. The priorities are reproducibility, explicit integration boundaries, source-to-runtime mapping and dependable human control. No production reliability or business-effectiveness claim is implied.

The public repositories contain synthetic examples and their own setup/test instructions.
