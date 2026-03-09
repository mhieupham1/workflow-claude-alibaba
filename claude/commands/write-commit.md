Write Commit Message Command - Generate commit message from recent code changes.

When invoked, execute the following steps:

## Step 1: Check git status
- Run `git status` to see staged and unstaged changes
- Identify which files have been modified

## Step 2: Review the changes
- Run `git diff` to see unstaged changes
- Run `git diff --staged` to see staged changes
- Understand what was changed (features, fixes, refactors, etc.)

## Step 3: Read recent commit history
- Run `git log --oneline -5` to see recent commit messages
- Follow the project's commit message style/convention

## Step 4: Generate commit message
- Write a concise commit message (1 line summary + optional body)
- Follow conventional commit format if project uses it (feat:, fix:, chore:, etc.)
- Focus on **what** and **why**, not **how**

## Step 5: Present to user
- Show the generated commit message
- Wait for user approval before committing
- **Do NOT auto-commit** - let user review and decide

---

**Next step:** After committing, run `/clear` to reset context before starting a new task.
