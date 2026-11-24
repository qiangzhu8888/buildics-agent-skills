# Common Data Contract v1.0 (proposed)

This is a **proposed interoperability schema**, not a verified BUILDICS API specification.

Envelope fields: `contract_version` (string, "1.0"), `record_id` (unique string), `record_type` (observation|finding|proposal|approval|action|outcome), `created_at` (ISO 8601 offset timestamp), `source` (source system/file and immutable locator), `asset_id` (pseudonymous identifier), `correlation_id` (shared workflow ID), `payload` (type-specific object), `provenance` (source references and transformations), `schema_status` (verified|mapped|unverified).

Observation payload: `observed_at`, `metric`, `value` (number or null), `unit`, `quality_flags`, `sampling_interval_seconds` (optional).
Finding payload: `window_start`, `window_end`, `method`, `severity`, `evidence_record_ids`, `limitations`.
Proposal payload: `finding_ids`, `options` (each with action, rationale, impact, risk), `priority`, `confidence_basis`, `requires_approval=true`.
Approval payload: `proposal_id`, `actor`, `decision` (approved|rejected|expired), `scope`, `expires_at`, `timestamp`.
Action payload: `proposal_id`, `approval_id`, `mode` (dry_run|execute), `integration_id`, `idempotency_key`, `status`, `audit_log_ref`.
Outcome payload: `action_id`, `measured_at`, `observed_effect`, `expected_effect`, `feedback`, `source`.

Compatibility: retain unknown fields, reject unsupported major versions, never silently convert units or timestamps, and validate required fields before passing between agents. Do not treat an LLM-generated statement as sensor evidence.
