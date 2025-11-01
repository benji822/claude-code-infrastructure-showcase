# Amp-Native Development Infrastructure

**Building intelligent development workflows with Amp's unique capabilities**

---

## Philosophy: Amp-First Design

This guide presents a **ground-up redesign** of development infrastructure patterns specifically for Amp, rather than translating Claude Code concepts.

### The Amp Advantage

Amp provides unique capabilities that enable fundamentally different approaches:

1. **Oracle (GPT-5)** - A "second opinion" model for complex reasoning
2. **Librarian** - Cross-repository and framework documentation research
3. **Toolboxes** - Project-specific automation with rich feedback
4. **AGENTS.md Ecosystem** - Hierarchical, context-aware guidance
5. **Thread Sharing** - Team knowledge captured in shareable conversations

### Core Principles (From Original Showcase)

✅ Auto-activation of relevant guidance
✅ Progressive disclosure of information
✅ Specialized agents for complex tasks
✅ Developer workflow automation
✅ Team-wide knowledge sharing

### Amp-Native Enhancements

🚀 **Oracle-Powered Reviews** - GPT-5 for architecture analysis and debugging
🚀 **Librarian Integration** - External documentation and cross-repo research
🚀 **Intelligent Toolboxes** - Context-aware automation with actionable feedback
🚀 **Command Orchestration** - Multi-step workflows invoking Oracle/Librarian
🚀 **Thread-Based Learning** - Capture and share team knowledge

---

## Architecture Overview

```
Amp-Native Infrastructure
│
├── AGENTS.md Hierarchy
│   ├── Root AGENTS.md (always included)
│   ├── Subtree AGENTS.md (context-specific)
│   └── Granular guidance files (glob-based)
│
├── Oracle Integration
│   ├── Architecture reviews
│   ├── Complex debugging
│   └── Planning and design
│
├── Librarian Integration
│   ├── Framework documentation
│   ├── Cross-repo research
│   └── Best practices lookup
│
├── Toolboxes
│   ├── Project-specific automation
│   ├── Validation with feedback
│   └── Workflow orchestration
│
└── Custom Commands
    ├── Workflow orchestrators
    ├── Oracle/Librarian invokers
    └── Team knowledge capture
```

---

## Part 1: Intelligent Context System

### 1.1 AGENTS.md Hierarchy

**Root AGENTS.md** - High-level project overview:

```markdown
# Project Development Guidelines

This project uses Node.js/Express/Prisma (backend) and React/MUI v7 (frontend).

## Quick Reference

- Build: `npm run build`
- Test: `npm test`
- Dev: `npm run dev`

## Architecture

We use layered architecture: Routes → Controllers → Services → Repositories

## Getting Detailed Guidance

For specific patterns, see:
- @docs/development/backend.md - Backend development
- @docs/development/frontend.md - Frontend development
- @docs/development/testing.md - Testing guidelines

## When to Use Oracle

Use Oracle (GPT-5) for:
- Architecture reviews: "Use Oracle to review this design"
- Complex debugging: "Ask Oracle to help debug this issue"
- Planning: "Work with Oracle to plan this refactoring"

## When to Use Librarian

Use Librarian for:
- Framework docs: "Ask Librarian about MUI v7 Grid component"
- Cross-repo research: "Use Librarian to find how we handle auth in other services"
- Best practices: "Librarian, show me Prisma transaction patterns"
```

### 1.2 Granular Guidance with Oracle Hints

**docs/development/backend.md:**

```yaml
---
globs:
  - 'backend/**/*.ts'
  - 'src/api/**/*.ts'
---

# Backend Development Guidelines

## Architecture

Layered architecture: Routes → Controllers → Services → Repositories

## When to Invoke Oracle

For backend work, consider using Oracle when:
- Designing new API endpoints (complex business logic)
- Debugging performance issues
- Reviewing database query patterns
- Planning major refactorings

Example: "Use Oracle to review this service layer design"

## Routing Patterns

See @docs/development/backend/routing.md

## Service Patterns

See @docs/development/backend/services.md

## Database Patterns

See @docs/development/backend/database.md
```

### 1.3 Oracle-Powered Architecture Reviews

**docs/development/oracle-workflows.md:**

