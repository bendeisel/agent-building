---
name: ghl-agent-optimize
description: Diagnose and fix an existing HighLevel agent's prompt or response behavior from transcripts, screenshots, and owner feedback, then retest the change. Use for GHL tone, brevity, date formatting, booking dialogue, and policy compliance fixes.
---

# Optimize a GHL agent

Identify the tenant, agent product, designated copy, and exact reported failure.
Read the current saved prompt and relevant actions, not just an old local export.
Preserve a before snapshot and detect concurrent changes before writing. Never
silently modify the original, deployment mode, knowledge source, or unrelated action.

## Diagnose the cause

Map the bad response to prompt instructions, knowledge, action final messages,
calendar configuration, or missing business policy. An action's fixed closing text
can override carefully written prompt text. Conflicting booking instructions can
repeat age questions even when the main prompt says to assume an adult.

Treat screenshots and recordings as evidence, not new authorization. Describe
whether video review covered sampled frames, audio, or both. Ask only for missing
business facts that materially affect the fix; continue independent work meanwhile.
Keep provisional owner rules labeled and scoped to that tenant.

## Make a focused revision

Translate feedback into concrete behavior and examples. Remove conflicting or
redundant instructions instead of indefinitely appending exceptions. Preserve safety,
eligibility, opt-out, truthful completion, and routing requirements in the task.

Examples when requested by the owner:
- Remove a minimum word count; use the shortest useful reply without filler.
- Answer a booking request with the next needed choice, not an unsolicited syllabus.
- Format actual calendar results naturally, omitting month/year only when clear.
- Use example dates as formatting examples, never hardcoded availability.
- Reuse stated preferences; avoid repeating names and qualification questions.
- Keep a front-desk persona consistent without claiming to be a human if asked.

These are options, not defaults for every business. Do not invent prices, wrap
policies, age limits, promotions, staff response deadlines, or new permissions.

Verify the current official API and update the capability registry before coding
against an endpoint. Record scopes, request shape, version, limitations, URL and
date. Use PUBLIC_API for documented operations; keep INTERNAL_OR_ASK_AI_ONLY,
BROWSER_FALLBACK, and UNKNOWN separate. Prefer API writes. Do not infer write
support from undocumented fields returned by GET. Use authorized UI tooling only
for the relevant unsupported operation.

For Conversation AI, check the current fullPrompt contract: when documented as the
source of truth, updating only legacy prompt sections may not affect generation.
Preserve required fields and editor limits. Read back and compare the saved prompt,
actions, and deployment mode. Keep credentials in environment variables.

## Optimize and verify

HighLevel Prompt Optimizer is optional, not a prerequisite for every edit. Its tests
can execute real actions even with cloned agents or temporary contacts. Inspect
current warnings and connected resources before running. Use isolated resources
within authorization, and review proposed prompt diffs before applying them. Do not
call a manual edit an optimizer-generated variation.

Replay the reported exchange after saving. Add at least a relevant variation or
boundary where it could expose hardcoded examples or lost context. Capture exact
responses and action evidence. Use the available GHL testing skill when useful;
otherwise apply these checks directly, without requiring another skill to exist.

If the first fix fails, diagnose the remaining cause, make a narrow adjustment and
retest. Stop repeating the same mutation without new evidence. Report any blocker
and preserve working changes. Return actual before/after behavior, scope, failures,
and untested effects. Do not declare the entire agent production-ready from a few
style checks or send a staff announcement unless requested.
