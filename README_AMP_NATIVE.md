# Amp-Native Infrastructure Showcase

**Production-tested patterns for building intelligent development infrastructure with Amp**

---

## 🎯 What Is This?

An **Amp-native** development infrastructure system that leverages Amp's unique capabilities:

- **Oracle (GPT-5)** - Complex reasoning for architecture, debugging, and planning
- **Librarian** - Cross-repository and framework documentation research
- **Toolboxes** - Project-specific automation with rich, actionable feedback
- **AGENTS.md** - Context-aware guidance that auto-activates
- **Custom Commands** - Workflow orchestrators combining Oracle + Librarian

**This is NOT a Claude Code translation.** It's designed from the ground up for Amp.

---

## 🚀 Quick Start (5 Minutes)

```bash
# 1. Copy template to your project
cp -r amp-native-template/.agents .
cp amp-native-template/AGENTS.md .

# 2. Set up toolbox directory
export AMP_TOOLBOX=~/.config/amp/toolbox
mkdir -p $AMP_TOOLBOX
cp amp-native-template/toolbox/* $AMP_TOOLBOX/
chmod +x $AMP_TOOLBOX/* .agents/commands/*

# 3. Add to shell profile
echo 'export AMP_TOOLBOX=~/.config/amp/toolbox' >> ~/.bashrc

# 4. Test it
amp
# Try: "Use Oracle to review this file: AGENTS.md"
# Try: "Ask Librarian about React 18 concurrent features"
# Press Ctrl-O to see custom commands
```

**Done!** You now have intelligent infrastructure.

---

## 📦 Package Contents

### Documentation (4 files, ~2,340 lines)

```
📄 AMP_NATIVE_INDEX.md        - Central navigation hub
📄 AMP_NATIVE_SUMMARY.md      - 5-minute quick start
📄 AMP_NATIVE_GUIDE.md        - Complete implementation guide (10 parts)
📄 AMP_NATIVE_COMPLETE.md     - Package summary
```

### Template (7 files, ~1,420 lines)

```
amp-native-template/
├── 📄 AGENTS.md                           # Root guidance
├── 📄 README.md                           # Template usage guide
├── .agents/
│   └── commands/
│       ├── 🔧 architecture-review         # Oracle-powered review
│       ├── 🔧 research-framework          # Librarian research
│       ├── 🔧 debug-with-research         # Oracle + Librarian debugging
│       └── 🔧 capture-knowledge           # Knowledge documentation
├── toolbox/
│   ├── 🛠️ validate-architecture           # Architecture validation
│   └── 🛠️ run-tests-smart                 # Intelligent test runner
└── docs/
    └── development/                       # (Create for your project)
```

---

## 🎓 Core Concepts

### 1. Oracle (GPT-5) - Your "Second Opinion"

**Use for:** Architecture reviews, complex debugging, planning, security analysis

**Example:**
```
"Use Oracle to review this authentication system:
- Files: auth/service.ts, auth/middleware.ts
- Requirements: JWT-based, refresh tokens, role-based access
- Concerns: Security, scalability, maintainability"
```

### 2. Librarian - External Knowledge

**Use for:** Framework documentation, cross-repo research, best practices

**Example:**
```
"Ask Librarian about MUI v7 Grid component:
- Search mui/material-ui repo
- Find API documentation
- Show migration examples from v6 to v7"
```

### 3. Toolboxes - Smart Automation

**Use for:** Validation, testing, code quality checks

**Features:**
- Auto-discovered by Amp
- Rich, actionable feedback
- Specific file/line numbers
- Code examples in errors

### 4. AGENTS.md - Context-Aware Guidance

**Use for:** Project overview, patterns, Oracle/Librarian hints

**Features:**
- Auto-activates based on directory
- Hierarchical (root + subtree)
- References other docs with @-mentions

### 5. Custom Commands - Workflow Orchestration

**Use for:** Multi-step workflows, team processes

**Access:** Press Ctrl-O (CLI) or Cmd-Shift-A (editor)

---

## 🌟 Key Features

### Oracle-Powered Workflows

