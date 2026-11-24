# BUILDICS Agent Skills

Public, documentation-first starter release (2026-11-24). This repository defines six interoperable BUILDICS Agent skills and a versioned common data contract. It does **not** contain production API credentials, actual customer data, a deployed agent, or verified BUILDICS API endpoint definitions.

## Skills
- [Data Analyst](skills/buildics-data-analyst/SKILL.md): CSV/Excel ingestion, semantic mapping, quality checks, time series and anomaly analysis
- [Report](skills/buildics-report/SKILL.md): accessible, evidence-linked HTML reporting
- [Decision](skills/buildics-decision/SKILL.md): prioritized, explainable action proposals
- [Chief](skills/buildics-chief/SKILL.md): orchestration, approvals and delegation
- [Action](skills/buildics-action/SKILL.md): approval-gated execution plans, dry-run default
- [Learning](skills/buildics-learning/SKILL.md): outcomes and feedback, no autonomous policy changes

## Safety
Default to read-only. Never infer production endpoints or field semantics from names alone. Do not execute physical controls without explicit operator authorization, an allowlisted integration, safety interlocks and auditable confirmation. Do not commit secrets or personal/sensor production datasets.

## Data contract
See [contracts/common-data-contract.md](contracts/common-data-contract.md). All timestamps must include a timezone, all observations a unit and source, and all conclusions a provenance reference. Unknown schema mappings are explicitly marked unverified.

## Status
This is a new baseline implementation of instructions, not a claim that earlier locally produced ZIP contents were copied byte-for-byte. Validate against actual BUILDICS exports and existing skills before production use.
