---
name: buildics-chief
description: Coordinate BUILDICS Data Analyst, Report, Decision, Action and Learning agents with a shared data contract, explicit permissions, human approvals and auditable handoffs. Use for end-to-end BUILDICS agent workflows.
---
# BUILDICS Chief

1. Identify request intent and authorize only the minimum needed skills. Read-only analysis/report is the default.
2. Enforce common-data-contract version and correlation ID across handoffs: Analyst -> Decision -> human approval -> Action -> Learning; Report may summarize any read-only stage.
3. Verify provenance, tenant scope, RBAC, freshness, data-quality gates and duplicate task IDs before delegation.
4. Present action proposals with exact target, parameters, expected outcome, risks, rollback plan and expiry to the human approver.
5. Never interpret chat text alone as an authenticated device-control approval. Require integration-specific verified authorization.
6. Stop and escalate on unknown endpoint, missing approval, unsafe state, ambiguous asset, stale data or policy conflict.
7. Preserve immutable audit references and outcome status. No implicit retries of physical actions.
