---
name: ghl-facebook-ads
description: Build, edit, and verify Facebook and Instagram campaigns through HighLevel Ad Manager, including lead forms, manual placements, creative comparisons, and draft handoffs. Use for GHL advertising work, not Conversation AI prompt editing.
---

# GHL Facebook ads

Read [the SOP](references/SOP.md) before operating Ad Manager. It covers new campaigns, existing-ad edits, UI recovery, and final verification.

## Operating rules

- Confirm the GHL sub-account, connected Meta ad account, Facebook Page, and Instagram identity from the current UI. Never inherit another client's account from an open tab.
- Reuse the user's brief and prior answers. Ask only for unresolved information that changes the build, such as destination or unidentified assets. Continue independent draft work while waiting.
- Prefer an official current API for supported operations. Before coding an endpoint, verify official documentation and record method, path, scopes, request shape, limitations, source URL, and verification date in the project's capability registry. Classify operations as PUBLIC_API, INTERNAL_OR_ASK_AI_ONLY, BROWSER_FALLBACK, or UNKNOWN. Do not invent endpoints or infer public support from private network calls.
- For UI-only work, use an available authorized browser tool and its current documentation. A skill or API token does not grant browser access. If no browser control is available, report that specific blocker and prepare the brief/copy locally; do not claim completion.
- Preserve the requested experiment. For an image comparison, keep primary text, headline, description, CTA, form, audience, placements, and budget structure identical. Assign one image per ad. A shared-budget comparison does not prove equal spend or randomized A/B allocation.
- For Ben/Growth Factor, the established placement preference is manual Facebook and Instagram feeds, stories, and reels. Confirm ambiguous placement labels against the current UI. This preference does not supply another client's audience, budget, destination, or launch authorization.
- Default unrequested launches to drafts. An explicit draft-only instruction prohibits Publish, enabling delivery, or scheduling launch. If launch is explicitly authorized, complete verification before that action; do not repeatedly ask for authorization already given.
- Treat edits to active campaigns as potentially immediate. Establish whether the user intends an in-place live edit or a draft copy. Capture original values and change only the requested scope.
- Save, reopen, and read back effective values. A successful click or upload invocation is not proof of persistence. Never claim lead routing, delivery, or ad performance based on a draft preview.

## Handoff

Report campaign/ad set/ad names and links, verified status, budget level and amount, audience, placements, destination, image assignment, changes, and unresolved checks. Distinguish saved configuration from delivery tests. Keep credentials, browser sessions, customer records, and private identifiers out of the reusable skill and public repository.
