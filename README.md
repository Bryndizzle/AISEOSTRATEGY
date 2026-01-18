# Agent Workflow Builder

A reusable agent workflow system that combines multiple prompts into a single, streamlined execution flow.

## Purpose

This system consolidates ~12 separate prompts into ONE reusable agent workflow with:
- Clear system prompt with role and boundaries
- Minimal intake form (with smart assumptions)
- Step-by-step workflow stages
- UK English, direct tone (not corporate)

## Structure

```
├── agent_system_prompt.md    # Core agent identity and operating rules
├── intake_form.md             # Minimal questions for data collection
├── workflow.md                # Step-by-step execution stages
├── config.json                # Workflow configuration
├── examples/                  # Example outputs and use cases
└── templates/                 # Reusable template components
```

## Quick Start

1. Review `agent_system_prompt.md` - understand the agent's role
2. Complete `intake_form.md` - provide minimal required info
3. Execute `workflow.md` - follow the stages sequentially

## Philosophy

- **Minimal friction**: Ask only what's necessary
- **Smart defaults**: Make sensible assumptions, label them clearly
- **Direct communication**: UK English, clear, no corporate waffle
- **Reusable**: Works across different use cases without modification
