# 🔧 Developer Prompts — 100+ Battle-Tested Prompts for Coding with AI

## Code Review & Refactoring

### 1. The Senior Code Reviewer
```
You are a principal software engineer at Google with 20 years of experience. Review the following code for:
1. Security vulnerabilities (OWASP Top 10)
2. Performance bottlenecks
3. Code smells and anti-patterns
4. Missing error handling
5. Naming conventions
6. SOLID principle violations

For each issue, provide:
- Severity: 🔴 Critical / 🟡 Warning / 🟢 Suggestion
- Line reference
- What's wrong
- How to fix it (with code)

Code to review:
[PASTE CODE HERE]
```

### 2. The Refactoring Machine
```
Refactor this code following these principles:
1. Single Responsibility Principle
2. DRY (Don't Repeat Yourself)
3. Early returns over nested conditionals
4. Descriptive variable names
5. Extract magic numbers into named constants
6. Add JSDoc/docstring comments

Keep the exact same functionality. Show me before/after with explanations.

Code:
[PASTE CODE HERE]
```

### 3. The Bug Hunter
```
I have a bug in my code. Here's what's happening:
- Expected behavior: [DESCRIBE]
- Actual behavior: [DESCRIBE]
- Steps to reproduce: [DESCRIBE]

Analyze this code like a detective. Walk through the execution step by step. Identify the root cause and provide a fix.

Code:
[PASTE CODE HERE]
```

### 4. Performance Optimizer
```
Analyze this code for performance. Consider:
1. Time complexity (Big O)
2. Space complexity
3. Database query optimization (N+1 problems)
4. Memory leaks
5. Unnecessary re-renders (if frontend)
6. Caching opportunities

Provide optimized version with benchmarks explaining the improvement.

Code:
[PASTE CODE HERE]
```

### 5. Test Writer
```
Write comprehensive tests for this code using [Jest/pytest/your framework]:
1. Happy path tests
2. Edge cases (empty inputs, nulls, boundaries)
3. Error cases (invalid inputs, network failures)
4. Integration tests if applicable
5. Mock external dependencies

Use descriptive test names that explain WHAT is being tested and WHY.
Aim for >90% code coverage.

Code to test:
[PASTE CODE HERE]
```

## Architecture & Design

### 6. System Design Architect
```
Design a system for [DESCRIBE YOUR FEATURE/APP]. Include:

1. **High-level architecture** (microservices vs monolith, why)
2. **Database schema** (tables, relationships, indexes)
3. **API design** (REST endpoints with request/response examples)
4. **Data flow** (how data moves through the system)
5. **Scaling strategy** (what breaks at 10x, 100x, 1000x users)
6. **Tech stack recommendation** with justification

Requirements:
- [LIST YOUR REQUIREMENTS]
- Expected scale: [USERS/REQUESTS]
- Budget: [LOW/MEDIUM/HIGH]
```

### 7. API Designer
```
Design a RESTful API for [FEATURE]. Include:
1. All endpoints (method, path, description)
2. Request/response schemas (JSON)
3. Authentication strategy
4. Rate limiting approach
5. Error response format
6. Pagination strategy
7. Versioning strategy

Follow OpenAPI 3.0 conventions. Output as a table first, then detailed specs.
```

### 8. Database Schema Designer
```
Design a database schema for [APP/FEATURE]:
1. Entity-Relationship Diagram (describe in text)
2. Table definitions with columns, types, constraints
3. Indexes for common queries
4. Migration strategy
5. Seed data examples

Optimize for these common queries:
- [QUERY 1]
- [QUERY 2]

Use [PostgreSQL/MySQL/MongoDB]. Explain normalization decisions.
```

## DevOps & Deployment

### 9. Dockerfile Generator
```
Create a production-ready Dockerfile for my [language/framework] application:
- Multi-stage build for minimal image size
- Non-root user for security
- Health check endpoint
- Proper signal handling (graceful shutdown)
- .dockerignore file
- Docker Compose for local development with [database/redis/etc]

My app entry point: [DESCRIBE]
Dependencies: [LIST]
```

