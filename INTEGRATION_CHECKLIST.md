# Integration Checklist: Combining Your 12 Prompts

Use this checklist to systematically integrate your existing prompts into the unified workflow.

---

## Phase 1: Inventory & Analysis

- [ ] List all 12 prompts with names and descriptions
- [ ] Document what each prompt produces
- [ ] Identify input requirements for each prompt
- [ ] Note any sequential dependencies between prompts
- [ ] Flag prompts that overlap in functionality

**Output**: Prompt inventory (use `templates/prompt_integration_template.md`)

---

## Phase 2: Mapping to Workflow Stages

### For Each Prompt:

- [ ] Identify primary function (analysis, planning, creation, validation, etc.)
- [ ] Map to corresponding workflow stage (0-9)
- [ ] Note if prompt spans multiple stages
- [ ] Document any prompt that doesn't fit existing stages

### Stage Mapping Review:

- [ ] Stage 0 (Intake): Which prompts gather information?
- [ ] Stage 1 (Analysis): Which prompts analyse strategy/audience/market?
- [ ] Stage 2 (Framework): Which prompts define approach/methodology?
- [ ] Stage 3 (Architecture): Which prompts structure content/flow?
- [ ] Stage 4 (Planning): Which prompts create task lists/plans?
- [ ] Stage 5 (Creation): Which prompts generate core content?
- [ ] Stage 6 (Optimisation): Which prompts refine/improve output?
- [ ] Stage 7 (Validation): Which prompts check quality/test?
- [ ] Stage 8 (Implementation): Which prompts provide next steps?
- [ ] Stage 9 (Documentation): Which prompts package deliverables?

**Output**: Mapping document showing prompt → stage relationships

---

## Phase 3: Consolidation

### Merge Overlapping Prompts:

- [ ] Identify prompts that do similar things
- [ ] Extract unique value from each
- [ ] Combine into single stage instruction
- [ ] Ensure no functionality is lost
- [ ] Document what was merged and why

### Handle Gaps:

- [ ] Identify workflow stages with no prompts mapped
- [ ] Decide if stage is needed for your use case
- [ ] Either skip stage or create new prompt
- [ ] Document decision

### Sequence Validation:

- [ ] Verify stage order makes logical sense
- [ ] Check dependencies are in correct order
- [ ] Confirm outputs feed into next stage inputs
- [ ] Adjust sequence if needed

**Output**: Consolidated workflow with integrated prompts

---

## Phase 4: Customisation

### Custom Stages (if needed):

- [ ] Identify unique prompt functions not in standard workflow
- [ ] Create custom stage number (e.g., 5.5)
- [ ] Define purpose, process, and output format
- [ ] Insert at correct position in sequence

### Stage Modifications:

- [ ] Adapt stage outputs to match your needs
- [ ] Modify process steps if required
- [ ] Update quality gates
- [ ] Adjust tone/style to your brand

### Configuration:

- [ ] Update `config.json` with your settings
- [ ] Enable/disable stages as needed
- [ ] Set assumption thresholds
- [ ] Configure output formats

**Output**: Customised workflow tailored to your use case

---

## Phase 5: Testing

### Test Run 1: Simple Project

- [ ] Choose straightforward test case
- [ ] Complete intake form
- [ ] Run full workflow
- [ ] Check each stage output
- [ ] Note what worked and what didn't

### Test Run 2: Complex Project

- [ ] Choose realistic, complex case
- [ ] Include edge cases and constraints
- [ ] Execute workflow
- [ ] Verify all prompts were used
- [ ] Check output quality

### Refinement:

- [ ] Adjust stage instructions based on test results
- [ ] Fix any broken dependencies
- [ ] Clarify ambiguous instructions
- [ ] Add examples where helpful

**Output**: Tested, refined workflow ready for production

---

## Phase 6: Documentation

### Create Usage Guide:

- [ ] Document when to use which stages
- [ ] Provide examples for common scenarios
- [ ] List customisation options
- [ ] Add troubleshooting tips

### Update System Prompt:

- [ ] Ensure agent knows all integrated prompts
- [ ] Update role/boundaries if needed
- [ ] Add domain-specific guidance
- [ ] Include quality standards

### Template Library:

- [ ] Create output templates for each stage
- [ ] Add examples of good outputs
- [ ] Provide intake form variations
- [ ] Build reusable components

**Output**: Complete documentation package

---

## Phase 7: Launch

### Preparation:

- [ ] Final review of all workflow stages
- [ ] Confirm config.json is correct
- [ ] Test with team members (if applicable)
- [ ] Create backup of working version

### Rollout:

- [ ] Run first production project
- [ ] Monitor outputs closely
- [ ] Collect feedback
- [ ] Make iterative improvements

### Maintenance:

- [ ] Document learnings from usage
- [ ] Update workflow based on feedback
- [ ] Add new examples
- [ ] Version control changes

**Output**: Live, production-ready workflow

---

## Success Criteria

You've successfully integrated when:

- [ ] All 12 prompts are represented in the workflow
- [ ] No functional overlap or duplication
- [ ] Sequential flow is logical and efficient
- [ ] Outputs are consistent and high-quality
- [ ] Agent can execute without getting stuck
- [ ] Users can complete intake form easily
- [ ] Assumptions are clear and sensible
- [ ] Deliverables meet your standards
- [ ] Workflow is reusable across projects
- [ ] Documentation is clear and complete

---

## Common Pitfalls to Avoid

- **Over-complication**: Don't add stages you don't need
- **Under-specification**: Don't leave too much to assumption
- **Rigid structure**: Allow flexibility for edge cases
- **Poor sequencing**: Ensure dependencies are in order
- **Vague outputs**: Define clear deliverable formats
- **Skipping testing**: Always test before production use
- **No documentation**: Future you will thank present you

---

## Need Help?

If you get stuck:
1. Review examples in `examples/` folder
2. Check templates in `templates/` folder
3. Re-read `workflow.md` for stage guidance
4. Start with fewer prompts and build up
5. Test each integration step before proceeding
