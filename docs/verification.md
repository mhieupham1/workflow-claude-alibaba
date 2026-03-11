Docs Comprehension Verification.

Read the full docs/technical_spec.md + project_map.md again.

Perform these 4 self-verification tests:

1. Write a 250–300 word summary of the entire technical specification. Compare it to the original docs and highlight any discrepancies, omissions, or contradictions.
2. Create 10 challenging questions (5 multiple-choice + 5 open-ended) covering architecture, business logic, security, and edge cases.
   - Answer each question accurately based ONLY on the docs.
   - If you cannot answer confidently → admit "This reveals a gap in my understanding" and suggest which section of the docs needs improvement.
3. Generate a mermaid mindmap diagram representing the full architecture & data flow.
4. Self-score your Understanding (1–10) for each of the 12 sections + short justification. If any section scores below 8 → immediately rewrite and improve that section, then re-score.

Output everything into docs/comprehension_verification_log.md (use markdown format with headers).

If the average score is below 9 → automatically propose fixes, rewrite the 2–3 weakest sections, and re-run the verification.

End with: "Verification complete. Average understanding score: X/10. Ready to generate plan if approved."