```yaml
---
globs:
  - '**/docs/**'
  - 'architecture/**'
---

# Oracle Workflows

## Architecture Review Workflow

When reviewing architecture:

1. **Initial Analysis** (Main Agent)
   - Gather relevant files
   - Identify key components
   - Note potential issues

2. **Deep Review** (Oracle)
   - "Use Oracle to review this architecture for:
     - Scalability concerns
     - Security vulnerabilities
     - Maintainability issues
     - Performance bottlenecks"

3. **Recommendations** (Oracle)
   - "Ask Oracle to suggest specific improvements with code examples"

## Complex Debugging Workflow

For difficult bugs:

1. **Reproduce** (Main Agent)
   - Run tests
   - Capture error messages
   - Identify affected files

2. **Root Cause Analysis** (Oracle)
   - "Use Oracle to analyze this bug. Files: [list]
     Error: [error message]
     Expected: [expected behavior]"

3. **Solution Design** (Oracle + Main Agent)
   - Oracle designs solution
   - Main agent implements
   - Oracle reviews implementation
```

---

## Part 2: Librarian Integration

### 2.1 Framework Documentation Access

**docs/development/librarian-patterns.md:**

```yaml
---
globs:
  - '**/*.tsx'
  - '**/*.ts'
---

# Librarian Integration Patterns

## When to Use Librarian

### Framework Documentation
- "Ask Librarian about MUI v7 Grid component API changes"
- "Librarian, show me React 18 concurrent features"
- "Use Librarian to find Prisma best practices for transactions"

### Cross-Repository Research
- "Librarian, search our auth-service repo for JWT implementation"
- "Ask Librarian how we handle rate limiting in api-gateway"
- "Use Librarian to find error handling patterns across our services"

### Best Practices Lookup
- "Librarian, find TypeScript strict mode patterns in popular repos"
- "Ask Librarian for React Testing Library best practices"
- "Use Librarian to research GraphQL schema design patterns"

## Librarian Workflow Examples

### Example 1: Framework Migration
```
"I'm migrating from MUI v6 to v7. Ask Librarian to:
1. Find breaking changes in MUI v7
2. Show migration examples from the MUI repo
3. Identify common pitfalls in Grid component migration"
```

### Example 2: Cross-Repo Pattern Research
```
"We need to implement feature flags. Use Librarian to:
1. Search our microservices repos for existing implementations
2. Find the most recent feature flag pattern we used
3. Show me the configuration approach from service-config repo"
```

### Example 3: Debugging with External Context
```
"This Zod validation is failing with a weird error. Ask Librarian to:
1. Search the Zod repo for similar issues
2. Find the source code causing this error
3. Show me the correct usage pattern"
```
```

### 2.2 Librarian + Oracle Combination

**docs/development/advanced-workflows.md:**

```markdown
# Advanced Workflows: Oracle + Librarian

## Pattern: Research → Plan → Implement

### Step 1: Research (Librarian)
```
"Use Librarian to research how Next.js handles server-side auth.
Search: vercel/next.js, nextauthjs/next-auth
Focus on: middleware patterns, session management"
```

### Step 2: Plan (Oracle)
```
"Based on Librarian's findings, use Oracle to plan our auth implementation:
- Adapt Next.js patterns to our Express backend
- Design session management strategy
- Identify security considerations"
```

### Step 3: Implement (Main Agent)
```
"Implement the auth system based on Oracle's plan.
Reference Librarian's findings for specific patterns."
```

## Pattern: Debug → Research → Fix

### Step 1: Debug (Oracle)
```
"Use Oracle to analyze this bug:
[error details]
[affected files]
[expected vs actual behavior]"
```

### Step 2: Research (Librarian)
```
"Oracle identified this might be a framework issue.
Ask Librarian to search the framework repo for:
- Similar bug reports
- Recent fixes
- Workarounds"
```

### Step 3: Fix (Main Agent + Oracle Review)
```
"Implement the fix based on Librarian's findings.
Then use Oracle to review the fix for edge cases."
```
```

---

## Part 3: Advanced Toolboxes

### 3.1 Intelligent Validation Toolbox

**$AMP_TOOLBOX/validate-architecture:**

