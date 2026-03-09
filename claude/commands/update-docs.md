Update Documentation Command - Update project documentation after code changes.

When invoked, execute the following steps:

## Step 1: Check recent changes
- Review recent git diff or changes made in the session
- Identify what has been changed/added/removed

## Step 2: Update relevant documentation
Based on the changes, update corresponding docs in `.claude/docs/`:

| Change type | Update file |
|-------------|-------------|
| New/removed dependencies in package.json | `02-tech-stack.md` |
| New/removed folders or structure changes | `01-project-structure.md` |
| New core components or major refactors | `04-core-components.md` |
| New/changed API endpoints or data flow | `05-api-integration.md` |
| Coding standard changes | `03-coding-rules.md` |

## Step 3: Update project summary
- Update `project-summary.md` if there are significant changes
- Ensure links to detailed docs are still accurate

## Step 4: Notify user
- List which documentation files were updated
- Summarize what changes were recorded

---

**Next step:** Run `/clear` then use `/write-commit` to create a commit message.
