# Ghost Run Kit

Status: proposed reusable product recipe.
This is not an existing Ghost Chat feature or an installed framework.

## Purpose

Give applications a reusable way to start background jobs, explain progress, request human approval, and deliver results with evidence.

## Activation

Use this recipe only when `PRODUCT.md` explicitly selects Ghost Run Kit.
Do not install dependencies or enable external services merely because this document exists.

Read `PRODUCT.md`, `DESIGN.md`, `AGENTS.md`, and applicable reference rules.
If the required briefs do not exist, follow the repository briefing process and stop before implementation.
See [product recipes](README.md).

## First example product

A client delivery portal.

A user submits a request. A worker prepares a result. The user reviews the specific result version, approves it or requests changes, and can download the approved delivery.

The first slice uses deterministic local fixture data, not paid AI.
It must be clearly labelled as a demonstration.

## Reusable modules

1. Jobs and attempts.
2. Approval decisions.
3. Results and evidence.
4. Usage receipts.
5. Access, retention, and export policy.

Modules are optional. `PRODUCT.md` selects which ones are needed.

## Job contract

States:

- queued
- running
- awaiting_approval
- succeeded
- failed
- cancelled

A job has:

- opaque ID
- owner or workspace ID
- job type
- input version
- current state
- created and updated timestamps
- attempts
- result references

Use server-authoritative state in a deployed multi-user app.

Terminal jobs cannot silently resume.
A retry creates a new attempt.
A cancellation request is distinct from confirmed cancellation.

## Execution safety

Validate state transitions.
Use idempotency for externally triggered operations.
Do not promise exactly-once execution.

Never retry an irreversible action blindly.
Reconcile ambiguous external outcomes before retrying.
Define cancellation checkpoints and external side-effect boundaries.

Do not execute arbitrary commands supplied by clients.

## Approval contract

An approval is bound to:

- job
- action
- target
- result or payload version
- requesting actor
- expiry, when applicable

Changed content invalidates the previous approval.
Approvals require authenticated authorization on the server.
Record who decided, what they decided, and when.

The worker cannot approve its own action.

## Evidence contract

Each check has:

- name
- status: passed, failed, not_run, or inconclusive
- method
- timestamp
- artifact or evidence reference, where available

Missing evidence is not a passed check.
Generated summaries are not proof that a check ran.

Redact sensitive content.
Authorize every private artifact download.
Do not place credentials or private signed URLs in exports.

## Usage contract

Separate estimates, measured usage, calculated cost, and customer charge.
Unknown values remain unknown, not zero.
Record currency and the pricing version used for calculations.
Use exact decimal or integer-minor-unit money arithmetic.

## First screen

Job detail screen only:

- job name and current state
- ordered activity
- result area
- approval panel when required
- checks and evidence
- usage receipt when measured

Include loading, empty, error, interrupted, and permission-denied states.

Do not add dashboards, billing, a workflow canvas, or a template marketplace in the first slice.

## Proposed visual direction

Subject to approval in `DESIGN.md`:

- Feeling: calm progress with clear control.
- Web system: shadcn/ui, one style, only if `PRODUCT.md` and `DESIGN.md` approve a UI library.
- No 3D.
- Paper, ink, and one accent.
- Typography: 14px body, 20px title, 32px hero.
- Spacing: 8, 16, 24, 32.
- One card and button radius.
- One motion idea: reveal newly completed activity.
- Respect reduced motion.

Do not install a UI library without explicit approval.
`DESIGN.md` wins over this section.

## Infrastructure

Keep execution, artifact storage, scanners, and telemetry behind replaceable adapters.

Existing project infrastructure takes priority.
Do not build a durable workflow engine from scratch for the MVP.
Do not claim an in-memory demonstration survives process restarts.

## Acceptance tests

- Refresh shows persisted state in the production implementation.
- Duplicate requests do not create duplicate external actions.
- Concurrent approval and cancellation have a defined outcome.
- A changed payload cannot reuse an old approval.
- Another user cannot read or modify the job or its artifacts.
- Failed or unrun checks are never displayed as passed.
- Unknown usage is never displayed as free.
- Exported files contain no private credentials.
- Narrow layouts and keyboard interaction work.
- Every visible control is exercised.

## Sources

Patterns researched from public repositories. These links are not permission to copy code. Review the licence of each exact component before reuse.

- [Trigger.dev](https://github.com/triggerdotdev/trigger.dev): durable tasks, retries, idempotency, human approval waits, and live run metadata.
- [Langfuse](https://github.com/langfuse/langfuse): traces, evaluations, datasets, experiments, and usage or cost dashboards.
- [Gitleaks](https://github.com/gitleaks/gitleaks): secret detection with redaction and structured reports. Keep any scanner integration replaceable; the project has said new feature work has stopped and later releases are security patches.

Recheck each project's status and licence at the time of use.