```bash
#!/usr/bin/env node

const action = process.env.TOOLBOX_ACTION;

if (action === 'describe') {
  console.log([
    'name: validate-architecture',
    'description: Validates codebase architecture and provides actionable feedback',
    'dir: string the workspace directory to validate',
  ].join('\n'));
  process.exit(0);
}

if (action === 'execute') {
  const fs = require('fs');
  const path = require('path');

  // Read parameters
  const input = fs.readFileSync(0, 'utf-8');
  const dirMatch = input.match(/dir: (.+)/);
  const dir = dirMatch ? dirMatch[1] : '.';

  // Validation logic
  const issues = [];

  // Check layered architecture
  const routesDir = path.join(dir, 'backend/routes');
  const controllersDir = path.join(dir, 'backend/controllers');

  if (fs.existsSync(routesDir)) {
    const routes = fs.readdirSync(routesDir);
    routes.forEach(file => {
      const content = fs.readFileSync(path.join(routesDir, file), 'utf-8');

      // Check for business logic in routes
      if (content.includes('prisma.') && !content.includes('controller.')) {
        issues.push({
          severity: 'high',
          file: `backend/routes/${file}`,
          issue: 'Direct database access in route file',
          suggestion: 'Move database logic to service layer',
          example: 'Create a service method and call it from controller'
        });
      }
    });
  }

  // Output structured feedback
  if (issues.length > 0) {
    console.log('\n=== Architecture Validation Issues ===\n');
    issues.forEach((issue, i) => {
      console.log(`${i + 1}. [${issue.severity.toUpperCase()}] ${issue.file}`);
      console.log(`   Issue: ${issue.issue}`);
      console.log(`   Suggestion: ${issue.suggestion}`);
      console.log(`   Example: ${issue.example}\n`);
    });
    process.exit(1);
  } else {
    console.log('✓ Architecture validation passed');
    process.exit(0);
  }
}
```

### 3.2 Oracle-Invoking Toolbox

**$AMP_TOOLBOX/oracle-review:**

```bash
#!/usr/bin/env bash

if [ "$TOOLBOX_ACTION" = "describe" ]; then
  cat << EOF
name: oracle-review
description: Triggers an Oracle review of recent changes with structured prompts
scope: string what to review (commit|staged|file)
focus: string what to focus on (security|performance|architecture|all)
EOF
  exit 0
fi

if [ "$TOOLBOX_ACTION" = "execute" ]; then
  # Read parameters
  SCOPE=$(grep "^scope:" | cut -d' ' -f2-)
  FOCUS=$(grep "^focus:" | cut -d' ' -f2-)

  # Build Oracle prompt based on scope and focus
  case "$SCOPE" in
    commit)
      CHANGES=$(git show HEAD)
      ;;
    staged)
      CHANGES=$(git diff --staged)
      ;;
    file)
      CHANGES=$(git diff)
      ;;
  esac

  # Output prompt for Oracle
  cat << EOF
Use Oracle to review these changes:

$CHANGES

Focus areas: $FOCUS

Oracle should analyze:
- Code quality and maintainability
- Potential bugs or edge cases
- Security vulnerabilities
- Performance implications
- Architecture consistency

Provide specific, actionable feedback with line numbers.
EOF
fi
```

---

## Part 4: Orchestrating Custom Commands

### 4.1 Oracle-Powered Architecture Review Command

**.agents/commands/architecture-review:**

```bash
#!/usr/bin/env bash

cat << 'EOF'
# Architecture Review Workflow

I'll conduct a comprehensive architecture review using Oracle.

## Phase 1: Gather Context

First, I'll identify the key architectural components:
- Main entry points
- Core business logic
- Data models
- External dependencies

## Phase 2: Oracle Analysis

Then I'll use Oracle to analyze:

"Use Oracle to review this codebase architecture. Focus on:

1. **Layering**: Are concerns properly separated?
2. **Dependencies**: Are dependencies well-managed?
3. **Scalability**: Can this scale horizontally?
4. **Security**: Are there security vulnerabilities?
5. **Maintainability**: Is the code maintainable?

Provide specific issues with file names and line numbers.
Suggest concrete improvements with code examples."

## Phase 3: Detailed Analysis

For each issue Oracle identifies, I'll:
1. Show the problematic code
2. Explain why it's an issue
3. Provide a refactored example
4. Estimate effort to fix

## Phase 4: Prioritized Recommendations

Finally, I'll create a prioritized action plan:
- Critical (fix immediately)
- High (fix this sprint)
- Medium (fix this quarter)
- Low (technical debt)

Ready to proceed with the review?
EOF
```

