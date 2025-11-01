# Amp-Native Infrastructure - Complete Guide

**Central navigation for the Amp-native development infrastructure**

---

## 📚 Documentation Overview

This package provides a complete Amp-native infrastructure implementation, redesigned from the ground up to leverage Amp's unique capabilities rather than simply translating Claude Code concepts.

### Quick Navigation

| Document | Purpose | Time to Read |
|----------|---------|--------------|
| **[AMP_NATIVE_SUMMARY.md](AMP_NATIVE_SUMMARY.md)** | Quick start guide | 5 minutes |
| **[AMP_NATIVE_GUIDE.md](AMP_NATIVE_GUIDE.md)** | Complete implementation guide | 30-45 minutes |
| **[amp-native-template/README.md](amp-native-template/README.md)** | Template usage guide | 10 minutes |

---

## 🚀 Getting Started

### For Beginners (Start Here)

1. **Read:** [AMP_NATIVE_SUMMARY.md](AMP_NATIVE_SUMMARY.md) (5 minutes)
   - Understand core concepts
   - See quick start steps
   - Learn key differences from Claude Code

2. **Copy:** Template to your project (5 minutes)
   ```bash
   cp -r amp-native-template/.agents .
   cp amp-native-template/AGENTS.md .
   export AMP_TOOLBOX=~/.config/amp/toolbox
   mkdir -p $AMP_TOOLBOX
   cp amp-native-template/toolbox/* $AMP_TOOLBOX/
   chmod +x $AMP_TOOLBOX/* .agents/commands/*
   ```

3. **Test:** Oracle, Librarian, Commands (5 minutes)
   ```bash
   amp
   # Try: "Use Oracle to review this file: AGENTS.md"
   # Try: "Ask Librarian about React 18"
   # Press Ctrl-O to see custom commands
   ```

### For Intermediate Users

1. **Read:** [AMP_NATIVE_GUIDE.md](AMP_NATIVE_GUIDE.md) Parts 1-5 (20 minutes)
   - Intelligent Context System
   - Librarian Integration
   - Advanced Toolboxes
   - Orchestrating Custom Commands
   - Thread-Based Knowledge Capture

2. **Customize:** Template for your project (30 minutes)
   - Update AGENTS.md with your tech stack
   - Create docs/development/ files
   - Add project-specific toolboxes

3. **Implement:** Oracle/Librarian workflows (ongoing)
   - Use Oracle for architecture reviews
   - Use Librarian for framework research
   - Share threads with team

### For Advanced Users

1. **Read:** [AMP_NATIVE_GUIDE.md](AMP_NATIVE_GUIDE.md) Parts 6-10 (25 minutes)
   - Implementation Examples
   - Migration Strategy
   - Best Practices
   - Team Adoption
   - Measuring Success

2. **Migrate:** From Claude Code (6-8 hours)
   - Convert skills to AGENTS.md + docs
   - Convert hooks to toolboxes
   - Convert agents to commands
   - Add Oracle/Librarian integration

3. **Extend:** Build custom infrastructure (ongoing)
   - Create specialized toolboxes
   - Build workflow commands
   - Develop team patterns

---

## 🎯 Core Concepts

### Oracle (GPT-5) - Complex Reasoning

**What:** A "second opinion" model for complex analysis  
**When:** Architecture, debugging, planning, security  
**How:** "Use Oracle to review [specific task with context]"

**Example:**
```
"Use Oracle to review this authentication system:
- Files: auth/service.ts, auth/middleware.ts
- Requirements: JWT-based, refresh tokens
- Concerns: Security, scalability, maintainability"
```

### Librarian - External Knowledge

**What:** Searches GitHub repos for documentation and examples  
**When:** Framework docs, cross-repo research, best practices  
**How:** "Ask Librarian about [framework] [topic]"

**Example:**
```
"Ask Librarian about MUI v7 Grid component:
- Search mui/material-ui repo
- Find API documentation
- Show migration examples from v6"
```

### Toolboxes - Smart Automation

**What:** Project-specific scripts with rich feedback  
**When:** Validation, testing, code quality  
**How:** Auto-discovered by Amp

**Example:**
- `validate-architecture` - Checks layered architecture
- `run-tests-smart` - Intelligent test runner

### AGENTS.md - Context-Aware Guidance

**What:** Hierarchical guidance that auto-activates  
**When:** Always (based on directory and files)  
**How:** Create AGENTS.md and docs/development/ files

