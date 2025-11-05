When I ask "Check if merged to master and send release" or say "VPR" (or similar), do this:

1. Verify if the mentioned PR has been merged to master branch
2. If merged:
   - Find the corresponding Linear task referenced in the PR
   - Prepare a release message for the #releases Slack channel with format:
     "[task_name](task_link)
     - Status: (going to production | in production)
     - Risks: <summarize in one sentence in Portuguese the potential risks of delivering this code>"
3. Show me the formatted release message
4. send message to chanel "releases"

If the PR is NOT merged:
- Inform me that the PR hasn't been merged yet
- Ask if I want to check another PR or wait

Additional guidelines:
- If multiple tasks are referenced in the PR, ask me to clarify which one to use
- If no Linear task is found, inform me and ask if I want to proceed without task reference
- Always verify the PR merge status by checking the actual merge commit
- Include risk assessment based on the changes made in the PR
- Use Portuguese for the risks section as specified in the original rules