### 4.2 Librarian Research Command

**.agents/commands/research-framework:**

```bash
#!/usr/bin/env bash

FRAMEWORK="$1"
TOPIC="$2"

cat << EOF
# Framework Research: $FRAMEWORK - $TOPIC

I'll use Librarian to research this topic comprehensively.

## Phase 1: Official Documentation

"Ask Librarian to search the official $FRAMEWORK repository for:
- Documentation on $TOPIC
- Code examples
- Best practices
- Common pitfalls"

## Phase 2: Real-World Usage

"Use Librarian to find how popular projects use $FRAMEWORK for $TOPIC:
- Search top 10 starred repos using $FRAMEWORK
- Find $TOPIC implementations
- Identify common patterns"

## Phase 3: Recent Changes

"Ask Librarian to check for recent changes:
- Breaking changes in latest versions
- New features related to $TOPIC
- Migration guides"

## Phase 4: Synthesis

I'll synthesize Librarian's findings into:
1. Recommended approach for our project
2. Code examples adapted to our stack
3. Migration plan if needed
4. Potential issues to watch for

Proceeding with research...
EOF
```

### 4.3 Combined Oracle + Librarian Workflow

**.agents/commands/debug-with-research:**

```bash
#!/usr/bin/env bash

cat << 'EOF'
# Advanced Debugging Workflow

This command combines Oracle's reasoning with Librarian's research capabilities.

## Step 1: Initial Analysis (Main Agent)

I'll gather:
- Error messages and stack traces
- Affected files
- Recent changes
- Reproduction steps

## Step 2: Root Cause Analysis (Oracle)

"Use Oracle to analyze this bug:

Error: [error details]
Files: [affected files]
Context: [recent changes]

Oracle should:
1. Identify the root cause
2. Explain why it's happening
3. Suggest potential fixes
4. Identify if this might be a framework issue"

## Step 3: External Research (Librarian)

If Oracle suspects a framework issue:

"Ask Librarian to research this in the framework repository:
- Search for similar issues
- Find the source code causing this
- Check for known bugs or fixes
- Look for workarounds"

## Step 4: Solution Design (Oracle)

"Based on Librarian's findings, use Oracle to design a fix:
- Adapt framework solutions to our codebase
- Consider edge cases
- Plan testing strategy
- Identify potential side effects"

## Step 5: Implementation & Verification

I'll implement the fix and verify:
- Run existing tests
- Add new tests for this bug
- Check for regressions
- Document the fix

Ready to start debugging?
EOF
```

---

## Part 5: Thread-Based Knowledge Capture

### 5.1 Knowledge Capture Command

**.agents/commands/capture-knowledge:**

```bash
#!/usr/bin/env bash

TOPIC="$1"

cat << EOF
# Knowledge Capture: $TOPIC

I'll document this solution for the team.

## What I'll Create

1. **Problem Statement**
   - What issue were we solving?
   - Why was it challenging?
   - What approaches did we try?

2. **Solution Overview**
   - Final approach
   - Key decisions
   - Trade-offs made

3. **Implementation Details**
   - Code changes
   - Configuration updates
   - Dependencies added

4. **Testing Strategy**
   - How to verify it works
   - Edge cases covered
   - Performance impact

5. **Team Guidance**
   - When to use this pattern
   - When NOT to use it
   - Common pitfalls

## Where to Save

I'll create: \`docs/knowledge/$TOPIC.md\`

And add a reference in AGENTS.md so future work automatically includes this knowledge.

## Thread Sharing

After documenting, I'll remind you to:
1. Set thread visibility to "Workspace-shared"
2. Add thread link to the knowledge doc
3. Share in team chat

This way, teammates can see both the documentation AND the full conversation that led to the solution.

Proceeding with knowledge capture...
EOF
```

---

## Part 6: Implementation Examples

### 6.1 Complete Backend Guidance with Oracle Integration

**docs/development/backend.md:**

