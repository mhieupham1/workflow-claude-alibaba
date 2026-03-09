Review code changes against a specific plan. Usage: /review-code @.claude/plans/<plan-name>.md

When invoked with a plan file:

1. **Read the plan file** to understand:
   - What changes were planned
   - Which files were supposed to be modified
   - The checklist of tasks

2. **Run git diff** to see the actual changes:
   - Check staged and unstaged changes
   - Compare with the plan's expected modifications

3. **Review each changed file**:
   - Verify the changes match the plan
   - Check for code quality issues
   - Look for potential bugs or edge cases
   - Ensure no unintended changes

4. **Check the plan checklist**:
   - Mark completed items based on actual changes
   - Identify any missing items from the plan

5. **Provide a review report** with:
   - Summary of changes vs plan
   - Issues found (if any)
   - Suggestions for improvement
   - Updated checklist status

6. **If issues are found that require additional changes**:
   - Propose creating a new plan file to fix the issues
   - Use the format: `/plan-cus "<description of the issue and proposed solution>"`
   - Example: `/plan-cus "Fix issues found in review: [list issues]"`

If no plan file is specified, ask the user to provide a plan file path or review the recent git diff without plan reference.

---

**Next step:** After review is complete, run `/clear` then use `/update-docs` to update documentation, or `/write-commit` to create a commit message.
