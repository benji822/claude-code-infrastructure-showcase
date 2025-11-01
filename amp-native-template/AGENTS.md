# Project Development Guidelines

This project uses [describe your tech stack here - e.g., Node.js/Express/Prisma (backend) and React/MUI v7 (frontend)].

---

## Quick Reference

**Build:** `npm run build`  
**Test:** `npm test`  
**Dev:** `npm run dev`  
**Lint:** `npm run lint`

---

## Architecture Overview

We use layered architecture:

```
Routes → Controllers → Services → Repositories → Database
```

**Key Principles:**
- Separation of concerns
- Dependency injection
- Test-driven development
- Type safety with TypeScript

---

## Getting Detailed Guidance

For specific development patterns, see:

- **@docs/development/backend.md** - Backend development patterns
- **@docs/development/frontend.md** - Frontend development patterns
- **@docs/development/testing.md** - Testing guidelines
- **@docs/development/oracle-workflows.md** - Oracle usage patterns
- **@docs/development/librarian-patterns.md** - Librarian integration

These files are automatically included when you work on relevant file types.

---

## When to Use Oracle (GPT-5)

Oracle is a "second opinion" model that excels at complex reasoning. Use Oracle for:

### Architecture & Design
```
"Use Oracle to review this API design:
- Files: [list relevant files]
- Requirements: [what you're trying to achieve]
- Concerns: [security, scalability, maintainability, etc.]"
```

### Complex Debugging
```
"Ask Oracle to help debug this issue:
- Error: [error message]
- Files: [affected files]
- Context: [what changed, what you've tried]
- Expected: [expected behavior]"
```

### Planning & Refactoring
```
"Work with Oracle to plan this refactoring:
- Current state: [describe current code]
- Goal: [what you want to achieve]
- Constraints: [backwards compatibility, performance, etc.]"
```

### Code Review
```
"Use Oracle to review my recent changes:
- Focus: [security, performance, architecture, all]
- Files: [list files or use 'git diff']"
```

**When NOT to use Oracle:**
- Simple code edits
- Straightforward bug fixes
- Basic questions (use Librarian or docs instead)

---

## When to Use Librarian

Librarian searches GitHub repositories (public + your configured private repos) for documentation and examples. Use Librarian for:

### Framework Documentation
```
"Ask Librarian about MUI v7 Grid component:
- Search mui/material-ui repo
- Find API documentation
- Show migration examples from v6"
```

### Cross-Repository Research
```
"Use Librarian to find how we handle auth in other services:
- Search our microservices repos
- Find JWT implementation
- Show middleware patterns"
```

### Best Practices Lookup
```
"Librarian, find Prisma transaction patterns:
- Search prisma/prisma repo
- Find best practices
- Show error handling examples"
```

### Debugging with External Context
```
"Ask Librarian to research this framework issue:
- Search [framework] repo for similar bugs
- Find the source code causing this
- Show workarounds or fixes"
```

**When NOT to use Librarian:**
- Questions about your own codebase (use codebase search)
- Vague questions without specific repos/topics
- Private repos you haven't configured access for

---

## Toolboxes

Toolboxes are project-specific automation scripts. Available toolboxes:

- **validate-architecture** - Validates layered architecture
- **validate-types** - TypeScript type checking with rich feedback
- **run-tests-smart** - Intelligent test runner
- **oracle-review** - Triggers Oracle review of changes

Amp discovers toolboxes automatically. They provide rich, actionable feedback.

---

## Custom Commands

Press **Ctrl-O** (CLI) or **Cmd-Shift-A** (editor) to access custom commands:

- **architecture-review** - Oracle-powered architecture review
- **research-framework** - Librarian-based framework research
- **debug-with-research** - Combined Oracle + Librarian debugging
- **capture-knowledge** - Document solutions for the team

---

## Workflow Examples

### Example 1: Implementing a New Feature

1. **Research** (Librarian)
   ```
   "I need to implement [feature]. Ask Librarian to:
   - Search [framework] repo for examples
   - Find best practices
   - Show common patterns"
   ```

2. **Plan** (Oracle)
   ```
   "Based on Librarian's findings, use Oracle to plan:
   - Component/service structure
   - Data flow
   - Error handling
   - Testing strategy"
   ```

3. **Implement** (Main Agent)
   ```
   "Implement based on Oracle's plan"
   ```

4. **Review** (Oracle)
   ```
   "Use Oracle to review the implementation:
   - Code quality
   - Edge cases
   - Performance
   - Security"
   ```

5. **Document** (Knowledge Capture)
   ```
   "Run capture-knowledge command to document this for the team"
   ```

### Example 2: Debugging a Complex Issue

1. **Reproduce** (Main Agent)
   - Run tests
   - Capture error messages
   - Identify affected files

2. **Analyze** (Oracle)
   ```
   "Use Oracle to analyze this bug:
   - Error: [details]
   - Files: [list]
   - Context: [recent changes]"
   ```

3. **Research** (Librarian - if framework issue)
   ```
   "Ask Librarian to search [framework] repo for:
   - Similar issues
   - Source code
   - Fixes or workarounds"
   ```

4. **Fix** (Main Agent + Oracle Review)
   ```
   "Implement fix based on findings.
   Then use Oracle to review for edge cases."
   ```

### Example 3: Architecture Review

1. **Run Command**
   ```
   "Run architecture-review command"
   ```

2. **Oracle Analysis**
   - Oracle reviews architecture
   - Identifies issues
   - Suggests improvements

3. **Prioritize**
   - Critical (fix immediately)
   - High (fix this sprint)
   - Medium (fix this quarter)
   - Low (technical debt)

4. **Document**
   - Capture decisions
   - Update AGENTS.md if patterns emerge
   - Share thread with team

---

## Team Knowledge Sharing

### Sharing Threads

When you solve a complex problem:

1. Use `capture-knowledge` command to document
2. Set thread visibility to "Workspace-shared"
3. Add thread link to knowledge doc
4. Share in team chat

This way, teammates can see both the documentation AND the full conversation.

### Growing the Knowledge Base

As patterns emerge:
- Update AGENTS.md with new guidance
- Add files to docs/development/
- Create new toolboxes for common validations
- Add custom commands for frequent workflows

---

## Common Patterns

### Backend Development
- See @docs/development/backend.md (auto-included for backend files)
- Layered architecture: Routes → Controllers → Services → Repositories
- Use Oracle for service layer design
- Use Librarian for framework patterns

### Frontend Development
- See @docs/development/frontend.md (auto-included for frontend files)
- Component-based architecture
- Use Oracle for component design
- Use Librarian for MUI/React patterns

### Testing
- See @docs/development/testing.md (auto-included for test files)
- Unit tests for services
- Integration tests for APIs
- Component tests for React
- Use Oracle to review test coverage

---

## Getting Help

**For framework questions:** Ask Librarian  
**For architecture decisions:** Use Oracle  
**For debugging:** Oracle + Librarian workflow  
**For team knowledge:** Check docs/knowledge/ and shared threads  
**For project patterns:** This AGENTS.md and @docs/development/

---

## Next Steps

1. Customize this file for your project
2. Add your tech stack details
3. Create docs/development/ files for your patterns
4. Set up toolboxes for your validations
5. Create custom commands for your workflows
6. Start sharing threads with your team

