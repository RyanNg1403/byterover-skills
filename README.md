# Byterover Skills

A collection of specialized Claude Code skills for working with the [Byterover MCP Server](https://github.com/ngalvare/byterover-mcp). These skills extend Byterover's memory and knowledge management capabilities with structured workflows, advanced documentation features, and seamless integrations.

## What are Byterover Skills?

Byterover is a powerful memory system for AI agents, allowing them to store and retrieve knowledge across conversations. These skills build on top of Byterover's foundation to provide:

- **Structured workflows** for common documentation tasks
- **Bidirectional integrations** with tools like Notion
- **Specialized formats** for reports, PRDs, architecture docs, and more
- **Best practices** for knowledge capture and retrieval

## Available Skills

### 🔄 byterover-notion-sync

**Bidirectional knowledge synchronization between Byterover memories and Notion documentation.**

**Use when you need to**:
- Convert Byterover memories into structured Notion documentation (implementation reports, PRDs, feature docs, architecture docs)
- Import Notion pages into searchable Byterover memories
- Create timelines and reports from development memories
- Document features and architectures based on implementation knowledge

**Key capabilities**:
- **4 Documentation Formats**: Implementation reports with timelines, PRDs, feature documentation, technical architecture docs
- **Smart format selection**: Automatically determines appropriate format based on content
- **Multi-query retrieval**: Intelligently queries memories multiple times with variations for comprehensive context
- **Logical chunking**: Breaks Notion content into optimal memory sizes (200-800 words)
- **Structure preservation**: Maintains code blocks, tables, headings, and nested pages
- **Bidirectional traceability**: Links between Notion pages and Byterover memories

**Example use cases**:
```
"Create an implementation report on the authentication system from July 10-15"
"Turn our notification system discussions into a PRD"
"Document the microservices architecture"
"Import the API documentation from Notion into memories"
```

[View full documentation →](byterover-notion-sync/)

---

## Installation

### Prerequisites

1. **Claude Code** - Install from [claude.ai/claude-code](https://claude.ai/claude-code)
2. **Byterover MCP Server** - Set up from [ngalvare/byterover-mcp](https://github.com/ngalvare/byterover-mcp)
3. (Optional for byterover-notion-sync) **Notion MCP Server** - Set up from [Notion MCP documentation](https://www.notion.so/help/mcp)

### Installing Skills

#### Option 1: Clone and Copy (Recommended)

1. **Clone this repository**:
   ```bash
   git clone https://github.com/RyanNg1403/byterover-skills.git
   cd byterover-skills
   ```

2. **Copy desired skill(s) to your Claude Code skills directory**:

   **On macOS/Linux**:
   ```bash
   # Copy individual skill
   cp -r byterover-notion-sync ~/.claude/skills/

   # Or copy all skills
   cp -r */ ~/.claude/skills/
   ```

   **On Windows**:
   ```powershell
   # Copy individual skill
   Copy-Item -Recurse byterover-notion-sync $env:USERPROFILE\.claude\skills\

   # Or copy all skills
   Get-ChildItem -Directory | Copy-Item -Recurse -Destination $env:USERPROFILE\.claude\skills\
   ```

3. **Verify installation**:
   ```bash
   # On macOS/Linux
   ls ~/.claude/skills/byterover-notion-sync

   # On Windows
   dir $env:USERPROFILE\.claude\skills\byterover-notion-sync
   ```

#### Option 2: Manual Download

1. Download individual skill folders from this repository
2. Place them in your Claude Code skills directory:
   - **macOS/Linux**: `~/.claude/skills/`
   - **Windows**: `%USERPROFILE%\.claude\skills\`

### Verifying Installation

After installation, skills should automatically be available in Claude Code. You can verify by:

1. Starting a Claude Code session
2. Asking: "What Byterover skills are available?"
3. Claude should list the installed skills

---

## Usage

### Quick Start

Once installed, skills are automatically invoked based on your requests. No special commands needed!

**Example workflows**:

```
# Memories → Notion Documentation
User: "Create an implementation report on the payment system we built last week"
→ Claude uses byterover-notion-sync to:
  1. Query memories about payment system
  2. Structure as implementation report
  3. Create Notion page with timeline

# Notion → Byterover Memories
User: "Import our API documentation from Notion into memories"
→ Claude uses byterover-notion-sync to:
  1. Fetch Notion page
  2. Break into logical chunks
  3. Store as searchable memories

# Architecture Documentation
User: "Document our microservices architecture based on recent work"
→ Claude uses byterover-notion-sync to:
  1. Retrieve architecture-related memories
  2. Structure as technical architecture doc
  3. Include diagrams and design decisions
```

### Skill-Specific Documentation

Each skill includes detailed documentation in its folder:
- **SKILL.md**: Complete workflow guides and best practices
- **references/**: Detailed format templates and guidelines

---

## Skill Development

### Contributing New Skills

We welcome contributions! To add a new Byterover skill:

1. **Fork this repository**
2. **Create a new skill** following the structure:
   ```
   your-skill-name/
   ├── SKILL.md          # Required: Skill instructions and workflows
   ├── references/       # Optional: Detailed guides and templates
   ├── scripts/          # Optional: Executable helpers
   └── assets/           # Optional: Templates and resources
   ```
3. **Update this README** with skill description
4. **Submit a pull request**

### Skill Structure Guidelines

Follow the [Claude Code Skill Creator](https://github.com/anthropics/skill-creator) guidelines:

- **SKILL.md**: Include name, description, workflows, and examples
- **References**: Detailed documentation loaded on-demand
- **Scripts**: Executable code for deterministic tasks
- **Assets**: Files used in output (templates, boilerplate)

---

## Roadmap

Future skills in development:

- **byterover-github-integration**: Sync code comments, PR discussions, and issue threads with memories
- **byterover-meeting-notes**: Convert meeting transcripts into structured memories and action items
- **byterover-code-knowledge**: Extract and organize code patterns, architectural decisions, and best practices
- **byterover-research-synthesis**: Aggregate memories into research reports and literature reviews

Have a skill idea? [Open an issue](https://github.com/[your-username]/byterover-skills/issues) or contribute!

---

## Requirements

- **Claude Code**: Latest version
- **Byterover MCP Server**: Configured and running
- Additional requirements vary by skill (e.g., Notion MCP for byterover-notion-sync)

---

## Support & Community

- **Issues**: [GitHub Issues](https://github.com/[your-username]/byterover-skills/issues)
- **Discussions**: [GitHub Discussions](https://github.com/[your-username]/byterover-skills/discussions)
- **Byterover MCP**: [ngalvare/byterover-mcp](https://github.com/ngalvare/byterover-mcp)

---

## License

MIT License - see [LICENSE](LICENSE) for details.

---

## Acknowledgments

- Built for [Claude Code](https://claude.ai/claude-code) by Anthropic
- Powered by [Byterover MCP Server](https://github.com/ngalvare/byterover-mcp)
- Integrations with [Notion MCP](https://www.notion.so/help/mcp)

---

**Made with ❤️ for better AI knowledge management**