```yaml
---
globs:
  - 'backend/**/*.ts'
  - 'src/api/**/*.ts'
  - 'server/**/*.ts'
---

# Backend Development Guidelines

## Architecture: Layered Approach

```
Routes → Controllers → Services → Repositories → Database
```

## Oracle-Assisted Development

### When to Use Oracle for Backend Work

**Architecture Decisions:**
```
"Use Oracle to review this API design:
- RESTful endpoint structure
- Request/response schemas
- Error handling strategy
- Authentication flow"
```

**Performance Optimization:**
```
"Ask Oracle to analyze these database queries for:
- N+1 query problems
- Missing indexes
- Inefficient joins
- Caching opportunities"
```

**Security Review:**
```
"Use Oracle to review security:
- Input validation
- SQL injection risks
- Authentication/authorization
- Data exposure"
```

## Librarian-Assisted Development

### Framework Documentation

**Prisma Patterns:**
```
"Ask Librarian about Prisma transaction patterns:
- Search prisma/prisma repo
- Find transaction best practices
- Show error handling examples"
```

**Express Middleware:**
```
"Use Librarian to research Express middleware patterns:
- Authentication middleware
- Error handling middleware
- Request validation"
```

## Routing Patterns

**Standard Route Structure:**
```typescript
// routes/posts.ts
import { Router } from 'express';
import { PostController } from '../controllers/PostController';

const router = Router();
const controller = new PostController();

router.get('/', controller.list);
router.get('/:id', controller.get);
router.post('/', controller.create);
router.put('/:id', controller.update);
router.delete('/:id', controller.delete);

export default router;
```

**When to Ask Oracle:**
- Complex routing logic
- API versioning strategy
- Rate limiting implementation

## Service Layer Patterns

**Standard Service Structure:**
```typescript
// services/PostService.ts
import { PostRepository } from '../repositories/PostRepository';
import { CreatePostDto, UpdatePostDto } from '../types';

export class PostService {
  private repo = new PostRepository();

  async list() {
    return this.repo.findAll();
  }

  async create(data: CreatePostDto) {
    // Business logic here
    this.validatePost(data);
    return this.repo.create(data);
  }

  private validatePost(data: CreatePostDto) {
    // Validation logic
  }
}
```

**When to Use Oracle:**
```
"Use Oracle to review this service layer:
- Is business logic properly separated?
- Are there missing validations?
- Could this be more testable?"
```

## Database Patterns

**Transaction Handling:**
```typescript
// Use Prisma transactions for multi-step operations
await prisma.$transaction(async (tx) => {
  const post = await tx.post.create({ data: postData });
  await tx.audit.create({
    data: { action: 'POST_CREATED', postId: post.id }
  });
});
```

**When to Ask Librarian:**
```
"Ask Librarian about Prisma transaction patterns:
- Nested transactions
- Error handling
- Performance implications"
```

## Testing with Oracle

**Test Review:**
```
"Use Oracle to review these tests:
- Coverage of edge cases
- Test quality and maintainability
- Missing test scenarios"
```

## Common Mistakes (Oracle Can Catch)

❌ Business logic in routes
❌ Direct database access in controllers
❌ Missing error handling
❌ No input validation
❌ Exposing internal errors

**Oracle Review Command:**
```
"Use Oracle to check for these anti-patterns in my recent changes"
```

---

For more specific patterns:
- @docs/development/backend/routing.md
- @docs/development/backend/services.md
- @docs/development/backend/database.md
```

### 6.2 Frontend Guidance with Librarian Integration

**docs/development/frontend.md:**

```yaml
---
globs:
  - 'frontend/**/*.tsx'
  - 'src/components/**/*.tsx'
  - 'client/**/*.tsx'
---

# Frontend Development Guidelines

## Framework Stack

- React 18 (concurrent features)
- MUI v7 (Material-UI)
- TanStack Query (data fetching)
- React Hook Form (forms)

## Librarian for Framework Research

### MUI v7 Patterns

**When migrating or using new components:**
```
"Ask Librarian about MUI v7 Grid component:
- Search mui/material-ui repo
- Find Grid API documentation
- Show migration examples from v6 to v7
- Identify breaking changes"
```

**Common Librarian Queries:**
```
"Librarian, show me MUI v7 theming best practices"
"Ask Librarian for MUI v7 responsive design patterns"
"Use Librarian to find MUI v7 form validation examples"
```

### React 18 Patterns

**Concurrent Features:**
```
"Ask Librarian about React 18 concurrent features:
- useTransition usage
- useDeferredValue patterns
- Suspense best practices"
```

## Oracle for Component Design

### Component Architecture Review

```
"Use Oracle to review this component architecture:
- Component composition
- Props design
- State management
- Performance considerations"
```

### Performance Analysis

```
"Ask Oracle to analyze component performance:
- Unnecessary re-renders
- Memoization opportunities
- Code splitting strategy"
```

## Component Patterns

**Standard Component Structure:**
```typescript
import { FC } from 'react';
import { Box, Typography } from '@mui/material';

