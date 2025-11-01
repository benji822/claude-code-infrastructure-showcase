# Amp-Native Development Infrastructure Template

**Ready-to-use template for intelligent development workflows with Amp**

---

## What's Included

This template provides a complete Amp-native infrastructure:

### 📁 Files

```
amp-native-template/
├── AGENTS.md                    # Root guidance (customize for your project)
├── .agents/
│   └── commands/
│       ├── architecture-review  # Oracle-powered architecture review
│       ├── research-framework   # Librarian-based framework research
│       ├── debug-with-research  # Combined Oracle + Librarian debugging
│       └── capture-knowledge    # Team knowledge documentation
├── toolbox/
│   ├── validate-architecture    # Layered architecture validation
│   └── run-tests-smart          # Intelligent test runner
└── docs/
    └── development/             # (Create these for your project)
        ├── backend.md           # Backend patterns with Oracle/Librarian hints
        ├── frontend.md          # Frontend patterns with Oracle/Librarian hints
        └── testing.md           # Testing patterns
```

### 🎯 Features

**Oracle Integration (GPT-5)**
- Architecture review workflows
- Complex debugging assistance
- Planning and design support
- Code review automation

**Librarian Integration**
- Framework documentation research
- Cross-repository pattern discovery
- Best practices lookup
- Real-world example finding

**Smart Toolboxes**
- Architecture validation with actionable feedback
- Intelligent test running
- Rich error messages with examples

**Workflow Commands**
- Multi-step architecture reviews
- Framework research workflows
- Advanced debugging with Oracle + Librarian
- Team knowledge capture

---

## Quick Start

### 1. Copy to Your Project

```bash
# Copy template files
cp -r amp-native-template/.agents .
cp amp-native-template/AGENTS.md .
mkdir -p docs/development

# Set up toolbox directory
export AMP_TOOLBOX=~/.config/amp/toolbox
mkdir -p $AMP_TOOLBOX
cp amp-native-template/toolbox/* $AMP_TOOLBOX/
chmod +x $AMP_TOOLBOX/*
chmod +x .agents/commands/*

# Add to your shell profile (.bashrc, .zshrc, etc.)
echo 'export AMP_TOOLBOX=~/.config/amp/toolbox' >> ~/.bashrc
```

### 2. Customize AGENTS.md

Edit `AGENTS.md` to match your project:

```markdown
# Project Development Guidelines

This project uses [YOUR TECH STACK HERE]

## Quick Reference

**Build:** `[your build command]`
**Test:** `[your test command]`
**Dev:** `[your dev command]`

## Architecture Overview

[Describe your architecture]

...
```

### 3. Create Development Docs (Optional)

Create `docs/development/backend.md`:

```yaml
---
globs:
  - 'backend/**/*.ts'
  - 'src/api/**/*.ts'
---

# Backend Development Guidelines

## Oracle Integration

Use Oracle for:
- API design reviews
- Service layer architecture
- Database query optimization

## Librarian Integration

Use Librarian for:
- Framework documentation
- Best practices research

[Your backend patterns here]
```

### 4. Test It

```bash
# Start Amp
amp

# Test Oracle
"Use Oracle to review this file: AGENTS.md"

# Test Librarian
"Ask Librarian about React 18 concurrent features"

# Test custom commands
# Press Ctrl-O (CLI) or Cmd-Shift-A (editor)
# Select: architecture-review

# Test toolboxes
# Amp discovers them automatically
# Try making an architecture violation and Amp may suggest validation
```

---

## Using the Commands

### architecture-review

Conducts comprehensive Oracle-powered architecture review.

**Usage:**
```
# In Amp, press Ctrl-O or Cmd-Shift-A
# Select: architecture-review
```

**What it does:**
1. Gathers all architectural files
2. Uses Oracle to analyze architecture
3. Identifies issues with severity levels
4. Provides specific fixes with code examples
5. Creates prioritized action plan

### research-framework

Uses Librarian to research framework topics.

