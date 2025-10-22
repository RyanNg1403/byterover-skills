# Notion to Byterover Memory Conversion Guide

**Purpose**: Guidelines for converting Notion pages into Byterover memories while preserving structure and maximizing knowledge capture.

## Core Principles

1. **Chunk logically**: Break content into coherent, self-contained memories
2. **Preserve structure**: Maintain hierarchical relationships and context
3. **Extract actionable knowledge**: Focus on reusable information
4. **Add context**: Include metadata about source and relationships
5. **Handle nested content**: Process child pages recursively

---

## Chunking Strategy

### Determining Chunk Boundaries

**Create separate memories for**:
- Each major section (## headings) with substantial content
- Distinct concepts or topics
- Code examples with their explanations
- Procedures or workflows
- Decision records or ADRs
- API endpoints or methods

**Keep together in one memory**:
- Closely related sub-points under a section
- Short related items (< 2 paragraphs)
- Code example + explanation
- Question + answer pairs

### Size Guidelines

- **Ideal memory size**: 200-800 words
- **Minimum**: Don't create memories < 100 words (combine with related content)
- **Maximum**: Split memories > 1500 words into logical sub-topics

---

## Conversion Process

### Step 1: Fetch Notion Page
```
Use Notion:notion-fetch to get the full page content
Review structure, headings, and nested pages
Identify major sections and topics
```

### Step 2: Analyze Structure
```
Identify:
- Main topic/purpose of the page
- Major sections (## level headings)
- Nested pages or sub-topics
- Code examples, tables, or special content
- Cross-references and links
```

### Step 3: Plan Memory Chunks
```
Create a list of planned memories:
- One memory per major section OR
- One memory per concept/topic OR
- One memory per procedure/workflow

Note: Adjust based on content density
```

### Step 4: Extract and Format
```
For each chunk:
1. Extract content with context
2. Format according to content type (see below)
3. Add source metadata
4. Store using Byterover:byterover-store-knowledge
```

### Step 5: Handle Nested Pages
```
For each nested page:
1. Fetch child page
2. Repeat conversion process
3. Add parent-child relationship context
```

---

## Memory Formatting by Content Type

### Concept/Definition Memory
```markdown
**Source**: [Page Title] - [Section Name]
**Topic**: [Concept Name]

## Definition
[Clear definition of the concept]

## Key Characteristics
- [Characteristic 1]
- [Characteristic 2]

## Examples
[Concrete examples if available]

## Related Concepts
- [Related concept 1]
- [Related concept 2]

**Notion Source**: [Page URL]
```

### Procedure/How-To Memory
```markdown
**Source**: [Page Title] - [Section Name]
**Task**: [What this procedure accomplishes]

## Prerequisites
- [Prerequisite 1]
- [Prerequisite 2]

## Steps
1. [Step 1 with details]
2. [Step 2 with details]
3. [Step 3 with details]

## Expected Outcome
[What should result from following this procedure]

## Troubleshooting
[Common issues if mentioned]

**Notion Source**: [Page URL]
```

### Code Example Memory
```markdown
**Source**: [Page Title] - [Section Name]
**Purpose**: [What this code does]

## Code
```language
[Full code example]
```

## Explanation
[Line-by-line or section-by-section explanation]

## Usage Context
[When and why to use this code]

## Related Examples
[Links to related code examples]

**Notion Source**: [Page URL]
```

### Decision/ADR Memory
```markdown
**Source**: [Page Title] - [Decision Name]
**Decision Date**: [Date if available]

## Decision
[What was decided]

## Context
[Why this decision was needed]

## Alternatives Considered
- [Alternative 1]: [Why not chosen]
- [Alternative 2]: [Why not chosen]

## Consequences
**Positive**:
- [Benefit 1]
- [Benefit 2]

**Negative**:
- [Trade-off 1]
- [Trade-off 2]

**Notion Source**: [Page URL]
```

### API/Reference Memory
```markdown
**Source**: [Page Title] - [API/Method Name]
**Signature**: [Method signature]

## Description
[What this API/method does]

## Parameters
- `[param1]` ([type]): [Description]
- `[param2]` ([type]): [Description]

## Returns
[Return type and description]

## Example Usage
```language
[Usage example]
```

## Notes
[Important notes, limitations, or considerations]

**Notion Source**: [Page URL]
```

### Architectural Component Memory
```markdown
**Source**: [Page Title] - [Component Name]
**System**: [System/Service Name]

## Purpose
[What this component does]

## Responsibilities
- [Responsibility 1]
- [Responsibility 2]

## Interfaces
**Inputs**: [What it receives]
**Outputs**: [What it produces]

## Technologies
[Technologies/frameworks used]

## Interactions
[How it interacts with other components]

**Notion Source**: [Page URL]
```

---

## Structure Preservation

### Handling Headings

**Top-level heading (#)**:
- Create a summary memory for the overall page
- Include page purpose and overview

**Section headings (##)**:
- Each becomes a separate memory (if substantial)
- Include section context in memory

**Subsection headings (###)**:
- Keep within parent section memory
- Use as structure within the memory

### Handling Lists

**Bulleted/Numbered Lists**:
- Preserve formatting in memory
- If list is very long (>10 items), consider splitting by topic

**Task Lists**:
- Convert to action items or procedures
- Preserve completion status if relevant

### Handling Tables

**Small Tables** (<5 rows):
- Include directly in memory using markdown

**Large Tables** (>5 rows):
- Summarize key points
- Note: "Full table available in Notion source"

**Schema Tables**:
- Include full table as it's reference material

### Handling Code Blocks

**Always include**:
- Full code with proper formatting
- Language specification
- Inline comments from original

**Add**:
- High-level explanation before code
- Usage context after code

### Handling Callouts/Quotes

**Callouts**:
- Convert to "Note:", "Warning:", "Tip:" prefixes
- Preserve content and emphasis

**Quotes**:
- Preserve as blockquotes
- Include attribution if available

---

## Nested Page Handling

### Strategy

For pages with nested/child pages:

1. **Fetch parent page first**
2. **Identify child pages** (look for `<page>` tags)
3. **For each child page**:
   - Fetch full content
   - Convert using same process
   - Add parent context to memories
4. **Create relationship memories** if needed

### Parent-Child Context

In child page memories, add:
```markdown
**Parent Topic**: [Parent Page Title]
**Context in Parent**: [How this relates to parent]
```

In parent page memories, add:
```markdown
**Related Sub-Topics**:
- [Child page 1]: [Brief description]
- [Child page 2]: [Brief description]
```

---

## Special Content Types

### Meeting Notes
```markdown
**Source**: [Page Title]
**Meeting Date**: [Date]
**Participants**: [If listed]

## Summary
[Key takeaways]

## Decisions Made
- [Decision 1]
- [Decision 2]

## Action Items
- [Action 1]
- [Action 2]

## Discussion Points
[Key discussion topics and outcomes]

**Notion Source**: [Page URL]
```

### Database Pages

When converting pages from Notion databases:

1. **Include properties** as metadata:
```markdown
**Source**: [Database Name] - [Page Title]
**Properties**:
- Status: [Value]
- Priority: [Value]
- Tags: [Values]
```

2. **Convert page content** as usual
3. **Add database context** to understand categorization

---

## Metadata and Traceability

### Always Include

In every memory:
```markdown
**Notion Source**: [Full page URL]
**Page Title**: [Original title]
**Section**: [Section name if applicable]
**Last Updated**: [Notion last-edited date if available]
```

### Optional Metadata

Add when relevant:
```markdown
**Authors**: [If listed in page]
**Tags**: [Relevant categorization]
**Related Pages**: [Links to related Notion pages]
**Version**: [If versioned documentation]
```

---

## Quality Checks

Before storing memories, verify:

- [ ] Memory is self-contained and understandable
- [ ] Context from parent page/section is included
- [ ] Code examples are complete and formatted
- [ ] Source URL is included
- [ ] Memory size is reasonable (200-800 words ideal)
- [ ] Technical terms are preserved
- [ ] Structure (headings, lists, code) is maintained
- [ ] Cross-references are preserved or noted

---

## Example Conversion

### Original Notion Content
```markdown
# API Authentication

Our API uses JWT tokens for authentication.

## Getting a Token

To get a token, send a POST request to `/auth/login`:

```javascript
fetch('/auth/login', {
  method: 'POST',
  body: JSON.stringify({ username, password })
})
```

## Using the Token

Include the token in the Authorization header:

```javascript
fetch('/api/data', {
  headers: { 'Authorization': `Bearer ${token}` }
})
```

## Token Expiration

Tokens expire after 24 hours. Handle 401 errors by refreshing.
```

### Converted Memories

**Memory 1: Getting JWT Token**
```markdown
**Source**: API Authentication - Getting a Token
**Topic**: JWT Token Acquisition

## Description
To authenticate with the API, obtain a JWT token by sending credentials to the login endpoint.

## Code
```javascript
fetch('/auth/login', {
  method: 'POST',
  body: JSON.stringify({ username, password })
})
```

## Usage
- Endpoint: `POST /auth/login`
- Required: username and password
- Returns: JWT token for subsequent requests

**Notion Source**: [URL]
```

**Memory 2: Using JWT Token**
```markdown
**Source**: API Authentication - Using the Token
**Topic**: JWT Token Usage

## Description
Once obtained, include the JWT token in the Authorization header for authenticated API requests.

## Code
```javascript
fetch('/api/data', {
  headers: { 'Authorization': `Bearer ${token}` }
})
```

## Important Notes
- Use Bearer scheme
- Include token in every authenticated request
- Tokens expire after 24 hours
- Handle 401 errors by refreshing token

**Notion Source**: [URL]
```

---

## Tips for Effective Conversion

1. **Preserve technical accuracy**: Don't paraphrase code or technical terms
2. **Maintain context**: Always explain where this fits in the bigger picture
3. **Be consistent**: Use similar formatting for similar content types
4. **Think reusability**: Format memories for future retrieval and use
5. **Include examples**: Code examples and concrete examples are valuable
6. **Don't over-split**: Related information should stay together
7. **Test retrieval**: Consider what search queries would find these memories
