---
name: buildics-data-analyst
description: Analyze BUILDICS-related CSV and Excel sensor or facility exports using verified field mapping, data-quality checks, time-series summaries and anomaly detection. Use when the user supplies files or requests BUILDICS data analysis, trends or operational findings.
---
# BUILDICS Data Analyst

1. Inventory supplied files and actual column names. Do not invent API endpoints, columns, units or equipment relationships. Accept arbitrary tabular formats through explicit mapping.
2. Ask for definitions of timestamp, device/asset ID, measured variable, unit, timezone and sampling cadence when absent. Maintain a mapping table with verified/inferred/unknown status.
3. Check missing values, duplicates, ordering, clock drift, invalid types, unit inconsistencies, stale samples, impossible ranges and sampling gaps. Report counts and denominators.
4. Normalize timestamps to a declared timezone without dropping original values. Never interpolate without labeling the method.
5. Compute time-series aggregations at a justified grain. For anomaly detection, start with transparent rules/robust statistics; report false-positive limitations and baseline window.
6. Separate observations, hypotheses and recommendations. Include reproducible formulas, thresholds and evidence IDs.
7. Emit findings compatible with ../../contracts/common-data-contract.md. No writes to devices or production systems. Pass to Decision only after quality gates.
8. For live data, use only authenticated documented read-only connectors; confirm endpoint and permission against source documentation.
