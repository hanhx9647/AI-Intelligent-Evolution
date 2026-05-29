# Project Self-Evolving Agent Skill

## 0. Purpose

This file defines the long-term self-evolution mechanism for GPT Project conversations.

The assistant must not treat each task as isolated. After completing substantial work, it must review the execution process, identify reusable procedural knowledge, remove redundant steps, improve existing skills, and provide targeted updates to the project-level skill repository.

The goal is to make future work more accurate, reproducible, efficient, concise, and less likely to repeat the same mistakes.

---

## 1. Core Principle

The assistant must classify task evidence into five categories.

### 1. Discovery

A successful or partially successful task reveals a useful new method, workflow, command, file structure, validation method, debugging pattern, or domain rule that was not previously recorded.

### 2. Optimization

An existing skill is valid, but the latest task shows a better, faster, safer, clearer, or more reproducible way to execute it.

### 3. Skill Defect

An existing skill is wrong, incomplete, too broad, too vague, unsafe, or misleading. It caused errors, wasted steps, or poor results.

### 4. Execution Lapse

The existing skill is valid, but the assistant failed to follow it. Do not rewrite the skill body. Add an appendix reminder or a reflection-buffer note so the valid rule is followed more carefully in future tasks.

### 5. Redundancy or Obsolescence

A skill, step, file, check, prompt, or workflow has become redundant, duplicated, outdated, or consistently unhelpful. It should be merged, simplified, archived, or removed only with enough evidence.

The assistant must never rewrite the whole skill repository just because one task succeeded or failed. Every update must be targeted, evidence-based, and traceable.

---

## 2. Skill Body and Appendix Separation

Each major skill has two parts:

- Skill Body: stable procedural guidance for future execution.
- Appendix: reminders about valid rules that the assistant previously failed to follow.

Update rules:

- Discovery, Optimization, and Skill Defect may update the Skill Body.
- Execution Lapse must not update the Skill Body.
- Execution Lapse only updates Appendix or Reflection Buffer.
- Redundancy or Obsolescence may archive or merge skills only when evidence is sufficient.

---

## 3. Task Protocol

### Step 1. Read relevant skills

Before a substantial task, inspect relevant parts of:

- `SKILL_LIBRARY.md`
- `META_SKILL.md`
- `REFLECTION_BUFFER.md` when needed

Select only relevant skills.

### Step 2. Execute

Track:

- user goal
- assumptions
- files inspected
- files modified or created
- commands or methods used
- errors encountered
- failed attempts
- successful fixes
- validation results
- user corrections
- final deliverables

### Step 3. Validate

Before claiming completion, validate using task-appropriate checks.

### Step 4. Reflect

Produce structured reflections only when the task provides reliable evidence.

### Step 5. Consolidate

Before updating:

- merge duplicate reflections
- resolve contradictions
- avoid overfitting to one unusual task
- prefer narrow trigger conditions
- preserve valid existing skill content

### Step 6. Update

Use:

- `SKILL_LIBRARY.md` for accepted reusable skills
- `REFLECTION_BUFFER.md` for low-confidence or pending evidence
- `META_SKILL.md` for rules about improving the skill-evolution process
- `CHANGELOG.md` for all accepted updates

---

## 4. Credit Assignment

After each substantial task, assign credit to any skill used or considered.

```markdown
| Skill ID | Used? | Effect | Evidence | Decision |
|---|---:|---|---|---|
| SKILL_... | yes/no | helpful / harmful / neutral / uncertain | concrete evidence | keep / revise / archive / disable / need more evidence |
```

A skill should be disabled only when it has repeated harmful evidence and insufficient helpful evidence.

---

## 5. Meta-Skill Update Protocol

Update `META_SKILL.md` when the assistant finds repeated problems in how it extracts, revises, validates, or filters skills.

Examples:

- creating broad skills from one narrow case
- ignoring validation
- confusing execution lapse with skill defect
- repeatedly creating duplicate skills
- preserving long and unusable skill descriptions
- failing to separate user ambiguity from agent error
- over-pruning skills that still have positive evidence

Keep at most five active meta skills per role.

---

## 6. Final Report Format

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

## 6. Project File Updates
...

## 7. Next Time
...
```
