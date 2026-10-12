# SWOT: TrustScan (AI independence monitoring for hospitals)

## Strengths

- **Large, documented problem:** Johns Hopkins researchers estimate about 795,000 Americans die or are permanently disabled from diagnostic error each year (BMJ Quality & Safety, 2023).
- **Fast-growing pool of overlapping tools:** the FDA list showed 1,524 AI-enabled medical devices as of March 31, 2026; about 76% were radiology devices.
- **Research behind the core idea:** an ICML 2025 study of 350+ language models found they agreed on the same wrong answer 60% of the time on one benchmark, and that larger, more accurate models were still highly correlated.
- **Easy to explain:** second opinions are standard in medicine, so "make sure the second opinion is truly independent" needs little setup.
- **Clear product boundary:** advisory monitoring that flags cases and does not diagnose.

## Weaknesses

- **No imaging-specific proof yet:** the correlated-error research is on language models, so the central claim is plausible but unproven for imaging tools.
- **Unknown market size:** no source found counts how many hospitals run multiple AI tools on the same scans.
- **Needs sensitive data and hospital cooperation** to test and monitor, which is slow and heavily regulated.
- **True independence is hard to establish:** different models need different training data, and good medical data is limited.
- **Abstract story:** "models share blind spots" needs a concrete patient scenario. The prototype's case #184920 (two tools report no lesion, a third flags one) is a first attempt.
- **Hard-to-reach customers:** clinician and hospital-staff interviews take time and connections.

## Opportunities

- **Growth in medical AI** may increase the relevance of this problem as more tools are adopted.
- **Regulatory and governance attention** to AI safety and validation could turn independence audits into an expectation.
- **Malpractice insurers** might reward hospitals that can show their AI is not a single point of failure.
- **An open research gap:** because we have not identified evidence establishing this effect in imaging tools, original interviews and a retrospective test could provide useful new evidence.
- **Bias detection as a bonus:** the same analysis shows patient groups where all tools underperform.
- **Partnerships** with radiology software vendors or hospital systems could speed adoption.

## Threats

- **Regulation:** a tool that influences diagnosis may face stricter device oversight, so TrustScan should stay advisory.
- **Vendors building it in:** large imaging and health-record companies could add a basic version to their platforms.
- **Liability fears:** hospitals may worry about being blamed if an alert is raised and nobody acts on it.
- **Slow sales cycles** and slow trust-building among clinicians and hospital buyers.
- **Privacy breaches:** one leak could end the business.
- **Data access:** without hospital data, the imaging claim stays unproven.

## Strategic implication

Do not sell "AI safety" in the abstract. Sell one specific problem: hospitals believe they have independent second opinions, but their tools may share the same blind spots. Make it concrete with a patient scenario, a clinical workflow, and evidence from emerging research. The first milestone is to test whether imaging tools actually show correlated errors.

---

## Assignment notes (not part of the business SWOT)

These points are about the class project, so they are kept separate from the SWOT above.

- **Fit with the project requirements:** the idea uses machine learning, touches cybersecurity and privacy, aims to benefit people, and can be shown as a wireframe or dashboard.
- **Risks to the grade:** a weak opening story or thin primary research could cost points even though the idea is strong.
- **Strongest next steps:** open with the case #184920 story, interview at least a few clinicians or hospital staff, and cite sources for every statistic.