interface PostCardProps {
  title: string;
  content: string;
  onEdit: (id: string) => void;
}

export const PostCard: FC<PostCardProps> = ({
  title,
  content,
  onEdit
}) => {
  return (
    <Box sx={{ p: 2, border: 1, borderColor: 'divider' }}>
      <Typography variant="h6">{title}</Typography>
      <Typography variant="body2">{content}</Typography>
    </Box>
  );
};
```

## Data Fetching with TanStack Query

**Standard Query Pattern:**
```typescript
import { useQuery } from '@tanstack/react-query';

export const usePosts = () => {
  return useQuery({
    queryKey: ['posts'],
    queryFn: async () => {
      const res = await fetch('/api/posts');
      return res.json();
    },
  });
};
```

**When to Ask Librarian:**
```
"Ask Librarian about TanStack Query patterns:
- Search TanStack/query repo
- Find caching strategies
- Show optimistic update examples"
```

## Oracle + Librarian Workflow

### Example: Implementing New Feature

**Step 1: Research (Librarian)**
```
"I need to implement infinite scroll with TanStack Query.
Ask Librarian to:
1. Search TanStack/query for infinite query examples
2. Find MUI v7 virtualization patterns
3. Show performance best practices"
```

**Step 2: Design (Oracle)**
```
"Based on Librarian's findings, use Oracle to design:
- Component structure
- State management approach
- Performance optimizations
- Error handling strategy"
```

**Step 3: Review (Oracle)**
```
"After implementation, use Oracle to review:
- Code quality
- Performance implications
- Accessibility
- Edge cases"
```

---

For more specific patterns:
- @docs/development/frontend/components.md
- @docs/development/frontend/data-fetching.md
- @docs/development/frontend/styling.md
```

---

## Part 7: Migration Strategy

### 7.1 From Claude Code to Amp-Native

**Phase 1: Foundation (1 hour)**

1. **Create Root AGENTS.md**
   ```bash
   # Copy template
   cp amp-native-template/AGENTS.md .

   # Customize for your project
   # - Update tech stack
   # - Add build/test commands
   # - Add Oracle/Librarian guidance
   ```

2. **Set Up Toolbox Directory**
   ```bash
   export AMP_TOOLBOX=~/.config/amp/toolbox
   mkdir -p $AMP_TOOLBOX

   # Copy validation toolboxes
   cp amp-native-template/toolbox/* $AMP_TOOLBOX/
   chmod +x $AMP_TOOLBOX/*
   ```

3. **Create Custom Commands**
   ```bash
   mkdir -p .agents/commands
   cp amp-native-template/commands/* .agents/commands/
   chmod +x .agents/commands/*
   ```

**Phase 2: Convert Skills (2-3 hours)**

For each Claude Code skill:

1. **Identify Core Patterns**
   - What guidance does this skill provide?
   - When should it activate?
   - What resources does it reference?

2. **Create Granular Guidance File**
   ```bash
   # Example: backend-dev-guidelines skill
   mkdir -p docs/development

   # Create main guidance file with globs
   cat > docs/development/backend.md << 'EOF'
   ---
   globs:
     - 'backend/**/*.ts'
   ---

   # Backend Development Guidelines
   [Content from SKILL.md]

   ## Oracle Integration
   [Add Oracle usage guidance]

   ## Librarian Integration
   [Add Librarian usage guidance]
   EOF
   ```

3. **Add Oracle/Librarian Enhancements**
   - Identify where Oracle would help (architecture, debugging)
   - Identify where Librarian would help (framework docs, cross-repo)
   - Add specific prompts for each

**Phase 3: Convert Hooks to Toolboxes (1-2 hours)**

For each Claude Code hook:

