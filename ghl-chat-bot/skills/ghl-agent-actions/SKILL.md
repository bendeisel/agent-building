---
name: ghl-agent-actions
description: Configure or simplify HighLevel agent actions, calendar routing, workflow triggers, staff handovers, notifications, and followups. Use when changing who handles a request or what happens after an agent response.
---

# Configure GHL agent actions

Build an action map from the user's intended behavior:
trigger, destination/person, customer acknowledgement, task or notification,
followup timing and timezone, pause/resume behavior, and opt-out handling.
Use existing authorized routing when requested. Ask for a specific assignee only
when the change needs one; do not guess a manager from a display name.

Inspect the exact tenant and agent, current action IDs, linked workflows, and shared
ownership. Preserve an original or excluded agent. A copy may reference shared
objects; check before mutation rather than assuming copy means isolation.

## Choose built-in behavior or workflows

Verify current official HighLevel documentation and the account's available controls.
Human Handover may assign a user, send a final reply, create a task, tag a contact,
and pause/resume the bot. Auto Follow-Up serves different purposes: inactive,
busy, or requested future contact. A task for a manager is not an automated check
that the manager replied. Do not promise followups while a bot is inactive without
verifying the supported resume path.

Inspect skip-assignment settings: an existing contact owner may prevent a newly
selected manager from receiving the conversation. Notifications depend on the
recipient's enabled channels. Verify email support for the exact event in the
current UI; do not assume every task alert is an email. Conversation summary emails
may be delayed by inactivity thresholds and are not necessarily immediate handover
alerts. Record these limitations when proposing workflow replacement.

Prefer built-in actions when they fully cover the requested behavior. Keep workflows
for conditional escalation, custom notifications, deadlines, or other logic not
covered. Avoid competing automated followups. Do not delete or disable working
workflows just because a simpler configuration looks plausible.

## Safe implementation

Before API use, record endpoint, version, auth/scopes, request shape, source URL,
date, and limitations in a capability registry. Use PUBLIC_API where documented;
classify UI-only work BROWSER_FALLBACK and unverified work UNKNOWN. Keep
INTERNAL_OR_ASK_AI_ONLY distinct. Never invent private endpoints or undocumented
write fields. Use authorized browser controls for supported UI-only configuration.

Back up affected fields and preserve unrelated details. Confirm shared action IDs
before updates. Check saved values by reading them back. Keep secrets in environment
variables and exclude contact history and configuration dumps from public commits.

Configuration work does not authorize sending a test email/SMS to a real person or
booking a production slot. Use authorized controlled test resources. A no-contact
preview can prove acknowledgement and a visible trigger, not delivery or task arrival.
If the owner accepts configuration evidence for now, record that acceptance and
the unverified delivery separately.

Before retiring a workflow, verify the replacement against the owner's success
criteria and retain a rollback path. Report the action map, changed fields, exact
verification level, remaining scopes or unknowns, and anything left active.