**Example:**
```yaml
---
globs:
  - 'backend/**/*.ts'
---

# Backend Development Guidelines
[Your patterns + Oracle/Librarian hints]
```

### Custom Commands - Workflow Orchestration

**What:** Multi-step workflows combining Oracle/Librarian  
**When:** Complex tasks, team processes  
**How:** Press Ctrl-O (CLI) or Cmd-Shift-A (editor)

**Example:**
- `architecture-review` - Oracle-powered review
- `research-framework` - Librarian-based research
- `debug-with-research` - Oracle + Librarian debugging
- `capture-knowledge` - Team knowledge documentation

---

## 📦 What's Included

### Documentation (4 files)

1. **AMP_NATIVE_INDEX.md** (this file)
   - Central navigation
   - Quick start paths
   - Concept overview

2. **AMP_NATIVE_SUMMARY.md**
   - 5-minute quick start
   - Core concepts
   - Workflow examples
   - Best practices

3. **AMP_NATIVE_GUIDE.md**
   - Complete implementation guide (10 parts)
   - Detailed examples
   - Migration strategy
   - Team adoption
   - Success metrics

4. **amp-native-template/README.md**
   - Template usage guide
   - Customization instructions
   - Troubleshooting

### Template Files (7 files)

1. **AGENTS.md** - Root guidance (customize for your project)
2. **architecture-review** - Oracle-powered architecture review command
3. **research-framework** - Librarian-based framework research command
4. **debug-with-research** - Combined Oracle + Librarian debugging command
5. **capture-knowledge** - Team knowledge documentation command
6. **validate-architecture** - Layered architecture validation toolbox
7. **run-tests-smart** - Intelligent test runner toolbox

---

## 🗺️ Learning Paths

### Path 1: Quick Start (15 minutes)

**Goal:** Get up and running fast

1. Read AMP_NATIVE_SUMMARY.md (5 min)
2. Copy template to project (5 min)
3. Test Oracle, Librarian, commands (5 min)

**Next:** Start using Oracle and Librarian in your daily work

### Path 2: Deep Understanding (1 hour)

**Goal:** Understand all capabilities

1. Read AMP_NATIVE_SUMMARY.md (5 min)
2. Read AMP_NATIVE_GUIDE.md Parts 1-5 (30 min)
3. Read amp-native-template/README.md (10 min)
4. Experiment with template (15 min)

**Next:** Customize for your project

### Path 3: Full Implementation (1 day)

**Goal:** Complete Amp-native infrastructure

1. Read all documentation (1 hour)
2. Copy and customize template (2 hours)
3. Create project-specific docs (2 hours)
4. Build custom toolboxes (2 hours)
5. Test and iterate (1 hour)

**Next:** Onboard team and start sharing threads

### Path 4: Migration from Claude Code (1 week)

**Goal:** Migrate existing Claude Code infrastructure

1. Read AMP_NATIVE_GUIDE.md completely (1 hour)
2. Analyze current Claude Code setup (2 hours)
3. Phase 1: Foundation (1 hour)
4. Phase 2: Convert Skills (2-3 hours)
5. Phase 3: Convert Hooks (1-2 hours)
6. Phase 4: Convert Agents (1 hour)
7. Phase 5: Test and iterate (1-2 hours)
8. Add Oracle/Librarian enhancements (4-6 hours)

**Next:** Team adoption and knowledge sharing

---

## 🎓 Key Differences from Claude Code

### Philosophy

**Claude Code:** Skills + Hooks for auto-activation  
**Amp-Native:** AGENTS.md + Oracle/Librarian for intelligence

### Activation

**Claude Code:** Hooks analyze prompts and activate skills  
**Amp-Native:** Auto-inclusion via globs + Oracle suggests when to activate

### Complex Tasks

**Claude Code:** Agents (subagents)  
**Amp-Native:** Subagents + Oracle for planning + Librarian for research

### Validation

**Claude Code:** Hooks that can block actions  
**Amp-Native:** Toolboxes with rich, actionable feedback

### Knowledge

**Claude Code:** Static skill files  
**Amp-Native:** AGENTS.md + Librarian + shared threads

### Research

**Claude Code:** Manual documentation lookup  
**Amp-Native:** Librarian searches GitHub repos automatically

---

## 📊 Success Metrics

### Adoption Metrics

- [ ] Team members use Oracle regularly
- [ ] Librarian is used for framework research
- [ ] Threads are shared weekly
- [ ] Knowledge base grows monthly
- [ ] AGENTS.md evolves with team learnings

### Quality Metrics

