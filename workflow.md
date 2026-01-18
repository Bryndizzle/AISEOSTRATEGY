# Agent Workflow: Step-by-Step Execution

## Overview

This workflow consolidates 12 specialist prompts into sequential stages. Execute them in order, producing clear outputs at each stage.

---

## Stage 0: Intake & Validation

**Purpose**: Confirm understanding and document assumptions

**Input**: Completed intake form

**Process**:
1. Review all provided information
2. Identify gaps in information
3. List all assumptions being made
4. Confirm understanding with user

**Output**:
```markdown
### Confirmed Details
- [List provided information]

### Assumptions Made
- [ASSUMPTION: Detail what you're assuming and why]
- [ASSUMPTION: ...]

### Ready to Proceed
[Yes/No - await user confirmation if major assumptions made]
```

---

## Stage 1: Strategic Analysis

**Purpose**: Understand the landscape and position

**Input**: Validated intake information

**Process**:
1. Analyse target audience needs and pain points
2. Identify market context and competitive landscape
3. Map success criteria to strategic approach
4. Highlight opportunities and risks

**Output**:
```markdown
### Audience Profile
- [Key characteristics]
- [Primary needs]
- [Pain points]

### Strategic Position
- [Market context]
- [Competitive angle]
- [Unique value]

### Opportunities & Risks
- Opportunities: [List]
- Risks: [List]
```

---

## Stage 2: Framework Definition

**Purpose**: Establish structure and approach

**Input**: Strategic analysis

**Process**:
1. Define core framework/methodology to use
2. Establish key principles and guidelines
3. Set structural boundaries
4. Identify required components

**Output**:
```markdown
### Framework
- [Name and description of approach]

### Core Principles
1. [Principle]
2. [Principle]
3. [Principle]

### Required Components
- [Component]: [Purpose]
- [Component]: [Purpose]
```

---

## Stage 3: Content Architecture

**Purpose**: Design the structure and flow

**Input**: Framework definition

**Process**:
1. Create high-level content structure
2. Define information hierarchy
3. Map user journey or narrative flow
4. Identify key sections and their purpose

**Output**:
```markdown
### Content Structure
1. [Section]: [Purpose]
   - [Sub-section]
   - [Sub-section]
2. [Section]: [Purpose]
   - [Sub-section]

### Narrative Flow
[Describe the journey/progression]

### Key Touchpoints
- [Critical moment]: [Action/Message]
```

---

## Stage 4: Detailed Planning

**Purpose**: Break down execution into actionable tasks

**Input**: Content architecture

**Process**:
1. List all required deliverables
2. Identify dependencies
3. Prioritise tasks
4. Estimate complexity (simple/moderate/complex)

**Output**:
```markdown
### Deliverables
- [ ] [Item]: [Complexity] - [Dependencies]
- [ ] [Item]: [Complexity] - [Dependencies]

### Execution Order
1. [Task group]
2. [Task group]

### Critical Path
[Highlight must-complete items]
```

---

## Stage 5: Core Content Creation

**Purpose**: Develop primary content/deliverables

**Input**: Detailed planning

**Process**:
1. Create core content following the architecture
2. Ensure alignment with framework principles
3. Address target audience needs directly
4. Maintain consistent tone and style

**Output**:
```markdown
### Primary Deliverable
[The main content/document/output]

### Supporting Elements
- [Element]
- [Element]

### Quality Check
- Framework alignment: [✓/✗]
- Audience relevance: [✓/✗]
- Tone consistency: [✓/✗]
```

---

## Stage 6: Optimisation & Enhancement

**Purpose**: Refine and strengthen the output

**Input**: Core content

**Process**:
1. Review against success criteria
2. Identify weak points or gaps
3. Enhance clarity and impact
4. Remove redundancy

**Output**:
```markdown
### Improvements Made
- [Area]: [Change and reason]
- [Area]: [Change and reason]

### Remaining Gaps
- [Gap]: [Recommendation]

### Optimised Deliverable
[Enhanced version or diff from Stage 5]
```

---

## Stage 7: Validation & Testing

**Purpose**: Verify quality and fitness for purpose

**Input**: Optimised content

**Process**:
1. Check against all success metrics
2. Test with audience perspective
3. Verify constraint compliance
4. Identify any risks or issues

**Output**:
```markdown
### Success Metrics Review
- [Metric]: [Status and evidence]
- [Metric]: [Status and evidence]

### Audience Validation
- [Does it solve their problem?]
- [Is it accessible/usable?]

### Constraints Check
- [Constraint]: [Compliant ✓/✗]

### Issues Flagged
- [Issue]: [Severity] - [Recommendation]
```

---

## Stage 8: Implementation Guidance

**Purpose**: Provide clear next steps for execution

**Input**: Validated output

**Process**:
1. List immediate next actions
2. Identify required resources
3. Highlight potential blockers
4. Suggest success tracking methods

**Output**:
```markdown
### Immediate Next Steps
1. [Action]: [Who/What/When]
2. [Action]: [Who/What/When]

### Resources Required
- [Resource]: [Purpose]

### Potential Blockers
- [Blocker]: [Mitigation strategy]

### Tracking & Measurement
- [How to monitor success metrics]
```

---

## Stage 9: Documentation & Handoff

**Purpose**: Package everything for delivery

**Input**: All previous stage outputs

**Process**:
1. Compile all deliverables
2. Create executive summary
3. Document decisions and rationale
4. Provide usage instructions

**Output**:
```markdown
### Executive Summary
[2-3 paragraph overview]

### Deliverables Package
- [Item]: [Location/Format]
- [Item]: [Location/Format]

### Key Decisions Log
- [Decision]: [Rationale]

### Usage Instructions
[How to use/implement the deliverables]
```

---

## Workflow Customisation

### Skip Stages
If a stage doesn't apply, document why and skip:
```
**Stage [X]: [Name]** - SKIPPED
Reason: [Explanation]
```

### Add Stages
Insert custom stages as needed:
```
**Stage [X.5]: [Custom Stage]**
Purpose: [Why this is needed]
[Standard stage structure]
```

### Parallel Execution
Some stages can run in parallel if independent:
- Stages 5 & 7 (if testing prototype)
- Stages 2 & 3 (if framework is predetermined)

---

## Quality Gates

Before proceeding to next stage, ensure:
- [ ] Current stage output is complete
- [ ] Output meets quality standards
- [ ] Dependencies for next stage are met
- [ ] No blocking issues remain

---

## Emergency Procedures

**If stuck**:
1. Document the blocker clearly
2. List what you've tried
3. Ask specific question
4. Don't proceed blindly

**If requirements conflict**:
1. Flag the conflict explicitly
2. Present options with trade-offs
3. Recommend preferred approach
4. Await user decision
