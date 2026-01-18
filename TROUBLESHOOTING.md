# Troubleshooting Guide

Common issues and solutions when using the Agent Workflow Builder.

---

## Issue 1: Agent Makes Too Many Assumptions

**Symptoms**:
- Outputs don't match expectations
- Agent assumes wrong context
- Results feel generic

**Solutions**:
1. **Provide more detail in intake form**
   - Fill optional sections
   - Add specific examples
   - Include relevant background

2. **Set stricter assumption limits**
   - In `config.json`, reduce `max_assumptions_before_confirmation`
   - Add fields to `critical_fields` array

3. **Review assumptions at Stage 0**
   - Check all assumptions before proceeding
   - Correct any that are wrong
   - Re-run if needed

**Example Fix**:
```json
// config.json
"assumptions": {
  "max_assumptions_before_confirmation": 1,  // Changed from 3
  "critical_fields": [
    "project_goal",
    "target_audience",
    "success_metrics",
    "constraints"  // Added
  ]
}
```

---

## Issue 2: Outputs Are Too Generic

**Symptoms**:
- Content lacks specificity
- Recommendations are vague
- Feels like template text

**Solutions**:
1. **Add examples to intake form**
   - Show what good looks like
   - Provide competitor examples
   - Include brand voice samples

2. **Request specific output format**
   - Specify exact deliverable structure
   - Request numbers/data where possible
   - Ask for concrete examples

3. **Strengthen Stage 1 analysis**
   - Add audience research
   - Include competitive context
   - Define unique positioning clearly

**Example Fix**:
```markdown
## Additional Context
Include 2-3 examples of content we like:
- [Example 1]: [Why it works]
- [Example 2]: [Why it works]

Our brand voice is: [Specific descriptors with examples]
Avoid these patterns: [Specific things to avoid]
```

---

## Issue 3: Agent Skips Important Steps

**Symptoms**:
- Missing deliverables
- Incomplete outputs
- Jumps to conclusions

**Solutions**:
1. **Explicitly list required deliverables**
   - In intake form, specify exactly what you need
   - Reference workflow stages by number
   - Set clear success criteria

2. **Enable quality gates**
   - In `config.json`, set `quality_gates.enabled: true`
   - Add stages to `require_user_confirmation`

3. **Run stages individually**
   - Don't run full workflow at once
   - Review each stage output
   - Confirm before proceeding

**Example Fix**:
```markdown
## Required Deliverables
1. Strategic brief (Stage 1)
2. Content framework (Stage 2)
3. 10 article outlines (Stage 5)
4. Content calendar (Stage 4)
5. Distribution plan (Stage 8)

All must be complete - no placeholders.
```

---

## Issue 4: Workflow Takes Too Long

**Symptoms**:
- Hours to complete
- Too many stages
- Overwhelming output

**Solutions**:
1. **Skip unnecessary stages**
   - Identify which stages you actually need
   - Use scenario guides in `USAGE_SCENARIOS.md`
   - Run minimal viable workflow

2. **Reuse previous outputs**
   - If strategic context hasn't changed, skip Stage 1
   - Use existing frameworks, skip Stage 2
   - Build library of reusable components

3. **Batch similar work**
   - Run Stages 0-2 once per project type
   - Run only Stages 5-7 for individual pieces
   - Create templates from repeated patterns

**Example Fix**:
```
For regular blog posts on same topic:
- Run Stages 0,1,2,3 ONCE → Save as template
- For each post: Run Stages 5,6,7 only (15 min)
```

---

## Issue 5: Conflicting Requirements

**Symptoms**:
- Agent flags contradictions
- Can't satisfy all constraints
- Outputs compromise too much

**Solutions**:
1. **Prioritise requirements**
   - Mark constraints as "must have" vs "nice to have"
   - Specify which takes precedence
   - Accept trade-offs explicitly

2. **Resolve conflicts upfront**
   - Address contradictions in intake form
   - Make decisions before workflow starts
   - Document reasoning

3. **Split into multiple workflows**
   - If requirements truly conflict, they might be different projects
   - Run separate workflows for different goals

**Example Fix**:
```markdown
## Constraints (Prioritised)
1. MUST: Stay under £5k budget [Non-negotiable]
2. MUST: Launch by March 1st [Non-negotiable]
3. NICE TO HAVE: Include video content [Skip if conflicts with 1 or 2]
4. NICE TO HAVE: 10 pieces of content [Reduce to 5 if needed]

If conflicts arise, priorities are: Budget > Timeline > Scope
```

---

## Issue 6: Agent Gets Stuck

**Symptoms**:
- Asks for information already provided
- Can't proceed without input
- Loops on same question

**Solutions**:
1. **Check input clarity**
   - Ensure answer was in intake form
   - Verify it was clear and unambiguous
   - Restate in different words if needed

2. **Provide decision rule**
   - Give agent permission to decide
   - Set default approach
   - Specify fallback option

3. **Skip problematic stage**
   - If stuck on Stage X, skip it
   - Note it as blocker
   - Proceed with rest of workflow

**Example Fix**:
```markdown
If you encounter missing information or unclear requirements:
1. Make your best assumption based on [criteria]
2. Label it clearly
3. Proceed - don't get stuck

Default approach when unclear: [Describe preferred method]
```

