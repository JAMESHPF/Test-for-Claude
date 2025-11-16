# CLAUDE.md - AI Assistant Guide

**Repository:** Test-for-Claude
**Last Updated:** 2025-11-16
**Purpose:** Test repository for AI assistant interactions

---

## 📋 Repository Overview

This is a test repository designed for validating AI assistant capabilities and workflows. It serves as a sandbox environment for testing various development tasks, git operations, and AI-assisted coding scenarios.

### Current State
- **Type:** Test/Sandbox Repository
- **Primary Language:** Not yet defined
- **Framework:** Not yet defined
- **Build System:** Not yet defined

---

## 🏗️ Codebase Structure

```
Test-for-Claude/
├── .git/              # Git repository metadata
├── README.md          # Project readme
└── CLAUDE.md          # This file - AI assistant guide
```

### Directory Conventions

As the repository grows, follow these conventions:

- `src/` - Source code files
- `test/` or `tests/` - Test files
- `docs/` - Documentation
- `scripts/` - Build and utility scripts
- `config/` - Configuration files
- `.github/` - GitHub workflows and templates

---

## 🔄 Development Workflow

### Branch Strategy

**Feature Branches:**
- All development work should be done on feature branches
- Current feature branch: `claude/claude-md-mi1e3sdm83bjclfc-012uJte9MH8EGCwhpKMwYaci`
- Branch naming convention: `claude/claude-md-<session-id>`

**Main Branch:**
- The main/master branch contains stable, reviewed code
- Never push directly to main without explicit permission

### Git Operations

#### Committing Changes

1. **Stage relevant files:**
   ```bash
   git add <files>
   ```

2. **Create descriptive commits:**
   ```bash
   git commit -m "Brief description of changes"
   ```

3. **Commit message guidelines:**
   - Use imperative mood ("Add feature" not "Added feature")
   - Be concise but descriptive
   - Reference issues/PRs when applicable
   - Examples:
     - "Add user authentication module"
     - "Fix null pointer exception in data parser"
     - "Update documentation for API endpoints"

#### Pushing Changes

Always push to the designated feature branch:
```bash
git push -u origin claude/claude-md-mi1e3sdm83bjclfc-012uJte9MH8EGCwhpKMwYaci
```

**Retry Logic:**
- If push fails due to network errors, retry up to 4 times
- Use exponential backoff: 2s, 4s, 8s, 16s

#### Fetching/Pulling

Prefer fetching specific branches:
```bash
git fetch origin <branch-name>
git pull origin <branch-name>
```

---

## 🤖 AI Assistant Guidelines

### Task Planning

When working on complex tasks:

1. **Use TodoWrite tool** to create task lists
2. **Break down complex tasks** into manageable steps
3. **Mark tasks in progress** before starting work
4. **Mark tasks completed** immediately after finishing
5. **Update task status** in real-time

### Code Quality Standards

#### Security
- Never introduce security vulnerabilities (XSS, SQL injection, command injection, etc.)
- Follow OWASP Top 10 best practices
- Validate and sanitize all inputs
- Use parameterized queries for database operations
- Implement proper authentication and authorization

