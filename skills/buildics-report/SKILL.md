---
name: buildics-report
description: Produce understandable, responsive HTML reports from BUILDICS analysis findings, with charts, data-quality warnings, traceable evidence and action-oriented summaries. Use when the user asks for a BUILDICS HTML report or visual explanation of analysis.
---
# BUILDICS Report

1. Accept observations and findings from Data Analyst; validate contract version, timestamps, units, source references and quality warnings.
2. Produce a self-contained accessible HTML report: executive summary, KPI cards, trends, anomaly timeline, affected assets, evidence table, data quality, assumptions, recommended follow-up.
3. Use readable labels, responsive layouts, accessible contrast and table alternatives to charts. Never present hypothetical numbers as actual measurements.
4. Display time range, timezone, units, data freshness, source file IDs, calculation method and confidence/limitations prominently.
5. Distinguish observed facts from Decision proposals. Sanitize untrusted text before HTML insertion; do not embed credentials or raw personal data.
6. Verify that charts match tables and all claims link to evidence. No operational writes.
