# TrustScan — AI independence monitoring for hospitals

**Verify true second opinions.** TrustScan is a concept for a monitoring tool that checks whether a hospital's AI imaging tools are truly independent, or whether they share blind spots and miss the same finding together.

**Status:** Concept stage. This package contains documents and a clickable prototype with made-up sample data. There is no working software, no real data, and no hospital integration. Last updated: October 2026.

## The problem

A hospital that runs several AI tools on the same scans may treat each one as an independent second opinion. (How common this setup is has not been measured.) But tools can share model families, training data, and vendor pipelines. If they share a blind spot, they can all miss the same tumor, and agreement between them gives false confidence. Nobody has to be doing anything wrong for this to happen, and a single accuracy score for each tool will not reveal it.

## The solution

TrustScan compares the outputs of a hospital's AI tools on the same cases and measures how often they fail together. It:

1. Tracks an **illustrative pair independence score** for each pair of tools (higher means the tools make more different mistakes; the calculation would need validation on real imaging data).
2. Reports a **shared-miss rate**: when one tool misses a confirmed finding, how often the other misses it too.
3. Finds **subgroup blind spots**, such as patient groups, anatomy types, or scan conditions where several tools underperform.
4. Raises **advisory alerts** when AI agreement looks suspicious, suggesting a manual read.
5. Keeps an **audit trail** for governance and quality teams.

TrustScan is designed as advisory monitoring only. It does not diagnose, and it does not block or change a clinician's decision. Keeping this boundary matters for regulation (see the SWOT).

## Evidence

| Claim | Source | Caveat |
|---|---|---|
| About 795,000 Americans die or are permanently disabled each year from diagnostic error | Newman-Toker et al., Johns Hopkins, *BMJ Quality & Safety*, 2023 | Covers all diagnostic error, not AI specifically |
| 1,524 AI-enabled medical devices on the FDA list as of March 31, 2026; about 76% were radiology devices | FDA AI-Enabled Medical Device List | The FDA says the list is not comprehensive. This is a dated snapshot, and the count may have changed since March 31, 2026 |
| On one benchmark, language models agreed on the same wrong answer 60% of the time when both were wrong; larger, more accurate models were still highly correlated | Kim, Garg, Peng and Garg, "Correlated Errors in Large Language Models," ICML 2025 | Language models, not imaging tools. Whether imaging AI behaves the same way is unproven |

## What is in this package

| File | What it is |
|---|---|
| `index.html` | Landing page |
| `prototype.html` | Clickable dashboard prototype (sample data) |
| `ONE_PAGE_SUMMARY.md` | One-page product summary |
| `PITCH_DECK.md` | Pitch deck outline |
| `SWOT.md` | SWOT analysis plus assignment notes |
| `BRAND.md` | Naming and tagline |

Open the two `.html` files in any modern browser. They need no installation.

## The prototype

The dashboard shows four sample cases in its review queue, and the Cases tab lists six. The main one (#184920) shows the core idea: two tools both report "no lesion" with high confidence, a third tool flags one, and the prototype sample data shows the first two tools missing the same finding 62% of the time on similar studies. You can open each case, request a second read, and dismiss alerts with a required reason. Every action is written to an on-screen audit log.

The prototype has seven tabs: Dashboard, Cases (search and filter), Records (enter a case and each tool's result; ratings, shared-miss counts, and a CSV download update from your own entries, and they are saved in your browser only), Tools (tools and pair independence), Alerts (all alerts, including dismissed or hidden ones), Reports (mock report requests and a real audit-log CSV download), and Settings. Settings let you choose which alert levels appear, set the shared-miss threshold that triggers pair alerts, change text size, layout density, and time format, and edit the display name. They are saved in your browser only.

Records are for made-up data only; the rating rules are simple illustrations, not validated. Left out on purpose: real data, login, report generation, and email notifications (the email setting is a mock).

## What a real version would need

- Connections to hospital AI tool outputs and PACS/EHR systems
- A backend that computes correlation and subgroup statistics
- Privacy and security controls, designed with HIPAA in mind, plus access control and audit logging
- Clinical validation, starting with a retrospective test on imaging data to see whether imaging tools show correlated errors

## Roadmap (hypothesis)

1. **Prove the effect:** test whether imaging AI tools show correlated errors, using retrospective or public data, and interview radiologists and quality staff.
2. **Pilot:** monitor 2 to 3 imaging AI tools in one hospital workflow.
3. **Deepen:** add subgroup analysis and governance reporting.
4. **Scale:** multi-hospital deployment and vendor partnerships.

## Presenting

1. Open with the patient story on slide 2 of the pitch deck.
2. Open `prototype.html` and click case #184920 to show the core idea. Then use the Cases, Tools, and Alerts tabs to show the wider workflow, and change the shared-miss threshold in Settings to show alerts appearing and disappearing.
3. In the Records tab, enter a case live (for example two tools saying "no finding" and a third flagging one) and show it appear in Cases with a high rating.
4. Use the evidence slides to explain why it matters, and be clear that the imaging claim is still to be proven.
5. Close with "What we still need to prove" and the roadmap.

## Submitting for a class

- Include all files in one folder, with the two HTML files together (they link to each other).
- Add your preferred contact information to the footer of `index.html` if your assignment requires it.
- The package uses a dated FDA snapshot: 1,524 devices as of March 31, 2026. If you present a newer count, update the date and number everywhere.
- Add your own interview or survey findings to this README and the SWOT. Original research is your strongest addition.

## Limits to state honestly

- The prototype is a mockup with sample data.
- The correlated-error research is on language models, not imaging tools.
- The market size is unknown.
- The 62% figure in the prototype is made-up sample data, not clinical evidence.
- The independence score is illustrative and has not been validated.
- Settings and records are saved only in your browser. Only the CSV downloads are real; the report buttons and the email setting are mocks.

## Sources

- Kim, E., Garg, A., Peng, K., Garg, N. "Correlated Errors in Large Language Models." ICML 2025. https://proceedings.mlr.press/v267/kim25e.html
- FDA, Artificial Intelligence-Enabled Medical Devices list. https://www.fda.gov/medical-devices/software-medical-device-samd/artificial-intelligence-enabled-medical-devices
- Newman-Toker, D. et al. Burden of serious harms from diagnostic error in the USA. *BMJ Quality & Safety*, 2023.
