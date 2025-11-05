When I say "DTT" (Do The Task), I want you to:

- Identify the Linear task: Find the task in Linear based on the current branch name
- Move the task to "in progress" on Linear
- Read task details: Analyze the task description, requirements, and acceptance criteria
- Plan implementation: Break down the task into actionable steps and create a todo list
- Execute the task: Implement all necessary changes in the repository following our coding standards
- Ensure quality: Run tests, linting, and fix any issues before completion
- Dont make tests, dont run tests, just lint if necessary

Requirements:
- Use the branch name to identify the corresponding Linear task
- Follow all established coding guidelines (Elixir contexts, React TypeScript, etc.)
- Implement using TDD methodology when applicable
- Ensure all changes are properly linted
- If the task involves backend changes, follow the 5 strict guidelines for context-based architecture

Example flow:
- Parse current branch name (e.g., vitorpiovezan/exp-345-add-payment-reports)
- Find Linear task EXP-345
- Read task description and requirements
- Create implementation plan with todos
- Implement the feature
- Run linting

Critical notes:
- Always analyze the task requirements thoroughly before starting
- Ensure all code follows the project's coding standards