✅ **Architecture Review** - Comprehensive analysis with prioritized recommendations  
✅ **Complex Debugging** - Root cause analysis with fix suggestions  
✅ **Planning & Design** - Refactoring strategies with trade-off analysis  
✅ **Code Review** - Security, performance, maintainability checks  

### Librarian Integration

✅ **Framework Research** - Official docs + real-world examples  
✅ **Cross-Repo Patterns** - How your team solved similar problems  
✅ **Best Practices** - Industry-standard patterns  
✅ **Issue Research** - Framework bugs and workarounds  

### Intelligent Toolboxes

✅ **Architecture Validation** - Layered architecture enforcement  
✅ **Smart Test Runner** - Finds and runs relevant tests  
✅ **Rich Feedback** - File/line numbers + code examples  
✅ **Oracle Integration** - Suggests Oracle review for complex issues  

### Team Knowledge Capture

✅ **Thread Sharing** - Workspace-shared conversations  
✅ **Knowledge Docs** - Structured documentation  
✅ **AGENTS.md Evolution** - Patterns added as they emerge  
✅ **Success Metrics** - Track adoption and quality  

---

## 📊 Comparison: Claude Code vs Amp-Native

| Feature | Claude Code | Amp-Native |
|---------|-------------|------------|
| **Guidance** | Skills + Hooks | AGENTS.md + Oracle hints |
| **Activation** | Hooks analyze prompts | Auto-inclusion via globs |
| **Complex Tasks** | Agents | Subagents + Oracle |
| **Validation** | Hooks (pass/fail) | Toolboxes (rich feedback) |
| **Research** | Manual | Librarian integration |
| **Knowledge** | Static docs | Shared threads + docs |
| **Reasoning** | Main agent only | Oracle (GPT-5) for complex tasks |

---

## 🗺️ Learning Paths

### Beginner (15 minutes)

1. Read [AMP_NATIVE_SUMMARY.md](AMP_NATIVE_SUMMARY.md) (5 min)
2. Copy template to project (5 min)
3. Test Oracle, Librarian, commands (5 min)

### Intermediate (1 hour)

1. Read [AMP_NATIVE_GUIDE.md](AMP_NATIVE_GUIDE.md) Parts 1-5 (30 min)
2. Customize AGENTS.md (15 min)
3. Create docs/development/ files (15 min)

### Advanced (1 day)

1. Read complete guide (1 hour)
2. Implement full infrastructure (4 hours)
3. Build custom toolboxes (2 hours)
4. Test and iterate (1 hour)

### Migration from Claude Code (1 week)

1. Analyze current setup (2 hours)
2. Convert skills → AGENTS.md + docs (2-3 hours)
3. Convert hooks → toolboxes (1-2 hours)
4. Convert agents → commands (1 hour)
5. Add Oracle/Librarian enhancements (4-6 hours)
6. Test and iterate (1-2 hours)

---

## 💡 Workflow Examples

### Example 1: Implementing a New Feature

```
1. Research (Librarian)
   "Ask Librarian about [framework] [feature]"

2. Plan (Oracle)
   "Use Oracle to design [feature] based on Librarian's findings"

3. Implement (Main Agent)
   Code the feature

4. Review (Oracle)
   "Use Oracle to review for edge cases"

5. Document (Command)
   Run capture-knowledge command
```

### Example 2: Debugging Complex Issue

```
1. Analyze (Oracle)
   "Use Oracle to analyze this bug: [details]"

2. Research (Librarian)
   "Ask Librarian to search [framework] for similar issues"

3. Fix (Main Agent)
   Implement the fix

4. Verify (Toolbox)
   Run tests with run-tests-smart

5. Document (Command)
   Run capture-knowledge command
```

### Example 3: Architecture Review

```
1. Run Command
   Press Ctrl-O → architecture-review

2. Oracle Analysis
   Oracle reviews architecture comprehensively

3. Prioritize
   Critical → High → Medium → Low

4. Fix
   Address issues in priority order

5. Share
   Share thread with team
```

---

## 🎯 Success Metrics

### Adoption

- [ ] Team members use Oracle regularly
- [ ] Librarian is used for framework research
- [ ] Threads are shared weekly
- [ ] Knowledge base grows monthly

### Quality

- [ ] Architecture issues caught by Oracle
- [ ] Bugs prevented by toolboxes
- [ ] Time saved by Librarian research
- [ ] Code review improvements

