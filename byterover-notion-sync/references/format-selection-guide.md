# Format Selection Guide

**Purpose**: Help determine which format to use when converting Byterover memories to Notion documentation.

## Decision Tree

### Question 1: What is the primary content type?

#### A. Implementation/Task Completion
**Characteristics**:
- Describes work that was done
- Has temporal progression (started → completed)
- Contains technical implementation details
- Includes challenges and solutions
- May have timeline or phases

**→ Use: [Implementation Report with Timeline](implementation-report-format.md)**

---

#### B. Product/Feature Planning
**Characteristics**:
- Describes what should be built
- Contains requirements and user stories
- Has success metrics and acceptance criteria
- Includes prioritization (must-have, should-have, nice-to-have)
- May be pre-implementation or planning stage

**→ Use: [PRD Format](prd-format.md)**

---

#### C. Feature/API Usage Guide
**Characteristics**:
- Explains how to use something
- Contains code examples and usage patterns
- Has troubleshooting information
- Includes API reference or method documentation
- Targeted at developers or end-users

**→ Use: [Feature Documentation](feature-documentation-format.md)**

---

#### D. System Design/Architecture
**Characteristics**:
- Describes system components and their interactions
- Contains architecture diagrams or design decisions
- Includes infrastructure, scaling, security considerations
- Has technical trade-offs and alternatives considered
- Documents technology choices and patterns

**→ Use: [Technical Architecture](technical-architecture-format.md)**

---

## When to Use Each Format

### Implementation Report with Timeline
**Best for**:
- Post-mortems of completed projects
- Sprint retrospectives
- Feature implementation summaries
- Migration or refactoring reports
- Incident post-mortems with timeline

**Key indicator**: Past tense, temporal sequence, "what we did"

**Example queries**:
- "Create report on user authentication implementation from July 10-15"
- "Document the database migration we completed last week"
- "Summarize the bug fix sprint with timeline"

---

### PRD (Product Requirements Document)
**Best for**:
- Feature proposals
- Product specifications
- Requirements gathering
- Scope definition
- Pre-implementation planning

**Key indicator**: Future/present tense, "what we should build", requirements

**Example queries**:
- "Create PRD for real-time collaboration feature"
- "Document requirements for notification system"
- "Turn these memories into a product spec"

---

### Feature Documentation
**Best for**:
- User guides
- API documentation
- Developer documentation
- How-to guides
- Feature usage instructions

**Key indicator**: Imperative mood, "how to use", examples and troubleshooting

**Example queries**:
- "Create documentation for the payment API"
- "Document how to use the authentication system"
- "Write user guide for the dashboard feature"

---

### Technical Architecture
**Best for**:
- System design documents
- Architecture decision records (ADRs)
- Infrastructure documentation
- High-level technical overview
- Component interaction design

**Key indicator**: System perspective, architecture diagrams, design decisions

**Example queries**:
- "Document the architecture of our microservices system"
- "Create architecture doc for the payment processing system"
- "Write up the design decisions for the new API gateway"

---

## Combining Formats

Sometimes memories span multiple formats. Consider creating multiple documents:

### Example 1: Feature from Idea to Implementation
1. **PRD** - Initial requirements and planning
2. **Technical Architecture** - System design decisions
3. **Implementation Report** - How it was built (with timeline)
4. **Feature Documentation** - How to use it

### Example 2: System Redesign
1. **Technical Architecture** (Old) - Document existing system
2. **PRD** - Requirements for new system
3. **Technical Architecture** (New) - New system design
4. **Implementation Report** - Migration process and timeline

### Example 3: API Development
1. **PRD** - API requirements and use cases
2. **Technical Architecture** - API design and infrastructure
3. **Feature Documentation** - API reference and usage guide

---

## Mixed Content Indicators

If memories contain mixed content:

| Content Mix | Primary Format | Additional Format |
|------------|---------------|-------------------|
| Requirements + Implementation | PRD | Add "Implementation" section or create separate Implementation Report |
| Architecture + Usage Guide | Technical Architecture | Add "Usage" section or create separate Feature Documentation |
| Implementation + Usage Guide | Implementation Report | Add "Using the Feature" section or create separate Feature Documentation |
| Requirements + Architecture | PRD | Add "Technical Approach" section or create separate Technical Architecture |

---

## Format Characteristics Summary

| Format | Tense | Perspective | Key Sections |
|--------|-------|-------------|--------------|
| **Implementation Report** | Past | Team/Project | Timeline, Challenges, Outcomes |
| **PRD** | Future/Present | Product/User | Requirements, User Stories, Acceptance Criteria |
| **Feature Documentation** | Imperative | User/Developer | Usage, Examples, Troubleshooting |
| **Technical Architecture** | Present | System/Technical | Components, Design Decisions, Infrastructure |

---

## Quick Selection Checklist

Use this checklist to quickly determine format:

- [ ] Does it describe **completed work with a timeline**? → Implementation Report
- [ ] Does it describe **what should be built**? → PRD
- [ ] Does it explain **how to use something**? → Feature Documentation
- [ ] Does it describe **system design and components**? → Technical Architecture

---

## Special Cases

### Case 1: Minimal Memories
If memories are sparse, start with simpler format and note gaps:
- **Few technical details**: Use PRD to capture requirements, mark technical details as TBD
- **No timeline info**: Use Feature Documentation focused on current state
- **High-level only**: Use Technical Architecture at high level, note areas needing detail

### Case 2: Multiple Topics
If memories span multiple unrelated topics:
- Create **separate documents** for each topic
- Use appropriate format for each
- Link documents together with cross-references

### Case 3: Incremental Documentation
If building documentation over time:
- Start with **PRD** during planning
- Add **Technical Architecture** during design
- Create **Implementation Report** after completion
- Develop **Feature Documentation** for users

---

## Examples

### Example 1: "Document authentication system from June"

**Analysis**:
- Past tense ("from June")
- Completed work
- Likely has implementation timeline

**Format**: Implementation Report with Timeline

---

### Example 2: "Create docs for notification feature requirements"

**Analysis**:
- Focus on requirements
- Planning/specification stage
- Not yet implemented

**Format**: PRD

---

### Example 3: "Write guide for using the search API"

**Analysis**:
- "How to use"
- User/developer focused
- Usage instructions

**Format**: Feature Documentation

---

### Example 4: "Document our microservices architecture"

**Analysis**:
- System design
- Component interactions
- Architecture decisions

**Format**: Technical Architecture
