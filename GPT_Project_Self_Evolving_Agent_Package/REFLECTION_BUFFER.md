# Reflection Buffer

This file stores raw reflection records before they are consolidated into Skill Library or Meta Skill.

Do not convert every task into a skill. Store low-confidence or single-instance observations here until repeated evidence appears.

---

## Reflection Template

```markdown
## Reflection ID: REF_YYYYMMDD_XXX

### Task Summary
What was the user trying to accomplish?

### Execution Trace Summary
Key steps taken, files changed, commands run, errors encountered, corrections made, and final result.

### Outcome
success / partial success / failure / uncertain.

### Reflection Type
Discovery / Optimization / Skill Defect / Execution Lapse / Redundancy or Obsolescence.

### Evidence
Specific observations from the task trajectory.

### Target Skill
Existing skill ID if applicable. Use "new skill" if this is a Discovery.

### Proposed Update
Concrete addition, revision, appendix reminder, archive decision, or deletion proposal.

### Confidence
high / medium / low.

### Decision
apply now / store in buffer / discard / wait for more evidence.
```
