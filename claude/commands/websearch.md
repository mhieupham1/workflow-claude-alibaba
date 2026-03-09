Web Search Command - Search the web using Gemini CLI with multi-agent parallel search.

**IMPORTANT:**
- Do NOT use the built-in Web Search tool
- Run `gemini search` bash commands directly in PARALLEL
- Do NOT spawn sub-agents (they don't have Bash access)

---

## Step 1: Get the search query
- Use the user's provided query
- If no specific query, ask the user what they want to search for

## Step 2: Build 3 search queries

**Query 1 - Technical/Logical:**
`"<topic> best practices official guide technical"`

**Query 2 - Creative/Practical:**
`"<topic> tutorial examples real world experience"`

**Query 3 - Critical/Analytical:**
`"<topic> common mistakes problems alternatives vs"`

## Step 3: Execute searches IN PARALLEL using background bash

**CRITICAL:** Run all 3 searches simultaneously using background mode:

Run this combined command:
```bash
gemini search "<query1>" &
gemini search "<query2>" &
gemini search "<query3>" &
wait
```

This launches all 3 searches in parallel and waits for completion.

**Important:** Use a SINGLE bash command with `&` to background each search, then `wait` for all to complete.

## Step 4: Process and present results

The bash output will contain results from all 3 searches. Organize them:

```
## Technical Perspective
[key findings + sources]

## Practical Perspective
[key findings + sources]

## Critical Perspective
[key findings + sources]

## Summary
[combined insights]
```

---

**Optional:** User can request single-agent search:
- `/websearch --technical <query>` - Only technical search
- `/websearch --creative <query>` - Only practical search
- `/websearch --critical <query>` - Only critical search

---

**Next step:** After search completes, run `/clear` to reset context.
