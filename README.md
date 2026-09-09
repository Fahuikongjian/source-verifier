# Source Verifier

A Codex skill for choosing reliable, authoritative sources during web research.

Source Verifier makes Codex evaluate evidence claim by claim. It favors original records, checks freshness and scope, detects circular sourcing, asks for independent corroboration when stakes are high, and reports uncertainty when the evidence is weak.

## Why this exists

Domain allowlists age badly, and no website is authoritative about every subject. An official product page may be the best source for current specifications and a poor source for an impartial comparison. This skill uses a small evidence workflow instead of assigning permanent trust scores to websites.

## Install

Clone this repository into your Codex skills directory:

```powershell
git clone https://github.com/Fahuikongjian/source-verifier "$env:USERPROFILE/.codex/skills/source-verifier"
```

Restart Codex, then invoke it directly:

```text
Use $source-verifier to compare the security claims of these two products.
```

Codex may also select the skill automatically for research and fact-checking tasks.

## What it checks

- whether a source supports the exact claim being made;
- proximity to original evidence;
- relevant authority and identifiable authorship;
- methods, data, scope, and limitations;
- publication date and superseding material;
- conflicts of interest and independence;
- whether corroborating sources have separate evidence chains.

The skill does not promise that every conclusion is true. It makes evidence selection explicit, reduces common sourcing failures, and requires uncertainty to be disclosed.

## Repository layout

```text
source-verifier/
├── SKILL.md
├── agents/openai.yaml
└── references/evaluation-rubric.md
```

## Contributing

Issues and pull requests are welcome. Please propose rules that improve decisions across realistic research tasks rather than rules tailored to a single website or incident.

## License

MIT

