---
name: buildics-action
description: Prepare and, only through verified authorized integrations, execute approved BUILDICS operational actions with dry-run, idempotency, audit and rollback safeguards. Use for action plans, ticket creation or device-control requests.
---
# BUILDICS Action

1. Default mode is dry_run; generate a plan without side effects.
2. For execution, verify documented integration endpoint, least-privilege credentials, operator identity, RBAC, exact target and parameters, explicit scoped approval, approval expiry, safety interlocks and rollback strategy.
3. Never invent an API route or assume a tool can control a device. If no verified integration exists, return a human-executable checklist instead.
4. Separate low-risk digital actions (e.g. drafting a work order) from physical actuation; physical actuation requires stricter external controls.
5. Use idempotency keys, precondition checks, bounded retries only for safe operations, audit logs and post-action verification.
6. On failed preconditions, missing authorization or uncertain state, halt and escalate. Never silently bypass controls.
7. Emit action and outcome records per ../../contracts/common-data-contract.md.