**Usage:**
```
# In Amp, press Ctrl-O or Cmd-Shift-A
# Select: research-framework
# Enter: framework name (e.g., "MUI v7")
# Enter: topic (e.g., "Grid component")
```

**What it does:**
1. Searches official framework repository
2. Finds real-world usage examples
3. Checks for recent changes
4. Searches your organization's repos
5. Synthesizes findings into recommendations
6. Creates knowledge documentation

### debug-with-research

Advanced debugging combining Oracle and Librarian.

**Usage:**
```
# In Amp, press Ctrl-O or Cmd-Shift-A
# Select: debug-with-research
# Provide error details when prompted
```

**What it does:**
1. Gathers error information
2. Uses Oracle for root cause analysis
3. Uses Librarian for external research (if framework issue)
4. Designs fix with Oracle
5. Implements and tests
6. Oracle reviews the fix
7. Documents for team

### capture-knowledge

Documents solutions for team knowledge sharing.

**Usage:**
```
# In Amp, press Ctrl-O or Cmd-Shift-A
# Select: capture-knowledge
# Enter: topic name (e.g., "authentication-implementation")
```

**What it does:**
1. Reviews conversation for key points
2. Creates comprehensive documentation
3. Suggests AGENTS.md updates
4. Provides thread sharing checklist
5. Recommends next steps (toolbox, command, etc.)

---

## Using the Toolboxes

### validate-architecture

Validates layered architecture and provides actionable feedback.

**Auto-discovered by Amp** - No manual invocation needed.

**What it checks:**
- Business logic in routes
- Database access in controllers
- Missing error handling
- Missing input validation

**Output:**
- Severity levels (Critical, High, Medium, Low)
- File names and line numbers
- Specific issues
- Concrete suggestions
- Code examples

### run-tests-smart

Intelligent test runner that finds relevant tests.

**Auto-discovered by Amp** - No manual invocation needed.

**Features:**
- Finds tests for changed files
- Runs only relevant tests
- Provides debugging suggestions on failure
- Suggests Oracle review for test coverage

---

## Customization Guide

### Adding Your Own Patterns

**1. Create granular guidance files:**

```bash
# Create docs/development/your-pattern.md
cat > docs/development/your-pattern.md << 'EOF'
---
globs:
  - 'path/to/files/**/*.ts'
---

# Your Pattern Name

## Oracle Integration
[When to use Oracle for this pattern]

## Librarian Integration
[When to use Librarian for this pattern]

[Your pattern details]
EOF
```

**2. Reference in AGENTS.md:**

```markdown
## Common Patterns

For [your pattern], see @docs/development/your-pattern.md
```

### Adding Custom Commands

**1. Create command file:**

```bash
cat > .agents/commands/your-command << 'EOF'
#!/usr/bin/env bash

cat << 'PROMPT'
# Your Command Workflow

[Your workflow steps]

## Phase 1: [Step 1]
[Details]

## Phase 2: [Step 2]
[Details]

...
PROMPT
EOF

chmod +x .agents/commands/your-command
```

**2. Test it:**

```bash
# In Amp, press Ctrl-O or Cmd-Shift-A
# Your command should appear in the list
```

### Adding Custom Toolboxes

**1. Create toolbox script:**

```bash
cat > $AMP_TOOLBOX/your-toolbox << 'EOF'
#!/usr/bin/env node

const action = process.env.TOOLBOX_ACTION;

if (action === 'describe') {
  console.log([
    'name: your-toolbox',
    'description: What your toolbox does',
    'param1: string description of param1',
    'param2: boolean description of param2'
  ].join('\n'));
  process.exit(0);
}

if (action === 'execute') {
  // Read parameters from stdin
  const fs = require('fs');
  const input = fs.readFileSync(0, 'utf-8');
  
  // Parse parameters
  const param1Match = input.match(/param1:\s*(.+)/);
  const param1 = param1Match ? param1Match[1].trim() : '';
  
  // Your toolbox logic here
  
  // Provide rich feedback
  console.log('✅ Success!');
  // or
  console.log('❌ Issue found:');
  console.log('   File: path/to/file.ts:42');
  console.log('   Problem: [description]');
  console.log('   Suggestion: [how to fix]');
  console.log('   Example:');
  console.log('   [code example]');
  
  process.exit(0); // or exit(1) for failure
}
EOF

chmod +x $AMP_TOOLBOX/your-toolbox
```

