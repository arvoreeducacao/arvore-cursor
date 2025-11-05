When I ask "Send PR to Slack" or when I say "EPS", do this:

1. Find the Linear task related to the current branch or with a similar name
1.1 If you can retrieve the Linear task, simply ignore this step. If you cannot retrieve the task from Linear, inform me that the MCP needs to be restarted, stop the process, and wait until I restart the Linear MCP.
2. Format the message for Slack channel #eng-prs as: "👉 [PR](pr_link) para [task_name](task_link)"
   - For task_name: Always include the full task name with ID prefix (e.g., "EXP-231: Task Title")
   - For PR: Keep "PR" text and include the PR link
3. Show me the formatted message before sending
4. After confirmation, move the Linear task to "In Review" status if it's not already there

Additional guidelines:
- If multiple tasks match the branch name, ask me to clarify which one
- If no task is found, inform me and ask if I want to proceed with just the PR link
- Always verify the task status before updating it
- If the task is already in review, just confirm the status without changing it

