# Implementation Report with Timeline Format

**Purpose**: Convert Byterover memories about implementations, features, or tasks into comprehensive reports with timelines.

## Structure

### 1. Executive Summary
```markdown
# [Implementation Name] - Implementation Report

**Timeline**: [Start Date] - [End Date]
**Status**: [Completed/In Progress/Blocked]
**Key Contributors**: [Names/teams if available from memories]

## Quick Summary
[2-3 sentence overview of what was implemented and why]

## Key Outcomes
- [Major outcome 1]
- [Major outcome 2]
- [Major outcome 3]
```

### 2. Context & Background
```markdown
## Background

**Problem Statement**: [Why this implementation was needed]

**Goals**:
- [Primary goal]
- [Secondary goal]
- [Additional goals]

**Scope**: [What was included and excluded]
```

### 3. Timeline Section
```markdown
## Implementation Timeline

### Phase 1: [Phase Name] ([Date Range])
**Key Activities**:
- [Activity with date if available]
- [Activity with date if available]

**Decisions Made**:
- [Decision 1 with rationale]
- [Decision 2 with rationale]

**Challenges Encountered**:
- [Challenge and how it was resolved]

### Phase 2: [Phase Name] ([Date Range])
[Repeat structure]

### Phase 3: [Phase Name] ([Date Range])
[Repeat structure]
```

### 4. Technical Details
```markdown
## Technical Implementation

### Architecture
[High-level architecture decisions and approach]

### Key Components
1. **[Component Name]**: [Description and purpose]
2. **[Component Name]**: [Description and purpose]

### Technologies Used
- [Technology 1]: [Purpose/reason]
- [Technology 2]: [Purpose/reason]

### Code References
- [Link to relevant code/files if available in memories]
```

### 5. Learnings & Outcomes
```markdown
## Learnings

### What Went Well
- [Success 1]
- [Success 2]

### Challenges & How They Were Addressed
- **[Challenge]**: [Solution and outcome]
- **[Challenge]**: [Solution and outcome]

### Key Takeaways
- [Takeaway for future implementations]
- [Takeaway for future implementations]

## Outcomes & Impact

### Metrics
- [Metric 1]: [Value/change]
- [Metric 2]: [Value/change]

### Impact
[Description of business/technical impact]
```

### 6. Next Steps & Future Considerations
```markdown
## Next Steps
- [ ] [Action item 1]
- [ ] [Action item 2]

## Future Enhancements
- [Potential improvement 1]
- [Potential improvement 2]

## Related Documentation
- <mention-page url="...">Related Implementation</mention-page>
- <mention-page url="...">Technical Spec</mention-page>
```

## Memory Extraction Guidelines

When aggregating memories for an implementation report:

1. **Search broadly** using the task/feature name and variations
2. **Look for temporal markers** in memories (dates, "started", "completed", "deployed")
3. **Identify decision points** where choices were made
4. **Extract challenges and solutions** from error/debugging memories
5. **Capture technical details** about architecture, components, technologies
6. **Find outcomes and metrics** from completion memories

## Timeline Construction

Organize memories chronologically:
- Group related memories by time period (if dates available)
- Identify distinct phases (planning, development, testing, deployment)
- Order activities within each phase logically
- Highlight key milestones and decision points

## Example Property Schema (if creating in database)

```javascript
{
  "Title": "User Authentication Implementation",
  "Type": "Implementation Report",
  "Status": "Completed",
  "Start Date": "2025-07-10",
  "End Date": "2025-07-15",
  "Team": "Backend",
  "Tags": ["authentication", "security", "backend"]
}
```
