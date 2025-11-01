# Amp-Native Infrastructure - Quick Start

**5-minute guide to building intelligent development infrastructure with Amp**

---

## What Is This?

An **Amp-native** approach to development infrastructure that leverages Amp's unique capabilities:

- **Oracle (GPT-5)** - Complex reasoning for architecture, debugging, planning
- **Librarian** - Cross-repository and framework documentation research
- **Toolboxes** - Project-specific automation with rich feedback
- **AGENTS.md** - Context-aware guidance that auto-activates
- **Custom Commands** - Workflow orchestrators for complex tasks

**Not a direct translation of Claude Code** - This is designed from the ground up for Amp.

---

## Quick Start (5 Minutes)

### 1. Copy the Template (1 minute)

```bash
# Copy the amp-native-template to your project
cp -r amp-native-template/.agents .
cp amp-native-template/AGENTS.md .
mkdir -p docs/development

# Set up toolbox directory
export AMP_TOOLBOX=~/.config/amp/toolbox
mkdir -p $AMP_TOOLBOX
cp amp-native-template/toolbox/* $AMP_TOOLBOX/
chmod +x $AMP_TOOLBOX/*
chmod +x .agents/commands/*
```

### 2. Customize AGENTS.md (2 minutes)

Edit `AGENTS.md`:
- Update tech stack description
- Update build/test commands
- Add your project-specific patterns

### 3. Test It (2 minutes)

```bash
# Start Amp
amp

# Test Oracle
"Use Oracle to review this file: [filename]"

# Test Librarian
"Ask Librarian about [framework] [topic]"

# Test custom commands
# Press Ctrl-O (CLI) or Cmd-Shift-A (editor)
# Try: architecture-review
```

**Done!** You now have intelligent infrastructure.

---

## Core Concepts

### 1. Oracle (GPT-5) - Your "Second Opinion"

**Use for:**
- Architecture reviews
- Complex debugging
- Planning refactorings
- Security analysis

**Example:**
```
"Use Oracle to review this authentication system:
- Files: auth/service.ts, auth/middleware.ts
- Focus: security, scalability, maintainability"
```

### 2. Librarian - External Knowledge

**Use for:**
- Framework documentation
- Cross-repo research
- Real-world examples
- Best practices

**Example:**
```
"Ask Librarian about MUI v7 Grid component:
- Search mui/material-ui repo
- Find API docs and examples
- Show migration guide from v6"
```

### 3. Toolboxes - Smart Automation

**Use for:**
- Architecture validation
- Type checking
- Test running
- Code quality checks

**Example:**
Amp automatically discovers and uses toolboxes when relevant.

### 4. AGENTS.md - Auto-Activating Guidance

**Use for:**
- Project overview
- Common patterns
- When to use Oracle/Librarian
- Team conventions

**Auto-activates** based on your current directory and files you're working on.

### 5. Custom Commands - Workflow Orchestration

**Use for:**
- Multi-step workflows
- Combining Oracle + Librarian
- Knowledge capture
- Team processes

**Example:**
```
# Press Ctrl-O or Cmd-Shift-A
architecture-review
```

---

## Key Differences from Claude Code

| Aspect | Claude Code | Amp-Native |
|--------|-------------|------------|
| **Guidance** | Skills + Hooks | AGENTS.md + Oracle hints |
| **Activation** | Hooks analyze prompts | Auto-inclusion via globs |
| **Complex Tasks** | Agents | Subagents + Oracle |
| **Validation** | Hooks | Toolboxes with rich feedback |
| **Research** | Manual | Librarian integration |
| **Knowledge** | Static docs | Shared threads + docs |

---

## Workflow Examples

### Example 1: New Feature

1. **Research** (Librarian): "Ask Librarian about [framework] [feature]"
2. **Plan** (Oracle): "Use Oracle to design [feature] based on Librarian's findings"
3. **Implement** (Main Agent): Code the feature
4. **Review** (Oracle): "Use Oracle to review for edge cases"
5. **Document** (Command): Run `capture-knowledge` command

### Example 2: Debugging

1. **Analyze** (Oracle): "Use Oracle to analyze this bug: [details]"
2. **Research** (Librarian): "Ask Librarian to search [framework] for similar issues"
3. **Fix** (Main Agent): Implement the fix
4. **Verify** (Toolbox): Run tests with `run-tests-smart`
5. **Document** (Command): Run `capture-knowledge` command

