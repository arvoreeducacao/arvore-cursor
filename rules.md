Use mysql mcp to see database schema and data to give to you more data and info to create code.

---

My username is <linear_name> in Linear and my squad is <squad_name>.

---

When suggesting or installing a package:

    1.	Always check the npm MCP registry for number of downloads and security signals.
    2.	Prefer official libraries or those with a relevant/high number of downloads.
    3.	Avoid obscure, low-adoption packages unless explicitly approved.

---

Always prefer pnpm as the package manager when running or suggesting commands. Only use npm or yarn if pnpm is not supported in the context.

---

Do not add comments in the code unless explicitly asked.
Prefer clean, self-explanatory code without inline explanations.

---

When writing or updating tests, always prefer Vitest as the test runner if possible. Only use another framework if Vitest is not supported in the context.

---

We are doing TDD.

    1.	Write meaningful tests first, based strictly on the PRD.
    2.	Tests must reflect real business logic and edge cases, not generic or trivial assertions.
    3.	Do not implement the feature yet.
    4.	Tests must fail for the right reasons.
    5.	Then, implement only what is needed for the tests to pass.

---

Before coding, generate a concise PRD:

    •	Problem to solve
    •	Scope in / Scope out
    •	API or data model changes
    •	Edge cases to consider
    •	Test plan with pass/fail criteria

---

Before implementing, read the relevant files.

Return: 1. What this code does (overview) 2. Unknowns or unclear parts 3. Risks and dependencies 4. Impacted files if changes are made 5. Draft of a test strategy

---

Use the MCP context7 to consult library and framework documentation before implementing something specific.

---

Always write unit tests in English.

---

When a PR is merged, send a message to the #releases channel with this message:

<(task_link)|(task_name)>

- Status: (indo para produção | em produção)
- Risks: <summarize in one sentence in portuguese the potential risks of delivering this code.>

---

When resolving a Linear task, you need to:

1. Create a branch with the appropriate name for Linear integration
2. Create a PR with correct descriptions
3. If everything is OK in the PR, move the card to review status
4. Send a message to Slack channel #eng-prs with the format: "👉 [PR](pr_link) para [task_name](task_link)"

Please handle the complete Linear task workflow including branch creation, PR management, status updates, and Slack notifications.

---

When Code has been created or modified. Please run the test suite, eslint, sonarquebe and build to verify that everything is working correctly. Execute 'pnpm test:cov', 'pnpm lint' and 'pnpm build' and fix any issues found. If tests fail or linting errors occur, fix them.