### Knowledge

- [ ] Knowledge docs created
- [ ] AGENTS.md evolves
- [ ] Team patterns documented
- [ ] Onboarding time reduced

---

## 📚 Documentation

### Start Here

- **[AMP_NATIVE_INDEX.md](AMP_NATIVE_INDEX.md)** - Central navigation
- **[AMP_NATIVE_SUMMARY.md](AMP_NATIVE_SUMMARY.md)** - Quick start (5 min)

### Deep Dive

- **[AMP_NATIVE_GUIDE.md](AMP_NATIVE_GUIDE.md)** - Complete guide (45 min)
- **[amp-native-template/README.md](amp-native-template/README.md)** - Template usage

### Reference

- **[AMP_NATIVE_COMPLETE.md](AMP_NATIVE_COMPLETE.md)** - Package summary
- **[Amp Manual](https://ampcode.com/manual)** - Official documentation

---

## 🛠️ Customization

### 1. Update AGENTS.md

```markdown
# Project Development Guidelines

This project uses [YOUR TECH STACK]

## Quick Reference
**Build:** `[your command]`
**Test:** `[your command]`

## When to Use Oracle
[Your Oracle usage patterns]

## When to Use Librarian
[Your Librarian usage patterns]
```

### 2. Create Development Docs

```bash
mkdir -p docs/development

cat > docs/development/backend.md << 'EOF'
---
globs:
  - 'backend/**/*.ts'
---

# Backend Development Guidelines

## Oracle Integration
[When to use Oracle for backend work]

## Librarian Integration
[When to use Librarian for backend work]

[Your backend patterns]
EOF
```

### 3. Add Custom Toolboxes

```bash
cat > $AMP_TOOLBOX/your-toolbox << 'EOF'
#!/usr/bin/env node

// Your toolbox implementation
// Provide rich feedback with examples
EOF

chmod +x $AMP_TOOLBOX/your-toolbox
```

### 4. Create Custom Commands

```bash
cat > .agents/commands/your-command << 'EOF'
#!/usr/bin/env bash

cat << 'PROMPT'
# Your Workflow

[Your workflow steps with Oracle/Librarian integration]
PROMPT
EOF

chmod +x .agents/commands/your-command
```

---

## 🤝 Team Adoption

### Onboarding (15 minutes per person)

1. Install Amp and configure workspace
2. Set up $AMP_TOOLBOX environment variable
3. Clone project and verify AGENTS.md
4. Test Oracle, Librarian, commands
5. Review shared threads from team

### Knowledge Sharing Workflow

1. Solve problem using Oracle/Librarian
2. Run `capture-knowledge` command
3. Set thread to "Workspace-shared"
4. Add thread link to knowledge doc
5. Share in team chat

---

## 🔗 Quick Links

**Documentation:**
- [Quick Start](AMP_NATIVE_SUMMARY.md)
- [Complete Guide](AMP_NATIVE_GUIDE.md)
- [Template Usage](amp-native-template/README.md)

**Template:**
- [AGENTS.md](amp-native-template/AGENTS.md)
- [Commands](amp-native-template/.agents/commands/)
- [Toolboxes](amp-native-template/toolbox/)

**External:**
- [Amp Manual](https://ampcode.com/manual)
- [Oracle Docs](https://ampcode.com/manual#oracle)
- [Librarian Docs](https://ampcode.com/manual#librarian)

---

## 🎉 Get Started

**Ready to build intelligent infrastructure?**

1. **Read:** [AMP_NATIVE_SUMMARY.md](AMP_NATIVE_SUMMARY.md) (5 min)
2. **Copy:** Template to your project (5 min)
3. **Test:** Oracle, Librarian, commands (5 min)

**Total time:** 15 minutes to get started!

---

## 💬 Philosophy

**This is not a Claude Code port.**

This is an **Amp-first design** that embraces Amp's unique capabilities:
- Oracle's reasoning for complex decisions
- Librarian's research for external knowledge
- Toolboxes for intelligent automation
- Thread sharing for team learning
- AGENTS.md for context-aware guidance

**Embrace Amp's unique capabilities!** 🚀

