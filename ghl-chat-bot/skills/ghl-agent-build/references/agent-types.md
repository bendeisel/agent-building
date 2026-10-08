# Product selection

Start at https://marketplace.gohighlevel.com/docs/ and follow the current product
reference. These are discovery pointers, not a frozen endpoint catalog.

| Product | Establish before implementation | Avoid |
| --- | --- | --- |
| Conversation AI | Bot ID, channels, full prompt, knowledge sources, calendars and actions | Treating it as an Agent Studio flow or assuming an execution endpoint exists |
| Agent Studio | Agent kind, flow/version, publication state, documented execution and session contract | Executing an excluded managed agent as a substitute |
| Voice AI | Inbound/outbound purpose, phone routing, voice settings, test-call destination and actions | Assuming SMS tests establish voice or phone behavior; making an unrequested call |
| Managed agent | Ownership and documented supported customization surface | Treating provider-managed configuration as editable by default |

Different business roles within a product should be tenant profiles rather than
forked clients: appointment setter, FAQ/front desk, qualification, support, or
re-engagement. Select the relevant profile without forcing every agent toward sales.

Capability registry entries should distinguish reading configuration, updating it,
executing a conversation, and verifying effects. Knowing that a workflow is attached
does not establish that it ran. A browser test is not proof of a public API session.

Preserve a reviewable version or before/after snapshot of prompt, actions, routing,
and deployment mode. On rollback, restore only the fields changed by the task after
checking for newer user changes.
