# TrustScan: One-Page Summary
*Concept stage.*

## Product
TrustScan is a monitoring tool that checks whether a hospital's AI imaging tools are truly independent or are reinforcing the same blind spots.

## The problem
A hospital that runs several AI tools on the same scans may treat each as an independent second opinion. But tools can be trained on similar data, share model lineage, or use overlapping vendor pipelines, so they can agree on the same wrong answer. The hospital believes it has layered safety when it may have one shared blind spot.

## Why it matters
- Johns Hopkins researchers estimate about 795,000 Americans die or are permanently disabled from diagnostic error each year (all causes, not only AI).
- The FDA list showed 1,524 AI-enabled medical devices as of March 31, 2026; about 76% were radiology devices.
- Early research on language models found they agree on the same wrong answer 60% of the time when both are wrong, even for larger, more accurate models. Whether imaging tools behave the same way is the open question TrustScan would test.

## Solution
TrustScan compares the outputs of a hospital's AI tools on the same cases and measures how often they fail together. It highlights shared blind spots and suggests a manual read when AI agreement looks suspicious.

## How it works
1. Ingest outputs from multiple AI tools.
2. Compare agreement, disagreement, and confidence on each case.
3. Measure correlated errors: how often one tool misses a finding that the other also missed.
4. Break results down by patient group, scan type, and finding.
5. Send advisory alerts suggesting a radiologist read.
6. Log every alert and action for governance and quality review.

## Key features
- Illustrative pair independence scores (to be validated on real data)
- Shared-miss rates
- Subgroup blind-spot analysis
- Case-level advisory alerts
- Review workflow with an audit trail
- Record entry: log a case and each tool's result to see shared misses in your own data
- Governance and compliance reporting

## Users
Radiologists, clinical quality and safety teams, hospital governance leaders, compliance teams, and imaging AI validation teams.

## Market opportunity
Hospitals are increasingly adopting AI tools, and governance expectations are growing with them. The number of hospitals running overlapping tools is not yet measured, so sizing the market is a first research task.

## Positioning
Many monitoring approaches focus on each tool's accuracy. TrustScan asks a different question: are our tools giving independent second opinions, or are they missing the same thing?

## Boundary
TrustScan is advisory monitoring. It does not diagnose, and clinicians make every decision.

**Tagline:** Verify true second opinions.
