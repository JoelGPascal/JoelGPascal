# Joel Gabriel Pascal

I am building supervised AI workflows for career operations, task coordination and business-data review. The projects grew from a practical need: keep source evidence, generated work and human decisions together when several tools are involved.

## Projects

| Project | Engineering work | Scope |
| --- | --- | --- |
| JARVIS AI Workforce | Python task/API service, agent registry, restricted model execution, review queues, integration adapters and local dashboard work | Private engineering pilot; newer integrated code remains in draft PRs |
| JOEL X | Python job-board discovery, eligibility/history checks, SQLite records, evidence-backed drafts and a later Next.js/model-tool interface | Private development system; drafts require review; automated submission is not implemented in the inspected workflow |
| [CRM Association Verifier](https://github.com/JoelGPascal/crm-association-verifier) | JavaScript Cloudflare Worker checking contact/opportunity/property relationships with fail-closed results | Public prototype and tests; live end-to-end deployment is not established |
| [PDH Revenue Intake Demo](https://github.com/JoelGPascal/pdh-revenue-intake-demo) | Pure Python normalization, source tracking, deduplication and review flags | Public synthetic-data demo; no CRM writes or outreach |

The private projects are not available as complete public deployments. Their local installations also depend on private state and configuration that are excluded from Git.

## Design and implementation approach

Work is prepared for human review. Uncertain source data stays uncertain; a draft or pipeline label is not treated as proof of a completed external action.

The projects use Python, JavaScript/TypeScript, local HTTP services, SQLite, browser interfaces and selected third-party APIs. Implemented capabilities differ by repository and branch; a model integration or agent definition alone does not establish autonomous operation.

I define workflow requirements and evidence/acceptance rules, direct and review AI-assisted implementation, integrate components and test results against the intended workflow. Repository history includes AI co-authorship.

Agent definitions and plugins reuse third-party collections. The private HUD has a separate upstream origin. Hermes and other model tools are components or historical foundations, not software I claim to have authored.

## Development record

As of 14 November 2026, JARVIS/JOEL X documentation is being reconciled with source, tests and draft branches. The priorities are reproducibility, explicit integration boundaries, source-to-runtime mapping and dependable human control. No production reliability or business-effectiveness claim is implied.

The public repositories contain synthetic examples and their own setup/test instructions.