**2. Test it:**

Amp will automatically discover your toolbox.

---

## Best Practices

### Oracle Usage

**Good:**
```
"Use Oracle to review this authentication system:
- Files: auth/service.ts, auth/middleware.ts
- Requirements: JWT-based, refresh tokens
- Concerns: Security, scalability"
```

**Bad:**
```
"Review this code"  # Too vague, no context
```

### Librarian Usage

**Good:**
```
"Ask Librarian about MUI v7 Grid component:
- Search mui/material-ui repo
- Find API documentation
- Show migration examples from v6"
```

**Bad:**
```
"How does Grid work?"  # Too vague, no repo specified
```

### Toolbox Design

**Good:**
- Rich, actionable feedback
- Specific file names and line numbers
- Code examples in error messages
- Clear severity levels

**Bad:**
- Generic "validation failed" messages
- No suggestions for fixes
- No examples

---

## Team Adoption

### Onboarding New Team Members

1. **Setup** (5 minutes)
   ```bash
   # Clone project
   git clone [your-repo]
   cd [your-repo]
   
   # Set up toolbox
   export AMP_TOOLBOX=~/.config/amp/toolbox
   echo 'export AMP_TOOLBOX=~/.config/amp/toolbox' >> ~/.bashrc
   ```

2. **Test** (5 minutes)
   - Test Oracle: "Use Oracle to review AGENTS.md"
   - Test Librarian: "Ask Librarian about [your framework]"
   - Test commands: Press Ctrl-O, try architecture-review
   - Test toolboxes: Make a change, see if validation triggers

3. **Learn** (5 minutes)
   - Read AGENTS.md
   - Review docs/development/
   - Check docs/knowledge/ for team learnings
   - Review shared threads

### Knowledge Sharing Workflow

1. Solve a problem using Oracle/Librarian
2. Run `capture-knowledge` command
3. Set thread to "Workspace-shared"
4. Add thread link to knowledge doc
5. Share in team chat
6. Update AGENTS.md if pattern emerges

---

## Troubleshooting

### Commands don't appear

```bash
# Make sure commands are executable
chmod +x .agents/commands/*

# Restart Amp
```

### Toolboxes not discovered

```bash
# Check environment variable
echo $AMP_TOOLBOX

# Make sure toolboxes are executable
chmod +x $AMP_TOOLBOX/*

# Restart Amp
```

### Oracle not responding

```
# Be more specific in your prompt
# Provide context: files, requirements, concerns
# Example:
"Use Oracle to review this specific file: [filename]
Focus on: [what to analyze]"
```

### Librarian not finding results

```
# Specify the repository to search
# Be specific about what you're looking for
# Example:
"Ask Librarian to search the [framework] repository for:
- [specific topic]
- [what you need]"
```

---

## Next Steps

1. **Customize** AGENTS.md for your project
2. **Create** docs/development/ files for your patterns
3. **Add** your own custom commands
4. **Build** project-specific toolboxes
5. **Share** threads with your team
6. **Grow** your knowledge base

---

## Resources

- **AMP_NATIVE_GUIDE.md** - Comprehensive implementation guide
- **AMP_NATIVE_SUMMARY.md** - Quick start guide
- **Amp Manual** - https://ampcode.com/manual

---

## Support

For questions or issues:
1. Check AMP_NATIVE_GUIDE.md for detailed documentation
2. Review Amp manual: https://ampcode.com/manual
3. Share threads with your team for collaborative problem-solving

---

**Remember:** This is an Amp-first design. Embrace Oracle, Librarian, and thread sharing!