### Example 3: Architecture Review

1. **Run Command**: `architecture-review`
2. **Oracle Reviews**: Analyzes architecture comprehensively
3. **Prioritize**: Critical → High → Medium → Low
4. **Fix**: Address issues in priority order
5. **Share**: Share thread with team

---

## File Structure

```
your-project/
├── .agents/
│   └── commands/
│       ├── architecture-review
│       ├── research-framework
│       ├── debug-with-research
│       └── capture-knowledge
├── AGENTS.md (root guidance)
├── docs/
│   ├── development/
│   │   ├── backend.md (with globs)
│   │   ├── frontend.md (with globs)
│   │   ├── testing.md (with globs)
│   │   ├── oracle-workflows.md
│   │   └── librarian-patterns.md
│   └── knowledge/
│       └── [captured-knowledge].md
└── $AMP_TOOLBOX/
    ├── validate-architecture
    ├── validate-types
    └── run-tests-smart
```

---

## Best Practices

### Oracle Usage

✅ **DO:**
- Use for complex architecture decisions
- Provide context (files, requirements, concerns)
- Be specific about what to analyze

❌ **DON'T:**
- Use for simple edits
- Use without context
- Use for every task (it's slower/costlier)

### Librarian Usage

✅ **DO:**
- Use for framework documentation
- Specify which repos to search
- Be specific about what you need

❌ **DON'T:**
- Use for your own codebase
- Ask vague questions
- Expect it to know unconfigured private repos

### Toolbox Design

✅ **DO:**
- Provide rich, actionable feedback
- Include examples in error messages
- Make them discoverable (good descriptions)

❌ **DON'T:**
- Just return pass/fail
- Use generic error messages
- Forget to make them executable

---

## Team Adoption

### Onboarding (15 minutes per person)

1. Install Amp and configure workspace
2. Set up `$AMP_TOOLBOX` environment variable
3. Clone project and verify AGENTS.md
4. Test Oracle: "Use Oracle to review [something]"
5. Test Librarian: "Ask Librarian about [framework]"
6. Test commands: Press Ctrl-O or Cmd-Shift-A
7. Review shared threads from team

### Knowledge Sharing

1. Solve problem using Oracle/Librarian
2. Run `capture-knowledge` command
3. Set thread to "Workspace-shared"
4. Add thread link to knowledge doc
5. Share in team chat

---

## Migration from Claude Code

**Time Investment:** 6-8 hours total

1. **Foundation** (1 hour) - Copy template, customize AGENTS.md
2. **Convert Skills** (2-3 hours) - Create docs/development/ files with Oracle/Librarian hints
3. **Convert Hooks** (1-2 hours) - Create toolboxes with rich feedback
4. **Convert Agents** (1 hour) - Create orchestrating commands
5. **Test** (1-2 hours) - Verify everything works

**See AMP_NATIVE_GUIDE.md for detailed migration steps.**

---

## Success Metrics

**Adoption:**
- Team members regularly use Oracle
- Librarian is used for framework research
- Threads are shared weekly
- Knowledge base grows

**Quality:**
- Architecture issues caught by Oracle
- Bugs prevented by toolboxes
- Time saved by Librarian
- Code review improvements

**Knowledge:**
- Knowledge docs created
- AGENTS.md evolves
- Team patterns documented

---

## Next Steps

1. **Read:** AMP_NATIVE_GUIDE.md for comprehensive guide
2. **Copy:** amp-native-template/ to your project
3. **Customize:** AGENTS.md for your tech stack
4. **Test:** Oracle, Librarian, commands, toolboxes
5. **Share:** Start sharing threads with team

---

## Resources

- **AMP_NATIVE_GUIDE.md** - Complete implementation guide
- **amp-native-template/** - Ready-to-use template
- **Amp Manual** - https://ampcode.com/manual

---

## Philosophy

**This is not a Claude Code port.**

This is an Amp-first design that leverages:
- Oracle's reasoning for complex decisions
- Librarian's research for external knowledge
- Toolboxes for intelligent automation
- Thread sharing for team learning
- AGENTS.md for context-aware guidance

**Embrace Amp's unique capabilities!**