- [ ] Architecture issues caught by Oracle
- [ ] Bugs prevented by toolboxes
- [ ] Time saved by Librarian research
- [ ] Code review quality improvements
- [ ] Reduced onboarding time

### Knowledge Metrics

- [ ] Knowledge docs created
- [ ] Thread shares per month
- [ ] AGENTS.md updates
- [ ] Team guidance additions
- [ ] Reusable patterns documented

---

## 🛠️ Customization Checklist

### Phase 1: Foundation

- [ ] Copy template to project
- [ ] Set up $AMP_TOOLBOX environment variable
- [ ] Make commands and toolboxes executable
- [ ] Test Oracle, Librarian, commands

### Phase 2: Customize

- [ ] Update AGENTS.md with tech stack
- [ ] Update build/test commands
- [ ] Add project-specific patterns
- [ ] Create docs/development/ files

### Phase 3: Extend

- [ ] Add custom toolboxes for your validations
- [ ] Create custom commands for your workflows
- [ ] Build granular guidance files with globs
- [ ] Add Oracle/Librarian hints to guidance

### Phase 4: Team Adoption

- [ ] Onboard team members
- [ ] Share example threads
- [ ] Create first knowledge docs
- [ ] Establish knowledge sharing workflow

---

## 🔗 Quick Links

### Documentation

- [Quick Start (5 min)](AMP_NATIVE_SUMMARY.md)
- [Complete Guide (45 min)](AMP_NATIVE_GUIDE.md)
- [Template Usage (10 min)](amp-native-template/README.md)

### Template Files

- [AGENTS.md](amp-native-template/AGENTS.md)
- [Commands](amp-native-template/.agents/commands/)
- [Toolboxes](amp-native-template/toolbox/)

### External Resources

- [Amp Manual](https://ampcode.com/manual)
- [Oracle Documentation](https://ampcode.com/manual#oracle)
- [Librarian Documentation](https://ampcode.com/manual#librarian)
- [Toolboxes Documentation](https://ampcode.com/manual#toolboxes)

---

## 💡 Pro Tips

### Oracle Usage

1. **Be specific** - Provide files, requirements, concerns
2. **Provide context** - What you're trying to achieve
3. **Use for complex tasks** - Architecture, debugging, planning
4. **Don't overuse** - It's slower and costlier than main agent

### Librarian Usage

1. **Specify repos** - Tell Librarian which repos to search
2. **Be specific** - What exactly are you looking for?
3. **Use for external knowledge** - Framework docs, cross-repo research
4. **Configure private repos** - Connect GitHub for private repo access

### Toolbox Design

1. **Rich feedback** - File names, line numbers, examples
2. **Actionable suggestions** - Tell users how to fix
3. **Clear descriptions** - Make them discoverable
4. **Exit codes** - 0 for success, 1 for failure

### Command Design

1. **Multi-step workflows** - Break down complex tasks
2. **Combine Oracle + Librarian** - Research then plan
3. **Knowledge capture** - Always document learnings
4. **Thread sharing** - Remind users to share

---

## 🎯 Next Steps

### Immediate (Today)

1. Read [AMP_NATIVE_SUMMARY.md](AMP_NATIVE_SUMMARY.md)
2. Copy template to your project
3. Test Oracle and Librarian

### Short-term (This Week)

1. Customize AGENTS.md
2. Create docs/development/ files
3. Test with your team
4. Share first thread

### Long-term (This Month)

1. Build custom toolboxes
2. Create workflow commands
3. Grow knowledge base
4. Measure success metrics

---

## 📞 Support

**Questions?**
1. Check [AMP_NATIVE_GUIDE.md](AMP_NATIVE_GUIDE.md) for detailed docs
2. Review [Amp Manual](https://ampcode.com/manual)
3. Share threads with your team for collaborative problem-solving

**Issues?**
1. Check [amp-native-template/README.md](amp-native-template/README.md) troubleshooting section
2. Verify environment setup ($AMP_TOOLBOX, executable permissions)
3. Test with simple examples first

---

## 🌟 Philosophy

**This is not a Claude Code translation.**

This is an **Amp-first design** that leverages:
- **Oracle's reasoning** for complex decisions
- **Librarian's research** for external knowledge
- **Toolboxes** for intelligent automation
- **Thread sharing** for team learning
- **AGENTS.md** for context-aware guidance

**Embrace Amp's unique capabilities!**

---

**Ready to get started?** → [AMP_NATIVE_SUMMARY.md](AMP_NATIVE_SUMMARY.md)

