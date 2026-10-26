# Hi, I'm Nusy

AI engineer building LLM tooling with guardrails. Computer Engineering at Stony Brook University, graduating May 2027. Based in NYC.

The part of AI engineering I like most is where the model meets a real system: deciding what the LLM is allowed to control, what stays deterministic, and proving it works with tests and evals.

---

## Experience

**Growth Engineering Intern, Blaze (YC S24)** · Oct 2026 to present
Building lead enrichment and outbound automation for Blaze's growth team.

**AI Engineer Intern, Commvault** · Jun to Aug 2026
Part of a 5-engineer team that took Commvault's MCP Gateway for its Cortex platform from a local prototype to production. The gateway centralizes authentication, authorization, rate limiting, and audit logging for 80+ governed AI tools across Databricks, Salesforce, and Datadog.

What I owned:
- **Databricks data foundation for the Sales AI Hub integration:** SQL transformations turning 20 raw Salesforce and HGI tables into 8 scored Silver tables and 5 account-level Gold products. Self-taught SQL and Databricks from zero.
- **Deterministic data-layer routing:** a rule-based resolver that picks the Bronze, Silver, or Gold table for each request. The LLM can choose which tool to call, but never which data tier it reads.
- **Salesforce RBAC preflight:** an authorization check that fails closed before any Databricks query runs.
- **65 automated tests** covering routing, input validation (including SQL-injection-style rejection), and both authorization outcomes.

The project won Commvault's Engineering Intern Showcase. I presented it to the CPO and CTO, and with my project partner to the CCO in Fort Lauderdale.

**Software Engineer Intern, Commvault** · Jun to Oct 2024
Python and VBA automation for billing reports, replacing manual Excel work.

Also: Break Through Tech AI/ML Fellow (Cornell Tech) · TA for ESE 224, Advanced Programming and Data Structures in C++

---

## Projects

**[AI Gym Tracker](https://github.com/nusyislam/ai-gym-tracker)** · FastAPI, SQLite, Claude API
Log workouts in plain English and get real plateau detection. Looks at the last 8 sessions per exercise and excludes auto-regulation "down" days so one off day doesn't count as a stall. Also detects weight and rep PRs, works on mobile, and supports transactional JSON import/export.

**[Speed-to-Lead](https://github.com/nusyislam/speed-to-lead)** · Python, FastAPI, Claude, Airtable, Discord
Instant AI lead qualification and follow-up. Deterministic hard rules run before the LLM, sign-offs are generated in code instead of by the model, and an eval suite (including prompt-injection and out-of-ICP fixtures) took it from 5/7 to 7/7 passing.

**Application Autofill** · Chrome extension, Claude API *(in progress)*
Autofills job applications on Workday, Greenhouse, Lever, Ashby, and YC. Bring your own API key, no account, and your data stays local.

**Vision-Guidance Wearable** · Senior design, project lead *(in progress)*
A wearable for blind and low-vision users using an OAK-D depth camera and Raspberry Pi: RANSAC ground-plane fitting and YOLOv8 detection, with haptic feedback instead of audio so users keep their ambient hearing. An orchestration layer decides what to run and when, and the safety-critical obstacle loop stays off the LLM path entirely.

**[Census Income Prediction](https://github.com/nusyislam/Census-Income-Prediction)** · scikit-learn
Break Through Tech fellowship project: random forest and logistic regression, 0.72 F1 with class imbalance handling.

---

## Tools

Python · C++ · SQL · Java · FastAPI · Databricks · SQLite · Claude API · Claude Code · MCP · scikit-learn

---

## Contact

[LinkedIn](https://www.linkedin.com/in/nusaybah-islam/) · nusy.islam@gmail.com
