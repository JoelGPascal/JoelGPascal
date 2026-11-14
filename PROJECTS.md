# Project engineering overview

I build and integrate systems for personal assistance, career operations and business workflows. The applications are related but have separate responsibilities and records.

## JARVIS: personal assistant and command centre

JARVIS brings task activity, career summaries, email/calendar context and business-data review into a local interface. Its engineering work includes Python HTTP APIs, browser dashboards, Google Desktop OAuth integration, human-review boundaries and Windows launch/recovery tooling. A newer React/TypeScript HUD exists in development alongside the baseline interface.

The local installation and private source are not a complete public deployment. Interface appearance, implementation and live verification are separate.

## AI Workforce: orchestration infrastructure

AI Workforce supplies the agent registry, task persistence, model execution, review queues and recovery mechanisms. It combines third-party role definitions/plugins with repository-specific orchestration code. Claude and Ollama paths are supervised; optional provider fallback is separate configuration.

The challenge is controlling what an agent can see or execute while preserving task/result provenance and human decisions. Registered roles do not establish that every role has been independently exercised or that the system is autonomous.

## JOEL X: AI career agent

JOEL X discovers jobs from official board sources, checks eligibility and application history, preserves career records in SQLite and prepares evidence-linked CV/application drafts. Later development adds a Next.js interface, bounded model-to-tool interaction, browser voice and canonical candidate-profile handling.

Important engineering boundaries include stable source identity, history freshness, duplicate/reapplication checks, versioned artifacts and review state. Preparing a document is distinct from confirming its quality or submitting it. Automatic submission is not implemented in the inspected workflow.

## PDH / GHL: business workflow automation

GoHighLevel is the third-party operational platform. The engineering work around it concerns CRM data/workflow design, exact record relationships, review-only source intake, deterministic validation, reporting and matching. JARVIS reporting is separate from GHL's native workflow configuration and customer state.

Public source examples:

| Example | What can be inspected |
| --- | --- |
| [CRM Association Verifier](https://github.com/JoelGPascal/crm-association-verifier) | JavaScript Worker, authenticated request contract, bounded read-only API access, exact association checks and failure handling |
| [Revenue Intake Demo](https://github.com/JoelGPascal/pdh-revenue-intake-demo) | Pure Python normalization, source tracking, deduplication, unverified-data labels and synthetic tests |

Neither public prototype certifies the complete live business workflow or any business outcome.

## Contributions, technologies and evidence

I define requirements, data/evidence rules and acceptance criteria; direct and review AI-assisted implementation; integrate components; and check behavior against the workflow. Commit history records AI assistance. I do not claim authorship of GHL, model providers, upstream agent collections or the imported HUD.

The work spans Python, JavaScript/TypeScript, REST APIs, OAuth, SQLite, JSON/JSONL state, browser interfaces, model routing, deterministic validation and local recovery. Private repositories document exact source paths, branch differences, test scope and unresolved technical work. Public examples include their own setup, source and dated verification records.

Documentation date: 14 November 2026. Working source, tested behavior, live deployment and future plans are kept distinct; no production-readiness or measured business-benefit claim is implied.
