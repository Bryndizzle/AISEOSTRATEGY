# Quick Start Guide

Get up and running with the Agent Workflow Builder in under 5 minutes.

---

## Step 1: Understand the System (2 minutes)

**Read these files in order**:
1. `README.md` - Overview and philosophy
2. `agent_system_prompt.md` - How the agent operates
3. `workflow.md` - The 9-stage execution process

**Key concept**: This system combines your 12 prompts into one workflow with minimal user input and smart assumptions.

---

## Step 2: Complete the Intake Form (3 minutes)

Open `intake_form.md` and fill in:
- **Required**: Project goal, target audience, success metrics
- **Optional**: Everything else (agent will assume)

**Example**:
```
Goal: Create email nurture sequence for product launch
Audience: Existing customers (B2B SaaS, marketing roles)
Success: 30% open rate, 5% click rate, 50 demo bookings
```

---

## Step 3: Run the Workflow

### Option A: Full Automated Run
Give the agent:
1. The completed intake form
2. Instruction: "Execute the full workflow from agent_system_prompt.md and workflow.md"
3. Wait for all 9 stages to complete

### Option B: Stage-by-Stage
Run one stage at a time, review outputs, then proceed.

### Option C: Custom Selection
Choose only the stages you need (e.g., "Run stages 1, 2, 5, and 8 only")

---

## Step 4: Review Outputs

Each stage produces a structured output. Check:
- [ ] Assumptions made (labelled clearly)
- [ ] Deliverables match your needs
- [ ] Quality meets standards
- [ ] Next steps are actionable

---

## Step 5: Integrate Your Prompts

Use `templates/prompt_integration_template.md` to map your 12 existing prompts into the workflow stages.

**Process**:
1. List all 12 prompts
2. Identify which stage each belongs to
3. Merge similar prompts
4. Add custom stages if needed
5. Test the integrated workflow

---

## Common Workflows

### Content Strategy
Stages: 1, 2, 3, 5, 8, 9

### Campaign Planning
Stages: 1, 2, 4, 5, 7, 8

### Full Execution
All stages: 0-9

### Quick Brief
Stages: 0, 1, 2, 9

---

## Troubleshooting

**Agent makes wrong assumptions?**
→ Provide more detail in intake form or correct the assumption when flagged

**Output too generic?**
→ Add specifics to "Additional Context" in intake form

**Workflow doesn't fit your use case?**
→ Create custom stages using the template in workflow.md

**Need to skip stages?**
→ Tell the agent which stages to skip and why

---

## Examples

See `examples/` folder for:
- Completed intake form
- Stage 0 output with assumptions
- Full workflow execution

---

## Next Steps

1. **Test it**: Run a simple project through the workflow
2. **Customise it**: Integrate your 12 prompts
3. **Refine it**: Adjust stages based on your needs
4. **Scale it**: Use for all similar projects

---

## Support

- Check `templates/` for reusable components
- Review `examples/` for real-world usage
- Modify `config.json` for workflow settings