1. **Analyze Hook Purpose**
   - What does this hook do?
   - When does it run?
   - What feedback does it provide?

2. **Create Equivalent Toolbox**
   ```bash
   # Example: tsc-check hook → validate-types toolbox
   cat > $AMP_TOOLBOX/validate-types << 'EOF'
   #!/usr/bin/env node

   if (process.env.TOOLBOX_ACTION === 'describe') {
     console.log([
       'name: validate-types',
       'description: Validates TypeScript types and provides actionable feedback',
       'dir: string workspace directory'
     ].join('\n'));
     process.exit(0);
   }

   // Implementation with rich feedback
   EOF

   chmod +x $AMP_TOOLBOX/validate-types
   ```

3. **Enhance with Oracle**
   - Add Oracle invocation for complex type errors
   - Provide structured, actionable feedback

**Phase 4: Convert Agents to Commands (1 hour)**

For each Claude Code agent:

1. **Create Orchestrating Command**
   ```bash
   # Example: code-architecture-reviewer agent
   cat > .agents/commands/architecture-review << 'EOF'
   #!/usr/bin/env bash

   cat << 'PROMPT'
   # Architecture Review Workflow

   I'll use Oracle to conduct a comprehensive review...
   [Workflow steps]
   PROMPT
   EOF

   chmod +x .agents/commands/architecture-review
   ```

2. **Add Oracle/Librarian Integration**
   - Oracle for analysis and planning
   - Librarian for research
   - Subagents for parallel work

**Phase 5: Test and Iterate (1-2 hours)**

1. **Test Auto-Activation**
   ```bash
   # Edit different file types
   code backend/routes/posts.ts
   # Verify backend.md is included

   code frontend/components/Button.tsx
   # Verify frontend.md is included
   ```

2. **Test Oracle Integration**
   ```bash
   amp
   # Try: "Use Oracle to review this architecture"
   # Verify Oracle is invoked correctly
   ```

3. **Test Librarian Integration**
   ```bash
   amp
   # Try: "Ask Librarian about MUI v7 Grid component"
   # Verify Librarian searches correctly
   ```

4. **Test Toolboxes**
   ```bash
   amp
   # Amp should discover toolboxes automatically
   # Try triggering validation
   ```

5. **Test Custom Commands**
   ```bash
   amp
   # Press Ctrl-O (CLI) or Cmd-Shift-A (editor)
   # Verify commands appear
   # Test command execution
   ```

---

## Part 8: Best Practices

### 8.1 Oracle Usage Patterns

**DO:**
✅ Use Oracle for complex architecture decisions
✅ Use Oracle for debugging difficult issues
✅ Use Oracle for planning major refactorings
✅ Be specific about what Oracle should analyze
✅ Provide context (files, errors, requirements)

