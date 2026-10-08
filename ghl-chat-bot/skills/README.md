# Growth Factor GHL skills

Four portable instruction skills, separate from credentials, customer history,
and the implementation of the API client.

| Skill | Use |
| --- | --- |
| ghl-agent-build | Build the appropriate GHL product or an API framework milestone |
| ghl-agent-test | Reproduce and grade historical or synthetic conversations |
| ghl-agent-optimize | Fix existing prompt behavior and verify the improvement |
| ghl-agent-actions | Configure or simplify workflows, handovers and followups |

Build supports Conversation AI, Agent Studio, and Voice AI as distinct products.
It does not claim that this repository's client already implements every product.
Agent purpose and business rules belong in tenant profiles. Fighters Boxing rules
are examples of one tenant, never defaults for another gym or business.

## Install and use

Each named folder contains its own SKILL.md. For Codex personal installation, copy
the four named folders into the skills directory under CODEX_HOME, or
`C:\Users\YOUR_NAME\.codex\skills` when CODEX_HOME is unset. Do not overwrite an
existing customized skill without comparing it first. Load a new session if needed.

Other agent tools may accept these Markdown instructions, but use their documented
skill installation path and supported tools. A skill does not provide credentials,
GitHub permission, browser access, or a HighLevel connector.

Example requests:

- Use $ghl-agent-build to build a Conversation AI appointment setter for the supplied tenant, starting with account verification only.
- Use $ghl-agent-test to test this copied bot against 20 historical conversations and five pricing-pressure scenarios.
- Use $ghl-agent-optimize to remove verbose dates and unsolicited class descriptions, then replay the attached conversation.
- Use $ghl-agent-actions to map manager handovers and identify which workflows built-in actions can replace. Keep existing routing until replacements are verified.

## Publish to GitHub

The pack is shared by `bendeisel/growthfactor` and `bendeisel/agent-building`.
Keep matching copies in both repositories when updating these skills. Keep this folder at
`ghl-chat-bot/skills/`. To move it through another coding agent, provide the skill
pack or local files, the repository, and a branch destination. That agent needs
repository write permissions and file/terminal or equivalent Git operations. A
read-only GitHub connector cannot push commits.

Suggested handoff request:

> Add the supplied four skills under ghl-chat-bot/skills in bendeisel/growthfactor.
> Read repository instructions, compare existing files, validate the skills, and
> scan the exact files for secrets. Commit only the skill-pack changes on a new
> branch and open a pull request. Do not include customer histories, recordings,
> results, credentials, unrelated staged changes, or enable any GHL agent.

This checkout contains other earlier changes. Avoid `git add .`, `git commit -a`,
or committing pre-existing staged files as part of a skills-only handoff. A fresh
clone/branch is simplest for another agent importing just the supplied archive.

The ZIP has a repository-relative `ghl-chat-bot/skills/` root. It excludes the GHL
framework implementation and tenant configuration. Ship those separately after
review if they are also wanted in the destination repository.
