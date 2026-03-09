Enable plan mode. When activated:

1. **Read project documentation first:**
   - Check if `.claude/docs/` directory exists
   - If documents exist, read all files in `.claude/docs/` (especially `project-summary.md` and related docs) to understand project context
   - If documents do NOT exist, inform user they can run `/project-doc` first to generate project documentation

2. **Explore selectively based on user's request:**
   - Only explore files/folders relevant to the specific task
   - Do NOT re-explore the entire project (docs already provide context)
   - Focus on understanding what needs to be changed for this specific feature/fix

3. **Mandatory: Create a plan file** in project's `.claude/plans/` directory before any implementation.
   The plan file MUST be created with the following structure:
   - **All content must be written in English** (except for user-specific text like UI labels that should remain unchanged)

   ```markdown
   # Plan: <Plan Name>

   ## Date
   YYYY-MM-DD

   ## Overview
   <Brief description>

   ## Checklist
   - [ ] Task 1
   - [ ] Task 2
   - [ ] Task 3

   ## Files to Modify
   - `path/to/file1.ts` - description
   - `path/to/file2.ts` - description

   ## Implementation Steps
   <Step-by-step details>

   ## Impact Analysis
   - Affected components:
   - Potential risks:
   - Testing considerations:
   ```

4. Save the plan file as `<project-root>/.claude/plans/<plan-name>-<YYYY-MM-DD>.md`

5. After saving the plan file, present it to the user and wait for approval before implementing

**IMPORTANT**: Always write the plan to a physical .md file in `.claude/plans/` - do not just display the plan in the response.

---

**Next step:** After user approves the plan, run `/clear` then use `/code` to start implementation.