---

## Issue 7: Wrong Tone/Style

**Symptoms**:
- Too formal/informal
- Wrong vocabulary
- Doesn't match brand

**Solutions**:
1. **Update system prompt**
   - Modify `agent_system_prompt.md`
   - Add specific tone guidelines
   - Include example phrases

2. **Provide voice samples**
   - In intake form, add existing content examples
   - Specify do's and don'ts
   - Reference style guide

3. **Review in Stage 6**
   - Make optimisation stage focus on tone
   - Check against brand voice
   - Refine before final delivery

**Example Fix**:
```markdown
## Tone Requirements
- Use UK English (organisation, not organization)
- Conversational but professional
- Active voice, short sentences
- Avoid: corporate jargon, buzzwords, hype
- Include: specific examples, data, practical tips

Good example: "This approach cut costs by 30% in 3 months"
Bad example: "Leverage synergies to optimise operational excellence"
```

---

## Issue 8: Integration Problems (12 Prompts)

**Symptoms**:
- Prompts don't fit workflow stages
- Functionality gaps or overlaps
- Sequential dependencies broken

**Solutions**:
1. **Use integration checklist**
   - Follow `INTEGRATION_CHECKLIST.md` systematically
   - Map each prompt carefully
   - Document decisions

2. **Create custom stages**
   - Add stages between existing ones (e.g., 3.5)
   - Define purpose and output clearly
   - Update `config.json`

3. **Merge similar prompts**
   - Consolidate overlapping functionality
   - Extract unique value from each
   - Create combined instruction set

**Example Fix**:
```markdown
## Custom Stage 5.5: SEO Optimisation
**Purpose**: Apply SEO best practices to content from Stage 5
**Prompts integrated**: [SEO audit prompt] + [Keyword research prompt]
**Process**:
1. Analyse content for SEO opportunities
2. Identify target keywords
3. Optimise titles, headings, meta
4. Check readability and structure
**Output**: SEO-optimised version of Stage 5 content
```

---

## Issue 9: Inconsistent Quality

**Symptoms**:
- Some outputs great, others poor
- Quality varies by stage
- Unpredictable results

**Solutions**:
1. **Add quality criteria per stage**
   - Define what "good" looks like
   - Create checklist for each stage
   - Include examples of quality outputs

2. **Enable validation stages**
   - Always run Stage 7 (Validation & Testing)
   - Set up peer review
   - Check against success metrics

3. **Iterate on weak stages**
   - Identify which stages produce poor outputs
   - Run them twice with refinement
   - Update instructions in `workflow.md`

**Example Fix**:
```markdown
## Stage 5 Quality Criteria
Before marking Stage 5 complete, verify:
- [ ] Addresses all points from Stage 3 architecture
- [ ] Follows framework from Stage 2
- [ ] Written in specified tone/style
- [ ] Includes specific examples (not generic)
- [ ] No placeholders or "TBD" sections
- [ ] Meets length requirements (if specified)
- [ ] Actionable for target audience
```

---

## Issue 10: Can't Reuse Outputs

**Symptoms**:
- Every project starts from scratch
- Reinventing the wheel
- No efficiency gains over time

**Solutions**:
1. **Build template library**
   - Save successful workflow outputs
   - Create reusable stage templates
   - Document common patterns

2. **Create project types**
   - Define standard workflows for recurring work
   - Pre-fill intake forms for each type
   - Skip stages that don't change

3. **Extract reusable components**
   - Save good strategic analyses
   - Keep framework definitions
   - Build component library

**Example Fix**:
```
Create templates/content_campaign/ folder:
- intake_template.md (pre-filled with common info)
- stage1_strategic_template.md (standard analysis)
- stage2_framework_template.md (proven framework)

For new campaign:
1. Copy templates
2. Customise specific details
3. Run Stages 3-9 only (saves 40% time)
```

---

## Prevention Tips

### Before Starting:
- [ ] Read relevant documentation
- [ ] Choose appropriate scenario
- [ ] Fill intake form completely
- [ ] Set clear success criteria

### During Execution:
- [ ] Review assumptions at Stage 0
- [ ] Check each stage output
- [ ] Flag issues immediately
- [ ] Don't skip quality gates

### After Completion:
- [ ] Document what worked/didn't
- [ ] Save successful outputs as templates
- [ ] Update workflow based on learnings
- [ ] Build library of reusable components

---

## Getting Help

If still stuck:
1. **Review examples**: Check `examples/` folder
2. **Check templates**: Review `templates/` folder
3. **Read scenarios**: See `USAGE_SCENARIOS.md`
4. **Simplify**: Try with fewer stages/simpler project
5. **Start over**: Sometimes easier than debugging

---

## Common Misconceptions

**"Agent should know my business"**
→ Provide context in intake form, agent can't read minds

**"More stages = better output"**
→ Only run stages you need, quality > quantity

**"Assumptions are failures"**
→ Assumptions are features, they enable speed

**"Workflow must be followed exactly"**
→ Customise to your needs, it's a framework not rules

**"One workflow fits all projects"**
→ Different scenarios need different stage combinations