### 10. CI/CD Pipeline Builder
```
Create a GitHub Actions CI/CD pipeline for my [language] project:
1. On PR: lint, test, type-check, build
2. On merge to main: deploy to [staging/production]
3. Caching for dependencies
4. Parallel jobs where possible
5. Slack/Discord notification on failure
6. Auto-tagging on release

Deployment target: [Vercel/AWS/GCP/etc]
```

## Quick Utility Prompts

### 11. Regex Builder
```
I need a regex that matches [DESCRIBE PATTERN]. 
Include:
1. The regex pattern
2. Explanation of each part
3. Test cases (matching and non-matching)
4. Edge cases to watch out for
5. Language-specific implementation ([Python/JS/etc])
```

### 12. Git Commit Message Writer
```
Based on this diff, write a conventional commit message:
- Format: type(scope): description
- Types: feat, fix, refactor, docs, test, chore, perf
- Include body if the change is complex
- Reference issue numbers if applicable

Diff:
[PASTE DIFF]
```

### 13. Error Message Decoder
```
I'm getting this error:
[PASTE ERROR]

Context:
- Language/Framework: [SPECIFY]
- What I was doing: [DESCRIBE]
- What I've tried: [LIST]

Explain this error like I'm a junior developer. What caused it? How do I fix it? How do I prevent it in the future?
```

### 14. Code Translator
```
Convert this [SOURCE LANGUAGE] code to [TARGET LANGUAGE]:
- Maintain exact same functionality
- Use idiomatic patterns of the target language
- Add comments explaining language-specific differences
- Include equivalent package/dependency imports
- Handle any API differences

Code:
[PASTE CODE]
```

### 15. Documentation Generator
```
Generate comprehensive documentation for this code:
1. Overview (what it does, why it exists)
2. Installation instructions
3. API reference (all public methods/functions)
4. Usage examples (basic and advanced)
5. Configuration options
6. Troubleshooting common issues
7. Contributing guide

Format: Markdown suitable for README.md

Code:
[PASTE CODE]
```

### 16. Security Auditor
```
Perform a security audit on this code:
1. Check for injection vulnerabilities (SQL, XSS, command injection)
2. Authentication/authorization flaws
3. Sensitive data exposure (API keys, passwords in code)
4. Insecure dependencies
5. CORS misconfiguration
6. Rate limiting gaps
7. Input validation issues

For each finding:
- Severity: Critical/High/Medium/Low
- Description of the vulnerability
- Proof of concept (how to exploit)
- Fix with code example

Code:
[PASTE CODE]
```

### 17. The AI Pair Programmer
```
You are my senior pair programming partner. We're building [FEATURE].

Rules:
1. Think step by step before writing code
2. Ask clarifying questions if requirements are ambiguous
3. Suggest the simplest solution first, then offer alternatives
4. Write production-quality code (error handling, types, tests)
5. Explain your reasoning for key decisions
6. Flag potential issues early

Let's start. Here's what I have so far:
[PASTE CURRENT CODE OR DESCRIBE WHAT YOU NEED]
```

### 18. Code Complexity Reducer
```
This code works but it's too complex. Simplify it while keeping identical behavior:
1. Reduce cyclomatic complexity
2. Extract helper functions
3. Replace conditionals with polymorphism where appropriate
4. Use early returns
5. Simplify nested logic
6. Add descriptive names

Target: Each function should be < 20 lines. McCabe complexity < 5.

Code:
[PASTE CODE]
```

### 19. Migration Script Generator
```
I'm migrating from [OLD TECHNOLOGY] to [NEW TECHNOLOGY].

Current setup: [DESCRIBE]
Target setup: [DESCRIBE]
Data to migrate: [DESCRIBE]

Generate:
1. Step-by-step migration plan
2. Migration scripts
3. Rollback plan
4. Data validation queries (pre and post migration)
5. Downtime estimation
6. Risk assessment
```

### 20. API Response Mocker
```
Generate realistic mock data for these API endpoints:
[LIST YOUR ENDPOINTS WITH SCHEMAS]

Requirements:
- Realistic names, emails, dates (not "test123")
- Consistent relationships between entities
- Include edge cases (empty arrays, null fields, Unicode)
- Format: JSON
- Generate [N] records per endpoint
- Include TypeScript types/interfaces
```

---

*Want the full 500+ prompt pack? Get it at [godlymane.gumroad.com](https://godlymane.gumroad.com)*
