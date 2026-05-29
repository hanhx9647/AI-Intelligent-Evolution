# EvoSkillKit
A lightweight self-evolving skill framework for GPT Projects and Codex agents.
# EvoSkillKit

<p align="center">
  <b>A lightweight self-evolving skill framework for GPT Projects and Codex agents.</b>
</p>

## Why EvoSkillKit?

LLM agents often repeat the same mistakes across tasks because their experience is not systematically converted into reusable procedural knowledge. EvoSkillKit provides a practical skill repository and reflection protocol that allows GPT Projects and Codex agents to review task traces, extract reusable skills, refine existing workflows, and maintain meta-skills for improving the skill evolution process itself.

## Core Ideas

- Skill-aware reflection
- Targeted skill revision
- Skill body / appendix separation
- Reflection buffer
- Skill library
- Meta-skill maintenance
- Changelog-based evolution history

## Supported Environments

| Environment | Status | Folder |
|---|---|---|
| GPT Project | Supported | `gpt-project/` |
| Codex | Supported | `codex/` |
| Gemini / other agents | Planned | `examples/` |

## Quick Start

### GPT Project

1. Create a new GPT Project.
2. Paste `gpt-project/GPT_PROJECT_INSTRUCTIONS_TO_PASTE.txt` into Project Instructions.
3. Upload the files in `gpt-project/`.
4. Send the content of `GPT_PROJECT_UPLOAD_MESSAGE.txt` as the first message.

### Codex

1. Copy `codex/AGENTS.md` to your repository root.
2. Copy `codex/.agents/skills/self-evolving-agent/SKILL.md` to your repository.
3. Copy `codex/.agent_evolution/` to your repository root.
4. Send the content of `CODEX_UPLOAD_MESSAGE.txt` to Codex.

## License

MIT License.
