When I say "OPR" (Open Pull Request), I want you to:

1. **Check for changes**: Verify if there are any uncommitted changes in the repository
2. **If changes exist**:
   - adicione todas as alterações usando git add, apenas ignore esses arquivos .tool-versions e devices.json
   - Create a commit with a descriptive message based on the changes
   - Push the current branch to origin
2. **If no changes**
   - just continue to step 3
3. **Generate PR-DESC**: Analyze the changes and create a complete PR description using the PR-DESC template
4. **Create Pull Request**: Open a PR with the generated description
5. **Send me the link**: Provide the PR URL
6. **Execute EPS rule**: If everything succeeds, automatically execute the "EPS" rule (move Linear task to review and send Slack notification)

**Requirements**:
- Use meaningful commit messages based on the actual changes
- Generate complete PR descriptions following the established template
- Only proceed if there are actual changes to commit
- If no changes exist, inform me that there's nothing to commit
- Always confirm the PR creation was successful before executing EPS

**Example flow**:
1. Check git status
2. If changes → commit → push → generate PR-DESC → create PR → send link → execute EPS
3. if no changes → generate PR-DESC → create PR → send link → execute EPS

