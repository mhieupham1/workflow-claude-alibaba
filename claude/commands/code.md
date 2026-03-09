Code Implementation Command - Implement features according to plan with project coding standards.

When invoked, execute the following steps:

## Step 1: Read coding standards
Before starting implementation, read these files from `.claude/docs/`:
- `03-coding-rules.md` - to follow coding standards, conventions, and patterns
- `02-tech-stack.md` - to understand available frameworks and libraries (optional, if needed)

## Step 2: Read the plan file
- Read the plan file specified by user (e.g., `@.claude/plans/<plan-name>.md`)
- The plan contains all necessary context: files to modify, implementation steps, and checklist

## Step 3: Implement according to plan
- Follow the checklist in the plan file
- Code according to the coding rules from docs
- Modify only the files specified in the plan

## Step 4: Verify implementation
- Ensure all tasks in the checklist are completed
- Code follows the project's coding standards (from 03-coding-rules.md)

## Step 5: Notify user
- Display summary of changes made
- List completed tasks from the plan checklist
- **Suggest user to run `/review-code @.claude/plans/<plan-name>.md`** to review the implementation against the plan

---

**Next step:** Run `/clear` then use `/review-code @.claude/plans/<plan-name>.md` to review, or `/update-docs` if docs need updating.
