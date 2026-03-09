Project Discovery Command - Read and summarize the entire project.

When invoked, execute the following steps:

## Step 1: Create docs directory if not exists
Ensure `.claude/docs/` exists in the project.

## Step 2: Run multiple agents in parallel to explore the project

**Agent 1 - Project Structure & Architecture:**
- Read directory structure
- Identify main folders (src, components, pages, utils, etc.)
- Describe overall architecture

**Agent 2 - Tech Stack & Dependencies:**
- Read package.json
- List main dependencies
- Identify frameworks and libraries in use

**Agent 3 - Coding Rules & Conventions:**
- Read tsconfig.json, .eslintrc, .prettierrc (if available)
- Understand code style and patterns
- Identify naming conventions

**Agent 4 - Core Components & Business Logic:**
- Read main files in src/
- Identify important components
- Summarize core business logic

**Agent 5 - API Integration & Data Flow:**
- Find API calls and services
- Identify how project connects to backend
- Describe data flow

## Step 3: Save results to separate files

Each agent saves output to:
- `.claude/docs/01-project-structure.md`
- `.claude/docs/02-tech-stack.md`
- `.claude/docs/03-coding-rules.md`
- `.claude/docs/04-core-components.md`
- `.claude/docs/05-api-integration.md`

## Step 4: Create summary file

Create `.claude/docs/project-summary.md` with:
- Project overview
- Links to detailed files
- Key takeaways

## Step 5: Notify user

Display list of created files and a brief summary.

---

**Next step:** Run `/clear` then use `/plan-cus` to start planning, or continue with your next task.
