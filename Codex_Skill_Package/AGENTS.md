# AGENTS.md

## Repository-Level Self-Evolving Agent Instructions

Before doing substantial work in this repository, read and follow:

- `.agents/skills/self-evolving-agent/SKILL.md`
- `.agent_evolution/SKILL_LIBRARY.md`
- `.agent_evolution/META_SKILL.md`
- `.agent_evolution/REFLECTION_BUFFER.md` when relevant

Use only relevant active skills. Do not overload the prompt with unrelated historical notes.

## Working Protocol

1. Clarify the user goal and success criteria.
2. Identify relevant existing skills.
3. Make a concise execution plan and validation plan.
4. Execute the task.
5. Validate before claiming completion.
6. Produce a compact task completion report.
7. Update the `.agent_evolution/` files when evidence supports a targeted update.

## Files to Maintain

- `.agent_evolution/SKILL_LIBRARY.md`
- `.agent_evolution/REFLECTION_BUFFER.md`
- `.agent_evolution/META_SKILL.md`
- `.agent_evolution/CHANGELOG.md`

## Update Rules

- Do not rewrite the whole skill library.
- Do not create broad skills from narrow evidence.
- Do not treat every failure as a skill defect.
- Do not delete a valid skill because Codex failed to follow it once.
- If the skill is valid but Codex ignored it, update the Appendix or Reflection Buffer only.
- Archive or disable a skill only with repeated harmful evidence and insufficient helpful evidence.
- Every accepted update must be recorded in CHANGELOG.md.

## Validation Expectations

For code tasks, run or explain the smallest reliable validation possible. Check imports, paths, outputs, errors, and regressions.

For Cantera or mechanism tasks, check mechanism loading, phase names, species names, thermo and transport consistency, units, reactor assumptions, convergence, and physical plausibility.

For data and plotting tasks, check row counts, units, missing values, figure labels, font size, overlap, output files, and reproducibility.

For writing tasks, check logic, terminology consistency, figure and table references, unsupported claims, and target style.
