# Contributing to Byterover Skills

Thank you for your interest in contributing to Byterover Skills! This document provides guidelines for contributing new skills or improving existing ones.

## Getting Started

1. **Fork the repository** on GitHub
2. **Clone your fork** locally:
   ```bash
   git clone https://github.com/YOUR-USERNAME/byterover-skills.git
   cd byterover-skills
   ```
3. **Create a branch** for your contribution:
   ```bash
   git checkout -b feature/your-skill-name
   ```

## Creating a New Skill

### Skill Structure

Every skill should follow this structure:

```
your-skill-name/
├── SKILL.md          # Required: Main skill documentation
├── references/       # Optional: Detailed guides and templates
│   └── *.md
├── scripts/          # Optional: Executable code
│   └── *.py
└── assets/           # Optional: Templates and resources
```

### SKILL.md Requirements

Your SKILL.md must include:

1. **YAML Frontmatter**:
   ```yaml
   ---
   name: your-skill-name
   description: Clear, concise description of what the skill does and when to use it (2-3 sentences)
   ---
   ```

2. **Overview**: Brief introduction (2-3 sentences)

3. **Core Capabilities**: What the skill enables

4. **Workflow/Usage**: Step-by-step instructions

5. **Examples**: Concrete usage examples

6. **Best Practices**: Tips for effective use

7. **References**: Links to bundled resources if applicable

### Skill Guidelines

**Good Skills**:
- Solve specific, well-defined problems
- Include clear workflows and examples
- Provide reusable templates or code
- Document best practices
- Are well-tested

**Avoid**:
- Overly broad or vague functionality
- Duplication of existing skills
- Incomplete documentation
- Untested workflows

## Testing Your Skill

Before submitting:

1. **Install locally**:
   ```bash
   cp -r your-skill-name ~/.claude/skills/
   ```

2. **Test with Claude Code**:
   - Try various user queries that should trigger the skill
   - Verify workflows work end-to-end
   - Test edge cases and error handling

3. **Validate structure**:
   Use the skill-creator validation script if available:
   ```bash
   python validate_skill.py your-skill-name/
   ```

## Submission Process

1. **Update README.md**:
   - Add your skill to the "Available Skills" section
   - Include description, key capabilities, and example use cases
   - Update the table of contents if needed

2. **Commit your changes**:
   ```bash
   git add .
   git commit -m "Add [your-skill-name] skill"
   ```

3. **Push to your fork**:
   ```bash
   git push origin feature/your-skill-name
   ```

4. **Create a Pull Request**:
   - Go to the original repository on GitHub
   - Click "New Pull Request"
   - Select your branch
   - Fill out the PR template with:
     - Description of the skill
     - What problem it solves
     - Testing you've performed
     - Any dependencies or requirements

## Improving Existing Skills

To improve an existing skill:

1. **Create an issue** describing the improvement
2. **Fork and branch** as above
3. **Make your changes**
4. **Test thoroughly**
5. **Submit a PR** referencing the issue

## Code Style

### Markdown

- Use clear, concise language
- Include code examples in triple backticks with language tags
- Use headings consistently (## for sections, ### for subsections)
- Include links to references where appropriate

### Python Scripts

If including Python scripts:
- Follow PEP 8 style guidelines
- Include docstrings
- Add comments for complex logic
- Handle errors gracefully

## Documentation Standards

- **Be specific**: "Use when creating PRDs from feature discussions" not "Use for documentation"
- **Include examples**: Real-world usage examples are invaluable
- **Explain why**: Don't just say what to do, explain why
- **Link resources**: Reference bundled materials and external docs
- **Update README**: Always update the main README when adding/changing skills

## Getting Help

- **Questions**: Open a [Discussion](https://github.com/[your-username]/byterover-skills/discussions)
- **Bugs**: Report an [Issue](https://github.com/[your-username]/byterover-skills/issues)
- **Ideas**: Share in [Discussions](https://github.com/[your-username]/byterover-skills/discussions)

## Code of Conduct

- Be respectful and inclusive
- Provide constructive feedback
- Focus on what's best for the community
- Help others learn and grow

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

Thank you for contributing to Byterover Skills! Your skills help the entire community work more effectively with AI agents and knowledge management.
