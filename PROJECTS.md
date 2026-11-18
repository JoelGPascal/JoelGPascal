# Projects

Each system started as a bottleneck in my own work. For every project: the problem, what I built, how it's built, and where it stands.

---

## Featured system: JARVIS, JOEL X and AI Workforce · `Working local pilot`

**Problem.** Research records, document drafts and delegated work needed a single reviewable workflow.

**My contribution.** I define the requirements, evidence rules and approval boundaries; direct AI-assisted implementation; operate the system; and review results through bounded acceptance checks.

| Part | Responsibility |
| --- | --- |
| JARVIS | Existing dashboard and user-facing assistant |
| JOEL X | Career research, eligibility/history checks and evidence-backed document drafts in a separate SQLite store |
| AI Workforce | Supervised task routing, model execution records and human review |

**Demonstrated.** Spoken career status, an approval summary that distinguishes separate queues, and one harmless task routed to an existing agent with one linked run and a result awaiting review. A recent staged suite passed 72 provider/routing/approval-security checks. This count is development evidence, not a measure of all-agent reliability.

**Current implementation.** Python services, SQLite career records, JSON/JSONL task records, a React/TypeScript HUD and local Ollama planning. Restricted Claude execution is another implemented lane. Earlier Next.js/Groq and Hermes experiments are historical development stages.

**Next.** Diagnose the almost-five-minute planning latency and misleading outbound warning, then continue granular monitoring, durable task recovery and scoped-memory acceptance. No measured productivity, revenue or hiring gain is claimed.

[Read the concise case study](JARVIS_CASE_STUDY.md). Source and private operational records remain private. This summary does not certify production autonomy or claim independent authorship of every component.

---

## PDH revenue engine · `In development`

**Problem.** Pascal Dominion Holdings buys and sells US residential property. Revenue depends on matching motivated sellers with active buyers quickly, across thousands of CRM records.

**What I built.** The operating system for the business on GoHighLevel: acquisitions and dispositions pipelines, buyer and seller databases, buy-box intelligence, and live seller and investor websites. Custom code handles what the CRM can't verify on its own.

**How it's built.**
- GoHighLevel CRM with custom Property and Buy Box objects
- Phased architecture: CRM foundation and workflow spine complete; property intelligence in progress; supervised AI outreach planned
- Python and JavaScript tools for intake, matching and record verification (two are public, below)

**Next.** Certified form-to-CRM routing and supervised buyer outreach.

---

## CRM Association Verifier · `Public prototype` · [repo](https://github.com/JoelGPascal/crm-association-verifier)

**Problem.** A deal acted on with the wrong contact or property attached costs money and trust.

**What I built.** A read-only service that checks contacts, opportunities and properties are correctly linked before anyone acts, and refuses to answer when the data is incomplete or ambiguous.

**How it's built.** JavaScript on Cloudflare Workers, authenticated requests, bounded read-only API access. 41 tests.

---

## Revenue Intake Demo · `Public prototype` · [repo](https://github.com/JoelGPascal/pdh-revenue-intake-demo)

**Problem.** Property leads arrive from many sources in inconsistent formats, with duplicates.

**What I built.** A pipeline that normalises raw listing inputs, tracks where each record came from, collapses duplicates and flags uncertain fields for review.

**How it's built.** Pure Python with no dependencies, synthetic data only. 8 tests.

---

## How I build

I define the workflow, the evidence rules and the acceptance criteria. I build with Claude Code as my development partner, review every change, and test against the real process. Third-party platforms (GoHighLevel, Hermes Agent, model providers, open-source agent collections) are credited in each repository.
