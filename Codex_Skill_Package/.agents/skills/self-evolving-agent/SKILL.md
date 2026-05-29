---
name: self-evolving-agent
description: Use this skill after substantial coding, debugging, simulation, data-processing, literature, or writing tasks to reflect on the execution trace, update reusable project skills, separate skill defects from execution lapses, prune redundancy, and improve the skill-maintenance process itself.
---

# Self-Evolving Agent Skill for Codex

## Purpose

Use this skill to make Codex improve through project-level text artifacts rather than model parameter updates.

After substantial tasks, Codex must inspect the execution trajectory, identify reusable procedural knowledge, update project skills only when evidence supports it, and improve the skill-maintenance process itself.

This skill is especially useful for:

- recurring coding and debugging workflows
- Cantera and combustion simulation tasks
- reaction mechanism merging and validation
- data processing and Excel output workflows
- scientific plotting
- paper writing and revision
- prompt engineering
- long-running research projects with repeated task patterns

## Required Local Files

Maintain these files in the repository:

```text
.agent_evolution/
  SKILL_LIBRARY.md
  REFLECTION_BUFFER.md
  META_SKILL.md
  CHANGELOG.md
```

If they are missing, create them using the templates in the repository or create minimal versions.

## Core Principle

Classify evidence from each substantial task into exactly targeted categories.

### Discovery

The task reveals a new reusable workflow, check, command, file structure, validation method, debugging pattern, or domain rule.

Action: add a new skill only if it has a clear trigger condition, verification method, and likely future reuse.

### Optimization

An existing skill is valid, but the task shows a better, faster, safer, clearer, or more reproducible way to execute it.

Action: revise only the affected part of the skill body.

### Skill Defect

An existing skill is wrong, incomplete, too broad, too vague, unsafe, or misleading.

Action: revise the implicated skill body only. Preserve unaffected parts.

### Execution Lapse

The existing skill is valid, but Codex failed to follow it.

Action: do not rewrite the skill body. Add an Appendix reminder or Reflection Buffer note.

### Redundancy or Obsolescence

A skill, step, file, check, or prompt is duplicated, outdated, inefficient, or consistently unhelpful.

Action: merge, simplify, archive, or disable only when evidence is sufficient.

## Pre-Task Procedure

Before starting substantial work:

1. Read `AGENTS.md`.
2. Read this `SKILL.md`.
3. Inspect `SKILL_LIBRARY.md` and `META_SKILL.md`.
4. Select only relevant active skills.
5. State the user goal, success criteria, plan, and validation method.

Use this compact format:

```markdown
## Pre-Task Plan

### User Goal
...

### Success Criteria
...

### Relevant Existing Skills
...

### Execution Plan
...

### Validation Plan
...
```

## During Task Execution

Track internally or in notes:

- files inspected
- files modified
- commands run
- errors encountered
- failed attempts
- fixes applied
- outputs generated
- validation performed
- user corrections
- final result

Avoid long narrative unless the user asks for it.

## Validation

Before completion, run or explain the smallest reliable validation possible.

For coding tasks:

- run tests or minimal reproductions when feasible
- check imports and dependencies
- check file paths
- check output files
- check error handling
- inspect changed code for regressions

For Cantera and combustion tasks:

- verify Cantera version assumptions
- check phase name
- check species names
- check thermo and transport completeness
- check units
- check reactor type and boundary assumptions
- check convergence and physical plausibility
- save outputs with clear names when requested

For writing tasks:

- check logical flow
- check terminology consistency
- check figure/table references
- check target style
- avoid unsupported claims

## Post-Task Reflection

After substantial tasks, produce reflection records using this format:

```markdown
## Reflection ID: REF_YYYYMMDD_XXX

### Task Summary
...

### Execution Trace Summary
...

### Outcome
success / partial success / failure / uncertain

### Reflection Type
Discovery / Optimization / Skill Defect / Execution Lapse / Redundancy or Obsolescence

### Evidence
...

### Target Skill
Existing skill ID or new skill.

### Proposed Update
...

### Confidence
high / medium / low

### Decision
apply now / store in buffer / discard / wait for more evidence
```

## Skill Update Rules

When updating `SKILL_LIBRARY.md`, use:

```markdown
## Skill ID: SKILL_YYYYMMDD_XXX

### Name
...

### Domain
...

### Trigger Conditions
Use this skill when...

### Skill Body
...

### Appendix
Valid rules that Codex previously failed to follow carefully.

### Verification Method
...

### Failure Modes
...

### Evidence
...

### Credit State
- helpful_count:
- harmful_count:
- neutral_count:
- uncertain_count:

### Status
active / trial / revised / archived / disabled
```

## Credit Assignment

After each substantial task, assign credit to any skill used or considered:

```markdown
| Skill ID | Used? | Effect | Evidence | Decision |
|---|---:|---|---|---|
| SKILL_... | yes/no | helpful / harmful / neutral / uncertain | concrete evidence | keep / revise / archive / disable / need more evidence |
```

Definitions:

- helpful: improved correctness, speed, reproducibility, robustness, or clarity
- harmful: caused wrong direction, unnecessary complexity, invalid output, or wasted debugging
- neutral: used but no clear effect
- uncertain: insufficient evidence

Disable a skill only when harmful evidence is repeated and positive evidence is insufficient.

## Meta-Skill Updates

Update `META_SKILL.md` when evidence shows a recurring problem in how Codex extracts, refactors, revises, credits, filters, or validates skills.

Examples:

- too many broad skills from one case
- duplicate skill creation
- missing validation
- confusing tool limitations with agent error
- treating execution lapses as skill defects
- keeping verbose skills that are not actionable
- deleting skills that still have positive evidence

Keep at most five active meta skills per role.

## Final Output Format

```markdown
# Task Completion Report

## 1. Final Outcome
success / partial success / failure / uncertain

## 2. What Was Done
...

## 3. Validation
...

## 4. Problems Encountered
...

## 5. Skill-Aware Reflection
...

## 6. Repository Updates
Files changed or exact proposed changes.

## 7. Next Time
1 to 5 concise rules for future similar tasks.
```

## Non-Negotiable Rules

1. Do not rewrite the whole skill library without targeted evidence.
2. Do not treat every failure as a skill defect.
3. Do not treat every success as a new reusable skill.
4. Do not create broad rules from narrow evidence.
5. Do not preserve harmful skills merely because they are old.
6. Do not delete valid skills because Codex failed to follow them once.
7. Prefer concrete procedural rules over vague advice.
8. Prefer reproducible validation over subjective confidence.
9. Keep skills short, trigger-based, and testable.
10. Every update must be traceable to task evidence.
