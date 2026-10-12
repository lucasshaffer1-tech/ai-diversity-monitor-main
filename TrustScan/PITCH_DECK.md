# TrustScan: Pitch Deck Outline
*Concept stage*

### Slide 1: Title
**TrustScan: Verify true second opinions.**
Find out when a hospital's AI tools are not truly independent.

### Slide 2: A story to open with
A 68-year-old patient has a brain MRI. Two AI tools both report "no lesion," each with more than 90% confidence. It looks like two independent opinions. A third tool, built differently, flags a region. In the prototype sample data, the first two tools missed the same finding 62% of the time on similar studies.
*TrustScan's job is to notice this before the report is finalized.*

### Slide 3: The problem
- Hospitals can layer multiple AI tools on the same scans.
- Each tool may be treated as an independent second opinion.
- Tools can share models, training data, and vendor pipelines, and with them, blind spots.
- Result: several tools can miss the same finding at once, and their agreement looks like safety.

### Slide 4: Why it matters
- About 795,000 Americans die or are permanently disabled from diagnostic error each year (Johns Hopkins researchers, 2023; all causes).
- Hospitals rely on AI more every year.
- If tools are not independent, the safety value of using several of them is overstated.

### Slide 5: The market
- 1,524 AI-enabled medical devices on the FDA list as of March 31, 2026; about 76% were radiology devices.
- Hospitals are increasingly adopting AI tools.
- Open question to research: how many hospitals run multiple tools on the same scans?

### Slide 6: The evidence, and its limit
- ICML 2025 (Kim et al.): on one benchmark, language models chose the same wrong answer 60% of the time when both were wrong. Larger, more accurate models were still highly correlated.
- This is language-model research. **Whether the same effect exists in medical imaging is still unproven.** Testing this is step one of our plan.

### Slide 7: Our solution
TrustScan compares hospital AI tools on the same cases and measures how often they fail together.
- Illustrative pair independence scores (to be validated on real imaging data)
- Shared-miss rates
- Subgroup blind-spot analysis
- Advisory alerts that suggest a manual read
- Audit trail for governance teams

### Slide 8: Product experience (show the prototype)
- Dashboard with independence score and trend
- Active alerts for suspicious agreement
- Case view: what each tool said, why it was flagged, suggested next step
- Review queue and audit log
- Cases, Tools, Alerts, and Reports tabs, plus settings for alert sensitivity
- Records tab: enter a case and each tool's result, and see shared misses in your own data

### Slide 9: Why now
- AI adoption in imaging is accelerating.
- Pressure for AI validation and governance is growing.
- Hospital safety and quality teams need ways to show their AI is not a single point of failure.

### Slide 10: Business model (hypotheses to test in interviews)
- Annual subscription per hospital or site
- Add-on governance and compliance reporting
- Integration services with imaging and EHR systems
- Pricing: to be set after interviews with buyers

### Slide 11: Competition and differentiation
| Alternative | What it does | Gap |
|---|---|---|
| Vendor dashboards | Show accuracy for one tool | May not compare tools against each other |
| Imaging AI platforms and marketplaces (for example Aidoc, Blackford; verify current offerings) | Deploy and route multiple tools | May focus on running and routing tools rather than auditing their cross-tool independence |
| General ML monitoring tools | Track drift and performance | May not be built for clinical workflow or cross-tool error overlap |
| Hospital in-house QA | Manual audits | Slow, and rarely looks at cross-tool overlap |

*Risk: large vendors could add a basic version. Our edge would be neutrality across vendors.*

### Slide 12: Regulation and trust
- Advisory monitoring only: flags cases, never diagnoses or blocks a decision.
- Designed with HIPAA in mind; privacy and security are core requirements.
- Every alert and action is logged.

### Slide 13: What we still need to prove
- Do imaging AI tools actually show correlated errors? (retrospective test)
- Will radiologists and quality teams act on the alerts? (interviews)
- Who pays, and how much? (buyer interviews)

### Slide 14: Roadmap
1. Prove the effect on imaging data and interview clinicians.
2. Pilot with 2 to 3 imaging AI tools in one hospital workflow.
3. Add subgroup analysis and governance reporting.
4. Expand to multi-hospital deployment and vendor partnerships.

### Slide 15: Closing
We are not building another diagnostic model. We are building a trust layer for medical AI, so that when a hospital counts a second opinion, it is truly a second opinion.
