---
name: ghl-agent-build
description: Build or extend HighLevel Conversation AI, Agent Studio, or Voice AI agents and reusable tenant-aware API tooling. Use for a new GHL agent or framework milestone; use a testing or optimization skill for an existing agent's response issues.
---

# Build GHL agents

Identify the product before choosing endpoints. Conversation AI bots, Agent Studio
flows, managed agents, and Voice AI agents are distinct products, not interchangeable
names. Read [agent types](references/agent-types.md) for the selected product.

## Establish the target

Read the user's plan and repository instructions before edits. Capture location ID,
agent ID and displayed name, product type, purpose, channels, allowed changes,
deployment mode, and any excluded original or managed agent. Read the target back
before writes. Prefer the user-designated copy; never switch agents merely because
another agent supports the endpoint you wanted.

Keep business rules in a tenant profile: age eligibility, prices and billing periods,
calendar mappings, persona, booking policy, handovers, equipment, and followup timing.
Separate confirmed facts, provisional owner decisions, and unresolved facts. Do not
copy another gym's rules into a new tenant.

## API-first implementation

Verify every operation in current official HighLevel documentation before coding.
Record it in a capability registry with product/category, operation, classification,
method and path when documented, API version, auth and scopes, request schema,
limitations, source URL, and verification date. Classifications are PUBLIC_API,
INTERNAL_OR_ASK_AI_ONLY, BROWSER_FALLBACK, and UNKNOWN. A missing search result does
not prove an API is unavailable; record the exact scope of the investigation.

Use public APIs for documented operations. Do not invent paths, infer write support
from undocumented GET fields, or call private browser endpoints. UI-only capabilities
may use the environment's authorized browser tooling when the user's scope permits.
Do not assume a particular browser runtime exists on another machine.

Use environment variables GHL_PRIVATE_TOKEN, GHL_LOCATION_ID, and GHL_AGENT_ID.
Never embed credentials in skills, scripts, examples, logs, or committed results.
Keep the API client independent from tenant policy, test generation, grading, and UI
drivers so it can support a future CLI or MCP. Reject cross-tenant mismatches, redact
errors, set timeouts, and avoid blindly retrying mutations after uncertain outcomes.

## Incremental delivery

Implement only the requested milestone. Back up configuration before mutation,
preserve unrelated fields, and verify saved state. If actions might be shared, check
ownership before changing them. Creating or editing a bot does not authorize enabling
live channels, sending messages, booking appointments, or publishing changes.

For a first API milestone, verify authentication and location, discover the intended
agent, and use an officially supported test execution path. Capture the returned
session/execution ID, reuse it for a second turn, and verify remembered context.
If this product lacks a verified execution route, complete independent work and
report that limitation. Do not use an unrelated agent to claim success.

Deliver structured evidence, configuration instructions, exact working and blocked
operations, missing scopes, and focused test results. Mock tests establish client
behavior, not live authentication or conversation persistence.

## Growth Factor integration

When present, reuse the repository's ghl-chat-bot/src/ghl-client,
config/ghl-capabilities.json, config/tenants, scenarios, and ignored results folders.
Inspect the actual CLI and supported operations before invoking them. This skill
also works without that module; it does not itself install a client or grant access.