#### Best Practices
- Write clean, readable code
- Follow language-specific style guides
- Add comments for complex logic
- Write meaningful variable and function names
- Keep functions small and focused
- Follow DRY (Don't Repeat Yourself) principle

#### Testing
- Write tests for new features
- Ensure existing tests pass before committing
- Aim for good test coverage
- Include unit tests, integration tests as appropriate

### File Operations

**Prefer specialized tools:**
- Use `Read` for reading files (not `cat`)
- Use `Edit` for editing files (not `sed/awk`)
- Use `Write` for creating files (not `echo >` or heredocs)
- Use `Grep` for searching content (not `grep` command)
- Use `Glob` for finding files (not `find` command)

**File creation policy:**
- ALWAYS prefer editing existing files over creating new ones
- Only create new files when absolutely necessary
- Don't create documentation files unless explicitly requested

### Communication Style

- Be concise and professional
- Don't use emojis unless explicitly requested
- Use GitHub-flavored markdown for formatting
- Reference code with `file_path:line_number` format
- Provide technical accuracy over validation

### Tool Usage

**Parallel execution:**
- Run independent tool calls in parallel when possible
- Examples: multiple file reads, multiple searches
- Send single message with multiple tool calls

**Sequential execution:**
- Use sequential calls when operations depend on previous results
- Chain with `&&` in bash when needed

**Task tool:**
- Use for complex multi-step explorations
- Use `Explore` subagent for codebase exploration
- Specify thoroughness level: "quick", "medium", or "very thorough"

---

## 📝 Code Review Checklist

Before committing changes, verify:

- [ ] Code follows style guidelines
- [ ] No security vulnerabilities introduced
- [ ] Tests added/updated as needed
- [ ] All tests pass
- [ ] Documentation updated if needed
- [ ] No commented-out code (unless necessary)
- [ ] No debug statements left in code
- [ ] Error handling implemented properly
- [ ] Code is DRY and maintainable

---

## 🚀 Common Tasks

### Adding a New Feature

1. Create task list with TodoWrite
2. Research existing codebase if needed
3. Implement feature with tests
4. Run tests to verify
5. Commit with descriptive message
6. Push to feature branch

### Fixing a Bug

1. Reproduce the bug
2. Identify root cause
3. Implement fix
4. Add regression test
5. Verify all tests pass
6. Commit and push

### Refactoring Code

1. Understand current implementation
2. Plan refactoring approach
3. Make incremental changes
4. Run tests after each change
5. Commit in logical chunks
6. Document significant changes

---

## 🔍 Exploration Guidelines

When exploring unfamiliar code:

1. **Start broad:** Use Task/Explore agent for general questions
2. **Narrow down:** Use Grep to find specific implementations
3. **Read context:** Use Read to understand surrounding code
4. **Trace dependencies:** Follow imports and function calls
5. **Document findings:** Keep notes on key discoveries

---

## ⚠️ Important Warnings

### DO NOT:
- Push to main/master without permission
- Commit sensitive data (.env files, credentials, API keys)
- Use `git push --force` without explicit user request
- Skip git hooks (--no-verify)
- Create unnecessary documentation files
- Use emojis in code or commits (unless requested)
- Amend commits from other developers

### DO:
- Always work on designated feature branches
- Write clear commit messages
- Test before committing
- Ask for clarification when requirements are unclear
- Use specialized tools over bash commands
- Track complex tasks with TodoWrite
- Push changes when task is complete

---

## 🔧 Environment Information

- **Working Directory:** `/home/user/Test-for-Claude`
- **Git Repository:** Yes
- **Platform:** Linux
- **OS Version:** Linux 4.4.0

---

## 📚 Additional Resources

### Git Best Practices
- Keep commits atomic and focused
- Write meaningful commit messages
- Don't commit generated files
- Review changes before committing

### Testing Best Practices
- Test edge cases and error conditions
- Use descriptive test names
- Keep tests independent
- Mock external dependencies

### Documentation Best Practices
- Keep documentation up-to-date
- Use clear examples
- Document assumptions and limitations
- Include setup and usage instructions

---

## 🔄 Updating This File

When the repository evolves:

1. **Update structure section** when directories/files are added
2. **Update workflow section** if processes change
3. **Add technology-specific guidelines** as needed
4. **Document new conventions** as they're established
5. **Keep examples current** with actual codebase patterns

---

## 📞 Getting Help

If you encounter issues:

1. Check this guide first
2. Review existing code patterns
3. Ask user for clarification on requirements
4. Consult language/framework documentation
5. Report bugs to: https://github.com/anthropics/claude-code/issues

---

**Remember:** This is a living document. Update it as the codebase grows and new patterns emerge.
