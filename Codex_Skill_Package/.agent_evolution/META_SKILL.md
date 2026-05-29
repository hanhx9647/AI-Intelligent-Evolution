# Meta Skill

This file stores rules about how the agent should improve the skill-evolution process itself.

Meta skills optimize how future skills are extracted, refactored, refined, credited, filtered, and validated.

Keep at most five active meta skills per role. Archive weaker or redundant rules.

---

## Active Meta Skills Index

| Meta Skill ID | Role Affected | Status | Last Updated |
|---|---|---|---|

---

## Meta Skill Template

```markdown
## Meta Skill ID: META_YYYYMMDD_XXX

### Role Affected
extractor / refactorer / refiner / credit assigner / filter / prompt designer / validator.

### Meta Rule
A concise rule for improving how future skills are extracted, revised, filtered, or validated.

### Evidence
Which previous task patterns support this meta rule?

### Scope
When this meta rule applies.

### Risk
When this meta rule may be harmful.

### Status
active / trial / archived.
```

---

## Initial Meta Skills

## Meta Skill ID: META_INITIAL_001

### Role Affected
extractor

### Meta Rule
Do not create a new reusable skill from a single accidental success unless the trigger condition, verification method, and future reuse scenario are clear.

### Evidence
Initial operating rule.

### Scope
All task domains.

### Risk
May delay skill creation when a strong one-shot case is clearly generalizable.

### Status
active

## Meta Skill ID: META_INITIAL_002

### Role Affected
refiner

### Meta Rule
When a skill causes over-application, first narrow its trigger condition before deleting the whole skill.

### Evidence
Initial operating rule.

### Scope
Reusable workflow and domain-rule skills.

### Risk
If the skill is fundamentally wrong, narrowing may preserve a harmful rule too long.

### Status
active

## Meta Skill ID: META_INITIAL_003

### Role Affected
credit assigner

### Meta Rule
Separate skill defects from execution lapses, tool/environment limitations, user ambiguity, and missing validation.

### Evidence
Initial operating rule.

### Scope
All post-task reflections.

### Risk
May classify ambiguous failures as uncertain and require additional evidence.

### Status
active

## Meta Skill ID: META_INITIAL_004

### Role Affected
validator

### Meta Rule
Every coding, data-processing, simulation, or plotting skill must include a minimal validation method.

### Evidence
Initial operating rule.

### Scope
Code, numerical simulation, data analysis, plotting, Cantera, and mechanism work.

### Risk
May add overhead to very small tasks.

### Status
active
