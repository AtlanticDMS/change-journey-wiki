---
title: "Data Quality and Integrity"
type: concept
topic: [data-analytics]
tags: [type/concept, topic/data-analytics, status/complete, source/book]
source_books:
  - "[[Data Insights and Analytics - A Guidebook for SMB Leaders]]"
---

## Definition
The degree to which data is accurate, complete, consistent, timely, and secure throughout its lifecycle. Data quality is the prerequisite for actionable analytics — poor quality data produces misleading insights and catastrophic business decisions.

## Why it matters
The 2023 State of Data Quality Report (Monte Carlo Data) found that data quality issues impact approximately 25% or more of revenue. The book is unequivocal: poor data quality is not merely an inconvenience — it is a strategic risk that has derailed major companies' marketing strategies.

## Eight common data quality issues
1. **Inaccurate data** — typos, misinformation, outdated entries; mitigated by validation rules and automated verification
2. **Incomplete data** — missing fields; mitigated by required field enforcement at data entry
3. **Duplicate data** — multiple records for the same entity; mitigated by deduplication tools and AI-assisted cleaning
4. **Inconsistent data** — different formats, units, or terminologies across sources; mitigated by standardisation at point of collection
5. **Outdated/stale data** — data older than 3 months may be unreliable in fast-moving industries; mitigated by update schedules and automated flagging
6. **Data integrity issues** — corruption from system failures or manipulation; mitigated by access controls and audit trails
7. **Security and privacy concerns** — unauthorised access; mitigated by encryption, RBAC, and compliance with GDPR/CCPA/POPIA
8. **Irrelevant data** — data collected without a clear purpose; mitigated by starting with business questions, not data availability

## Ensuring data quality
- **Data audits** — frequency matched to the rate of change in the data (monthly for e-commerce, quarterly for manufacturing)
- **Cleaning tools** — OpenRefine, Excel (Pandas for Python users), AI-assisted deduplication
- **Real-time validation** — dropdown menus, required fields, calendar pop-ups at the point of data entry
- **Data governance frameworks** — standardised naming conventions, access policies, and storage standards

## Cross-volume link
Data quality is the Vol 3 operational foundation for Vol 2's [[Data Analytics]] — analytics is only as good as the underlying data. Vol 2's [[Cybersecurity]] framework directly protects data integrity. Both volumes cross-reference each other explicitly on this point.

## Related concepts
- [[Concepts/Analytics Framework]] — the governance structure that enforces data quality standards
- [[Data Analytics]] — Vol 2; analytics capability that data quality enables
- [[Cybersecurity]] — Vol 2; security practices that protect data integrity
- [[Ethical Data Use]] — privacy compliance is a dimension of data integrity

## Appears in
- [[Data Insights and Analytics - A Guidebook for SMB Leaders]] (Ch. 2, Ch. 4)

## Themes this concept feeds
- [[Data as Organisational Asset]]

## My thinking
