# Hi, I'm Nusy
 
AI engineer building LLM tooling with guardrails. Computer Engineering at Stony Brook University, graduating May 2027. Based in NYC.
 
The part of AI engineering I like most is where the model meets a real system: deciding what the LLM is allowed to control, what stays deterministic, and proving it works with tests and evals.
 
---
 
## Experience
 
### AI Engineering Fellow (Founding Cohort), DNAi Systems
*Nov 2026 to present*
 
Healthcare AI startup building neurosymbolic systems.
 
### Growth Engineering Intern, Blaze (YC S24)
*Oct to Nov 2026*
 
Built three lead-sourcing pipelines with Claude Code for an early-stage fintech, including one that turned 481 job posts into 282 verified decision-maker contacts for $1.82 in scraping costs.
- Took a founder-built Instagram lead monitor to production (Next.js, Supabase) with a budget guard and dry-run controls, growing its tests from **25 to 237**.
- Used SQL to find AI scoring silently failing in production, added Slack alerts, and built a Gemini replacement benchmarked across 8 runs (20/20 identical outputs at temperature 0).
- Built a daily LinkedIn commenter pipeline (scraping, LLM classification, Apollo enrichment) with a $1/day cost cap and **134 tests**, and fixed LLM false positives found through hand-verification with strict evidence rules.
### AI Engineer Intern, Commvault
*Jun to Aug 2026*
 
Part of a 5-engineer team that took Commvault's MCP Gateway for its Cortex platform from a local prototype to production. The gateway centralizes authentication, authorization, rate limiting, and audit logging for 80+ governed AI tools across Databricks, Salesforce, and Datadog.
- **Databricks data foundation for the Sales AI Hub integration:** SQL transformations turning 20 raw Salesforce and HGI tables into 8 scored Silver tables and 5 account-level Gold products. Self-taught SQL and Databricks from zero.
- **Deterministic data-layer routing:** a rule-based resolver that picks the Bronze, Silver, or Gold table for each request. The LLM can choose which tool to call, but never which data tier it reads.
- **Salesforce RBAC preflight:** an authorization check that fails closed before any Databricks query runs.
- **65 automated tests** covering routing, input validation (including SQL-injection-style rejection), and both authorization outcomes.
The project won Commvault's Engineering Intern Showcase. I presented it to the CPO and CTO, and with my project partner to the CCO in Fort Lauderdale.
 
### Software Engineer Intern, Commvault
*Jun to Oct 2024*
 
Python and VBA automation for billing reports, replacing manual Excel work.
 
**Also:** Break Through Tech AI/ML Fellow (Cornell Tech) · TA for ESE 224, Advanced Programming and Data Structures in C++
 
---
 
## Projects
 
### [Application Autofill](https://github.com/nusyislam/application-autofill)
*JavaScript · Chrome Extensions (MV3) · Claude API · pdf.js · Published on the Chrome Web Store (unlisted)*
 
Autofills job applications across eight portals (Workday, Greenhouse, Lever, Ashby, Gem, iCIMS, Rippling, and YC) with a shared core and per-portal adapters. Rules answer first, a Haiku classifier routes unknown questions back to rules, and Claude only answers above a confidence threshold. It never submits for you, legal and EEO questions never go to AI, and page text is treated as data to block prompt injection.
 
Version 1.1 (in store review) adds resume prefill: upload your resume and LinkedIn PDF, the text is extracted locally in the browser, Claude structures it into schema-validated JSON, and any value that doesn't appear in the source text is dropped before you review the suggestions.
 
Backed by 600+ regression checks across 120+ fixtures built from real application failures, plus 260+ setup and UI tests. Shipped publicly with a privacy policy, narrowed permissions, and versioned releases. Bring your own API key, no account, and your data stays in your browser. Next up for 2.0: multiple resume versions and a local application tracker.
 
### [fpgrowth-cuda](https://github.com/nusyislam/fpgrowth-cuda)
*C++17 · OpenMP · CUDA · Python*
 
FP-Growth frequent itemset mining with serial, OpenMP, and CUDA versions, benchmarked on four UCI datasets on an RTX 4070 desktop and an NVIDIA Jetson Orin Nano. The OpenMP version mines each top-level item's conditional tree in parallel, and the CUDA version is a hybrid that offloads item and conditional-support counting to the GPU while the recursion stays on the CPU. Correctness is checked against a brute-force reference (thousands of randomized runs, including under AddressSanitizer) and exact itemset matches with mlxtend. OpenMP gave 7.1x to 11.8x speedups on the desktop and 5.2x to 6.7x on the Jetson, while the GPU kernel was up to 110x faster for its step but gave no end-to-end gain, since that step is at most 1.8% of a serial run.
 
### [AI Gym Tracker](https://github.com/nusyislam/ai-gym-tracker)
*FastAPI · SQLite · Claude API*
 
Log workouts in plain English and get real plateau detection. Looks at the last 8 sessions per exercise and excludes auto-regulation "down" days so one off day doesn't count as a stall. Also detects weight and rep PRs, works on mobile, and supports transactional JSON import/export.
 
### [Speed-to-Lead](https://github.com/nusyislam/speed-to-lead)
*Python · FastAPI · Claude · Airtable · Discord*
 
Instant AI lead qualification and follow-up. Deterministic hard rules run before the LLM, sign-offs are generated in code instead of by the model, and an eval suite (including prompt-injection and out-of-ICP fixtures) took it from 5/7 to 7/7 passing.
 
### [Wearable Obstacle-Detection Aid](https://github.com/nusyislam/point-cloud-9-vision-guide)
*Senior design · Project lead · Python · DepthAI · MicroPython · In progress*
 
Leading a 3-person team building a wearable for blind and low-vision users that signals obstacle distance and direction through vibration instead of audio, so users keep their ambient hearing. I built the perception pipeline on an OAK-D S2 stereo depth camera: 30 fps RGB-aligned depth and nearest-obstacle detection in left, center, and right zones, streamed to a Raspberry Pi Pico 2 W driving a haptic driver over I2C with a 500 ms motor failsafe. I modeled the camera's minimum depth range from stereo geometry, confirmed it by measurement, and switched to extended disparity to halve the close-range blind spot (30.5 to 15 cm). The safety-critical loop stays on classical depth thresholding, off any language-model path.
 
### [Census Income Prediction](https://github.com/nusyislam/Census-Income-Prediction)
*scikit-learn*
 
Break Through Tech fellowship project: random forest and logistic regression, 0.72 F1 with class imbalance handling.
 
---
 
## Tools
 
Python · C++ · CUDA · OpenMP · SQL · Java · FastAPI · Databricks · SQLite · Claude API · Claude Code · MCP · Chrome Extensions · scikit-learn
 
---
 
## Contact
 
[LinkedIn](https://www.linkedin.com/in/nusaybah-islam/) · nusy.islam@gmail.com
 
