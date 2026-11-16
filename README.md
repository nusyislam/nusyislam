# Hi, I'm Nusy

AI engineer building LLM tooling with guardrails. Computer Engineering at Stony Brook University, graduating May 2027. Based in NYC.

The part of AI engineering I like most is where the model meets a real system: deciding what the LLM is allowed to control, what stays deterministic, and proving it works with tests and evals.

---

## Experience

**AI Engineering Fellow (Founding Cohort), DNAi Systems** · Nov 2026 to present
Healthcare AI startup building neurosymbolic systems.

**Growth Engineering Intern, Blaze (YC S24)** · Oct to Nov 2026
Took a prototype AI lead-monitoring pipeline to production in the company's internal app, adding safety guards, cost controls, and scoring fixes, and built a second automated data pipeline alongside it.

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

**[Application Autofill](https://github.com/nusyislam/application-autofill)** · Chrome extension, Claude API · *Live on the Chrome Web Store (unlisted)*
Autofills job applications on Workday, Greenhouse, Lever, Ashby, and YC from your saved profile, and uses Claude for free-response questions it can't match. Bring your own API key, no account, and your data never leaves your browser. Next up for 2.0: multiple resumes with a per-application picker, first-run profile prefill from your resume, and a local application tracker with CSV export.

**[fpgrowth-cuda](https://github.com/nusyislam/fpgrowth-cuda)** · C++17, OpenMP, CUDA, Python
FP-Growth frequent itemset mining with serial, OpenMP, and CUDA versions, benchmarked on four UCI datasets on an RTX 4070 desktop and an NVIDIA Jetson Orin Nano. The OpenMP version mines each top-level item's conditional tree in parallel, and the CUDA version is a hybrid that offloads item and conditional-support counting to the GPU while the recursion stays on the CPU. Correctness is checked against a brute-force reference (thousands of randomized runs, including under AddressSanitizer) and exact itemset matches with mlxtend. OpenMP gave 7.1x to 11.8x speedups on the desktop and 5.2x to 6.7x on the Jetson, while the GPU kernel was up to 110x faster for its step but gave no end-to-end gain, since that step is at most 1.8% of a serial run.

**[AI Gym Tracker](https://github.com/nusyislam/ai-gym-tracker)** · FastAPI, SQLite, Claude API
Log workouts in plain English and get real plateau detection. Looks at the last 8 sessions per exercise and excludes auto-regulation "down" days so one off day doesn't count as a stall. Also detects weight and rep PRs, works on mobile, and supports transactional JSON import/export.

**[Speed-to-Lead](https://github.com/nusyislam/speed-to-lead)** · Python, FastAPI, Claude, Airtable, Discord
Instant AI lead qualification and follow-up. Deterministic hard rules run before the LLM, sign-offs are generated in code instead of by the model, and an eval suite (including prompt-injection and out-of-ICP fixtures) took it from 5/7 to 7/7 passing.

**Vision-Guidance Wearable** · Senior design, project lead *(in progress)*
A wearable for blind and low-vision users using an OAK-D depth camera and Raspberry Pi: RANSAC ground-plane fitting and YOLOv8 detection, with haptic feedback instead of audio so users keep their ambient hearing. An orchestration layer decides what to run and when, and the safety-critical obstacle loop stays off the LLM path entirely.

**[Census Income Prediction](https://github.com/nusyislam/Census-Income-Prediction)** · scikit-learn
Break Through Tech fellowship project: random forest and logistic regression, 0.72 F1 with class imbalance handling.

---

## Tools

Python · C++ · CUDA · OpenMP · SQL · Java · FastAPI · Databricks · SQLite · Claude API · Claude Code · MCP · Chrome Extensions · scikit-learn

---

## Contact

[LinkedIn](https://www.linkedin.com/in/nusaybah-islam/) · nusy.islam@gmail.com
