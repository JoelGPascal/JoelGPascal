# Projects

Each system started as a bottleneck in my own work. For every project: the problem, what I built, how it's built, and where it stands.

---

## JOEL X — AI career agent · `In development`

**Problem.** A serious job search means scanning dozens of boards, checking eligibility, avoiding duplicate applications and tailoring a CV per role, all without stretching the truth.

**What I built.** An agent that pulls live roles from official job boards, rejects or flags roles I'm not eligible for, remembers every past application, and prepares a CV and cover letter where every claim links back to a verified source. I approve every decision; nothing is submitted automatically.

**How it's built.**
- Python discovery adapters for Greenhouse and Ashby job boards
- Rule-based eligibility (`ELIGIBLE` / `VERIFY` / `REJECT`) with application-history checks
- SQLite records for jobs, decisions, CV versions, evidence links and approvals
- Bounded model tool loop with schemas, time limits and an audit trail
- Next.js interface with browser voice
- 82 offline tests

**Next.** Job-posting liveness checks, claim-level CV verification, and a supervised recruiter-email-to-interview workflow. Benchmarked against [Career Ops](https://github.com/career-ops-hq/career-ops).

---

## JARVIS — command centre · `Pilot`

**Problem.** Career, business and inbox work were spread across a dozen tools with no single view of what needed attention.

**What I built.** One command centre that shows tasks, agent activity, the career pipeline, and email and calendar context, with voice control and an approval queue for anything that acts on my behalf.

**How it's built.**
- Python services with a React/TypeScript HUD
- Gmail and Google Calendar through Google OAuth
- Local models through Ollama, with free-tier cloud models for small tasks
- Agent runtime on Hermes Agent with a localhost model router

**Next.** Lower memory use on the laptop and one connected view of JOEL X and PDH.

---

## AI Workforce — agent coordination · `In development`

**Problem.** Running several specialist agents safely needs task tracking, limits on what each agent can do, and a human review step.

**What I built.** The coordination layer behind JARVIS: an agent registry, task persistence, restricted model execution, review queues and recovery after a crash or restart.

**How it's built.**
- Python HTTP service with JSON/JSONL task and audit records
- Claude CLI and Ollama execution with model routing
- Specialist roles adapted from open-source agent collections (credited in the repo)

**Next.** Merge the consolidation, Windows, model-routing and command-board work into one release.

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
