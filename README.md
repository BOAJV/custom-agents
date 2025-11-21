# Custom Agents Repository

This repository contains custom GitHub Copilot agents designed to enhance your development workflow.

## Available Agents

### 🚀 git-push Agent

A specialized agent for safely managing git push operations with proper branch management and commit workflow.

#### What it does:
- **Branch Discovery**: Shows all available branches (local and remote)
- **Branch Confirmation**: Ensures you're pushing to the correct target branch
- **Branch Switching**: Safely switches branches when needed
- **Pre-push Checks**: Verifies working directory state and shows change summaries
- **Commit Process**: Helps create meaningful commit messages with user review
- **Push Operations**: Handles various push scenarios with safety checks

## How to Use the git-push Agent

### Prerequisites
- Access to GitHub Copilot Chat
- Repository with the custom agent configuration merged to the default branch

### Usage Methods

#### 1. GitHub Copilot Chat in VS Code (Recommended)
1. Open GitHub Copilot Chat (`Ctrl+Shift+I` or `Cmd+Shift+I`)
2. Type `@git-push` followed by your request
3. The agent will guide you through the safe git workflow

**Example interactions:**
```
@git-push help me push my current changes to the main branch

@git-push I need to create a new feature branch and push my work

@git-push can you help me safely push to the development branch?

@git-push show me all branches and help me push to the right one
```

#### 2. GitHub Copilot Chat on GitHub.com
1. Navigate to your repository on GitHub.com
2. Open the Copilot Chat interface
3. Mention `@git-push` in your message
4. Ask for help with your git operations

#### 3. General Git Workflow with the Agent
The agent follows a structured workflow:

1. **Branch Discovery Phase**
   - Shows local and remote branches
   - Displays current branch status

2. **Target Confirmation Phase**
   - Asks you to confirm the target branch
   - Warns about potential issues

3. **Pre-push Safety Checks**
   - Checks for uncommitted changes
   - Shows summary of changes to be committed
   - Verifies working directory state

4. **Commit Review Phase**
   - Helps craft meaningful commit messages
   - Allows review before committing
   - Provides default messages when appropriate

5. **Push Execution Phase**
   - Executes git push with appropriate options
   - Handles first push, force push warnings, etc.
   - Provides clear feedback on results

### Example Scenarios

#### Scenario 1: First time pushing a new feature
```
You: @git-push I've been working on a new login feature and need to push it
Agent: I'll help you safely push your login feature. Let me first check your current branch status...
```

#### Scenario 2: Pushing to an existing branch
```
You: @git-push push my changes to the development branch
Agent: I'll help you push to the development branch. First, let me show you the current state...
```

#### Scenario 3: When you're unsure about branches
```
You: @git-push I'm not sure which branch to push to, can you help?
Agent: Of course! Let me show you all available branches and help you choose the right one...
```

## Safety Features

The git-push agent prioritizes safety with:
- ✅ **Confirmation before destructive operations**
- ✅ **Clear status reporting at each step**
- ✅ **Branch verification before switching**
- ✅ **Working directory checks**
- ✅ **Meaningful commit message guidance**
- ✅ **Force push warnings and alternatives**

## Agent Configuration

The agent is configured in `.github/agents/git-push.agent.md` and includes:
- Specialized knowledge of git workflows
- Safety-first approach to git operations
- User-friendly guidance and confirmations
- Handling of common git scenarios

## Contributing

To modify or extend the git-push agent:
1. Edit `.github/agents/git-push.agent.md`
2. Test your changes using the methods above
3. Submit a pull request with your improvements

## Troubleshooting

**Agent not responding?**
- Ensure the agent file is merged to the default branch
- Try mentioning `@git-push` explicitly in your message
- Check that you have GitHub Copilot access

**Need help with complex git scenarios?**
- Be specific about your current situation
- Mention what branch you're on and what you want to achieve
- The agent can handle most common git workflows

---

For more information about GitHub Custom Agents, visit: [GitHub Custom Agents Documentation](https://gh.io/customagents/config)