**DON'T:**
❌ Use Oracle for simple code edits
❌ Use Oracle without providing context
❌ Expect Oracle to read your mind
❌ Use Oracle for every single task (it's slower/costlier)

**Example Good Oracle Prompts:**
```
"Use Oracle to review this authentication system design:
- Files: auth/service.ts, auth/middleware.ts
- Requirements: JWT-based, refresh tokens, role-based access
- Concerns: Security, scalability, maintainability"
```

```
"Ask Oracle to debug this performance issue:
- Symptom: API response time increased from 100ms to 2s
- Affected endpoint: GET /api/posts
- Recent changes: Added pagination, changed query
- Database: PostgreSQL with Prisma"
```

### 8.2 Librarian Usage Patterns

**DO:**
✅ Use Librarian for framework documentation
✅ Use Librarian for cross-repo research
✅ Use Librarian to find real-world examples
✅ Specify which repos to search
✅ Be specific about what you're looking for

**DON'T:**
❌ Use Librarian for your own codebase (use codebase search)
❌ Ask Librarian vague questions
❌ Expect Librarian to know private repo details (configure access first)

**Example Good Librarian Prompts:**
```
"Ask Librarian to search the MUI repo for Grid v7 examples:
- Focus on responsive layouts
- Show size prop usage
- Find migration guides from v6"
```

```
"Use Librarian to research how Next.js handles middleware:
- Search vercel/next.js repo
- Find authentication middleware examples
- Show edge runtime patterns"
```

### 8.3 Toolbox Design Patterns

**Provide Rich Feedback:**
```javascript
// Good: Actionable feedback
console.log(`
❌ Issue: Direct database access in route file
📁 File: backend/routes/posts.ts:45
💡 Suggestion: Move to PostService
📝 Example:
   // In PostService.ts
   async createPost(data) {
     return this.repo.create(data);
   }
`);

// Bad: Generic error
console.log('Validation failed');
```

**Make Toolboxes Discoverable:**
```javascript
// Good: Clear description
if (action === 'describe') {
  console.log([
    'name: validate-architecture',
    'description: Validates layered architecture and provides specific fix suggestions',
    'dir: string workspace directory to validate'
  ].join('\n'));
}
```

### 8.4 Command Orchestration Patterns

**Multi-Step Workflows:**
```bash
# Good: Clear phases with Oracle/Librarian integration
cat << 'EOF'
## Phase 1: Research (Librarian)
"Ask Librarian to..."

## Phase 2: Plan (Oracle)
"Use Oracle to design..."

## Phase 3: Implement (Main Agent)
"Implement based on Oracle's plan..."

## Phase 4: Review (Oracle)
"Use Oracle to review..."
EOF
```

**Capture Knowledge:**
```bash
# Always include knowledge capture
cat << 'EOF'
## Final Step: Document

I'll create docs/knowledge/[topic].md with:
- Problem statement
- Solution approach
- Implementation details
- Team guidance

Then remind you to share this thread with the team.
EOF
```

---

## Part 9: Team Adoption

### 9.1 Onboarding Checklist

**For Each Team Member:**

- [ ] Install Amp and configure workspace
- [ ] Set up `$AMP_TOOLBOX` environment variable
- [ ] Clone project and verify AGENTS.md is present
- [ ] Test Oracle: "Use Oracle to review [something]"
- [ ] Test Librarian: "Ask Librarian about [framework]"
- [ ] Test custom commands (Ctrl-O or Cmd-Shift-A)
- [ ] Review shared threads from team
- [ ] Create first knowledge-capture thread

### 9.2 Team Workflows

**Knowledge Sharing:**
1. Solve a problem using Oracle/Librarian
2. Use `capture-knowledge` command
3. Set thread to "Workspace-shared"
4. Add thread link to knowledge doc
5. Share in team chat

**Code Reviews:**
1. Use `architecture-review` command
2. Oracle reviews changes
3. Share thread with reviewer
4. Discuss Oracle's findings
5. Capture decisions in knowledge base

**Debugging Sessions:**
1. Use `debug-with-research` command
2. Oracle analyzes, Librarian researches
3. Share thread with team
4. Document solution
5. Update AGENTS.md if pattern emerges

---

## Part 10: Measuring Success

### 10.1 Metrics to Track

**Adoption Metrics:**
- % of team using Oracle regularly
- % of team using Librarian
- Number of shared threads per week
- Number of knowledge docs created

**Quality Metrics:**
- Architecture issues caught by Oracle
- Bugs prevented by validation toolboxes
- Time saved by Librarian research
- Code review quality improvements

**Knowledge Metrics:**
- Knowledge docs created
- Thread shares per month
- AGENTS.md updates
- Team guidance additions

### 10.2 Success Indicators

✅ Team members ask Oracle for architecture reviews
✅ Librarian is used for framework research
✅ Threads are regularly shared
✅ Knowledge base grows organically
✅ AGENTS.md evolves with team learnings
✅ Toolboxes catch issues before code review
✅ Custom commands are actively used

---

## Conclusion

This Amp-native approach goes beyond simple translation of Claude Code patterns. By leveraging Oracle, Librarian, advanced toolboxes, and thread sharing, you create an intelligent development infrastructure that:

1. **Learns and improves** through Oracle's reasoning
2. **Connects to external knowledge** via Librarian
3. **Automates intelligently** with rich toolboxes
4. **Captures team knowledge** through shared threads
5. **Evolves organically** as patterns emerge

**Next Steps:**
1. Review the amp-native-template/ directory
2. Start with Phase 1 (Foundation)
3. Gradually add Oracle/Librarian integration
4. Build toolboxes for your specific needs
5. Share threads and build team knowledge

**Remember:** This is an Amp-first design. Don't try to replicate Claude Code exactly—embrace Amp's unique capabilities!

