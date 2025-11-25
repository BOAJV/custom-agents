# Custom Agents Repository

This repository contains custom GitHub Copilot agents designed to enhance your development workflow.

## Available Agents

### 🌟 gita Agent

A specialized git operations expert that helps you safely push your work to git repositories with automated workflow and nano editor integration.

#### What gita does:
- **Branch Discovery**: Shows all available branches (local and remote) with current status
- **Branch Confirmation**: Ensures you're pushing to the correct target branch with safety checks
- **Branch Switching**: Automatically switches branches when needed
- **Pre-push Checks**: Verifies working directory state and stages necessary files
- **Automated Commit Process**: Opens nano editor for commit message review with automatic continuation
- **Seamless Push Operations**: Automatically pushes after commit completion without additional prompts
- **Nano Editor Integration**: Specifically configured to use nano for commit message editing
- **Continuous Workflow**: Complete commit → push → confirmation flow in one operation

## How to Use the gita Agent

### Prerequisites
- Access to GitHub Copilot Chat
- Repository with the custom agent configuration merged to the default branch

### Usage Methods

#### 1. GitHub Copilot Chat in VS Code (Recommended)
1. Open GitHub Copilot Chat (`Ctrl+Shift+I` or `Cmd+Shift+I`)
2. Type `@gita` followed by your request
3. The agent will guide you through the automated git workflow with nano editor

**Example interactions:**
```
@gita help me push my current changes to the main branch

@gita I need to create a new feature branch and push my work

@gita can you help me safely push to the development branch?

@gita show me all branches and push my changes automatically

@gita commit and push my changes with nano editor review
```

#### 2. GitHub Copilot Chat on GitHub.com
1. Navigate to your repository on GitHub.com
2. Open the Copilot Chat interface
3. Mention `@gita` in your message
4. Ask for help with your automated git operations

#### 3. Automated Git Workflow with gita Agent
The gita agent follows a streamlined, automated workflow:

1. **Branch Discovery Phase**
   - Shows local and remote branches with current status
   - Displays uncommitted changes and repository state

2. **Target Branch Confirmation**
   - Confirms the target branch for your push operation
   - Automatically switches branches if needed

3. **Pre-push Safety Checks**
   - Stages uncommitted changes automatically
   - Configures nano as the default git editor
   - Enables verbose commit mode for detailed information

4. **Nano Editor Commit Phase**
   - Opens nano editor with `git commit -e` command
   - Provides meaningful default commit message
   - Waits for you to review/edit in nano (Ctrl+O to save, Ctrl+X to exit)
   - **Automatically continues** after you close nano

5. **Automatic Push Execution**
   - Immediately pushes to target branch after successful commit
   - Handles first push scenarios with upstream tracking
   - Provides clear feedback on push results
   - **No additional user input required** after nano closes

### Key Features of gita's Automated Workflow

#### ✨ Nano Editor Integration
- Specifically configured to use nano for all commit message editing
- Automatically sets `git config --global core.editor nano`
- Forces interactive commit review with `git commit -e`

#### ⚡ Continuous Automation
- **Zero interruption**: After you close nano, everything happens automatically
- **Seamless flow**: commit → push → confirmation without stops
- **Status reporting**: Real-time updates throughout the process

#### 🛡️ Safety with Speed
- All safety checks happen upfront
- User reviews commit message in nano
- Automatic execution only after user confirmation via nano

### Example Scenarios

#### Scenario 1: Quick push with automated workflow
```
You: @gita push my login feature changes
Agent: I'll help you push your login feature with the automated workflow. 
       Let me check your branches and set up nano for commit review...
       [Opens nano for commit message] → [Auto-push after you close nano]
```

#### Scenario 2: New feature branch with seamless push
```
You: @gita create a new branch and push my work
Agent: I'll create a new branch and push your changes automatically.
       [Sets up branch] → [Opens nano] → [Auto-push] → [Sets upstream tracking]
```

#### Scenario 3: Automated push to existing branch
```
You: @gita commit and push to development branch
Agent: I'll automate the commit and push to development.
       [Switches to dev] → [Stages changes] → [Opens nano] → [Auto-push]
```

## Key Advantages of gita Agent

### 🚀 **Speed & Automation**
- **One command**: Complete git workflow in a single interaction
- **Nano integration**: Familiar editor for commit message review
- **Auto-continuation**: No manual steps after nano closes
- **Instant feedback**: Real-time status throughout the process

### 🛡️ **Safety & Control**
- **Review point**: You control the commit message in nano
- **Safety checks**: Automatic verification before operations
- **Branch awareness**: Always confirms target branch
- **Error handling**: Clear guidance when issues occur

### ⚙️ **Technical Features**
- **Nano-first**: Specifically optimized for nano editor users
- **Git config automation**: Automatically configures optimal settings
- **Verbose commits**: Enhanced commit information display
- **Upstream tracking**: Handles first-time branch pushes correctly

## Safety Features

The gita agent combines automation with safety:
- ✅ **Nano editor review**: Always opens nano for commit message confirmation
- ✅ **Pre-flight checks**: Verifies repository state before operations
- ✅ **Branch verification**: Confirms target branch before switching
- ✅ **Automatic staging**: Handles uncommitted changes intelligently
- ✅ **Clear status updates**: Reports progress at each automation step
- ✅ **Error recovery**: Provides guidance when automation encounters issues
- ✅ **No surprise pushes**: User must close nano to trigger the push

## Agent Configuration

The gita agent is configured in `.github/agents/gita.agent.md` with:
- **Nano editor specialization**: Optimized workflow for nano users
- **Automated continuation logic**: Smart workflow that continues after user input
- **Git configuration management**: Automatic setup of optimal git settings
- **Safety-first automation**: Combines speed with user control
- **Verbose commit support**: Enhanced commit information and review

### Critical Requirements Built Into gita:
- **Mandatory nano usage**: All commits must go through nano review
- **Automatic continuation**: Workflow continues without prompts after nano closes
- **Git config automation**: Sets nano as editor and enables verbose commits
- **Continuous flow design**: Optimized for uninterrupted commit → push workflow

## Testing the gita Agent

Use these command patterns to test various git operations with the gita agent. Each command will trigger the automated nano editor workflow.

### Basic Operations

#### Simple Push to Current Branch
```
@gita push my changes
@gita commit and push current work
@gita save my progress to this branch
```

#### Push to Specific Branch
```
@gita push to main branch
@gita commit and push to development
@gita push my changes to feature/login
@gita push to origin/staging
```

### Branch Management

#### Create New Branch and Push
```
@gita create new branch feature/payment and push
@gita make a new branch called bugfix/auth-error
@gita create branch hotfix/security-patch and push my work
```

#### Switch Branch and Push
```
@gita switch to main and push my changes
@gita change to development branch and push
@gita move to feature/api branch and commit
```

### Advanced Scenarios

#### First Time Push (Upstream Tracking)
```
@gita push my new branch for the first time
@gita set up upstream and push to origin
@gita push new feature branch with tracking
```

#### Multiple File Operations
```
@gita commit all my changes and push
@gita stage everything and push to main
@gita add all modified files and push
```

#### Specific File Operations
```
@gita commit README.md and push
@gita push only the config changes
@gita commit src/ directory changes and push
```

### Project-Specific Commands

#### Feature Development
```
@gita push my login feature implementation
@gita commit the user authentication changes
@gita push database migration updates
@gita commit API endpoint modifications
```

#### Bug Fixes
```
@gita push the security vulnerability fix
@gita commit memory leak patch
@gita push performance optimization changes
```

#### Documentation Updates
```
@gita push documentation improvements
@gita commit README updates
@gita push changelog modifications
```

### Complex Workflow Testing

#### Multi-step Operations
```
@gita check branches, commit changes, and push to development
@gita show me branches then push my work to the right one
@gita verify my changes and push to main safely
```

#### Conflict Resolution Scenarios
```
@gita help me push after resolving conflicts
@gita commit merge resolution and push
@gita push after fixing merge issues
```

### Expected Workflow for All Commands

1. **Branch Discovery**: gita shows current and available branches
2. **Change Detection**: Identifies modified, added, or deleted files
3. **Staging**: Automatically stages changes for commit
4. **Git Config**: Sets nano editor and verbose commit mode
5. **Nano Opens**: You review/edit commit message in nano
6. **Save & Exit**: Ctrl+O to save, Ctrl+X to exit nano
7. **Auto-Push**: Immediate push after successful commit
8. **Confirmation**: Status report of completed operation

### Testing Tips

- **Make some changes**: Modify files before testing push commands
- **Try different branches**: Test switching and pushing to various branches
- **Test edge cases**: Empty commits, large files, special characters in messages
- **Verify automation**: Ensure push happens automatically after nano closes
- **Check configurations**: Verify nano is set as git editor after first use

## Setting Up gita Agent in Your Repository

Follow these steps to add the gita agent to any GitHub repository:

### Step 1: Create the Agent Directory Structure

```bash
# Navigate to your repository root
cd your-repository-name

# Create the agents directory
mkdir -p .github/agents
```

### Step 2: Copy the Agent Configuration

Create a new file `.github/agents/gita.agent.md` with the following content:

```markdown
---
name: gita
description: Agent specializing in pushing work to git branches with proper branch management and commit workflow.
---

# gita Agent

You are a git operations expert that helps users safely push their work to git repositories. Follow this workflow:

1. **Branch Discovery**: Display all available branches (local and remote) to help the user understand the repository state.

2. **Branch Confirmation**: Ask the user to confirm which branch they want to push to, ensuring they understand the target branch.

3. **Branch Switching**: Switch to the correct branch if not already on it.

4. **Pre-push Checks**: 
   - Check for any uncommitted changes
   - Verify the working directory is clean or stage necessary files
   - Show a summary of changes to be committed

5. **Commit Process**: 
   - FIRST: Always run `git config --global core.editor nano` to ensure nano is set as the default editor
   - SECOND: Always run `git config --global commit.verbose true` for detailed commit information
   - THIRD: You MUST use `git commit -e` command (never use `git commit -m` alone)
   - FOURTH: The `git commit -e` command MUST open nano editor in the terminal for user review
   - FIFTH: After the user saves (Ctrl+O, Enter) and exits (Ctrl+X) the nano editor, the commit will complete automatically
   - SIXTH: Immediately after commit completion, continue to the push operation without waiting for additional user input
   - Always provide meaningful default commit messages when using `-m` with `-e`
   - The editor opening is MANDATORY - if it doesn't open, something is wrong

6. **Automatic Push Operation**: 
   - IMMEDIATELY after successful commit completion, proceed with git push
   - Execute the git push with appropriate options (use `-u origin [branch-name]` for first push)
   - Handle common push scenarios (first push, force push warnings, etc.)
   - Provide clear feedback on the push result
   - Complete the entire workflow without requiring additional user confirmation after nano closes

Always prioritize safety and user confirmation before executing destructive operations.

## CRITICAL REQUIREMENTS:
- The `git commit -e` command MUST always open nano editor
- If nano doesn't open, check git configuration and retry
- After user closes nano editor, AUTOMATICALLY continue to push without asking
- Always verify git config settings before committing
- Complete the full workflow: commit → push → confirmation in one continuous flow

## Workflow Automation:
- Once nano editor closes and commit succeeds, immediately execute push
- Do not pause or ask for confirmation between commit and push
- Provide status updates as each step completes
- Only stop if there are errors that require user intervention

## Troubleshooting:
- If nano doesn't open: Run `git config --global core.editor nano` first
- If commit completes without editor: The `-e` flag was not used properly
- Always use both `-e` and `-m` flags together: `git commit -e -m "message"`
```

### Step 3: Commit and Push the Agent

```bash
# Add the agent file
git add .github/agents/gita.agent.md

# Commit the agent
git commit -m "Add gita agent for automated git workflow with nano editor integration"

# Push to your default branch (usually main or master)
git push origin main
```

### Step 4: Verify Agent Activation

1. **Wait a few minutes** for GitHub to process the new agent
2. **Open GitHub Copilot Chat** in VS Code or on GitHub.com
3. **Test the agent** with: `@gita help me test the agent setup`

### Step 5: Start Using gita

Once set up, you can use gita with commands like:
- `@gita push my changes`
- `@gita commit and push to main branch`
- `@gita create new branch and push my work`

### Repository Requirements

- **GitHub Copilot access** for your account and repository
- **Agent file must be on default branch** (main/master) to be active
- **Terminal access** for nano editor functionality (works best in VS Code)

### Customization Options

You can modify the agent behavior by editing `.github/agents/gita.agent.md`:
- Change commit message patterns
- Modify branch handling logic
- Adjust safety checks and confirmations
- Customize editor preferences (though nano is recommended)

## Contributing

To modify or extend the gita agent:
1. Edit `.github/agents/gita.agent.md`
2. Test the automated workflow using the methods above
3. Ensure nano editor integration works properly
4. Submit a pull request with your improvements

## Troubleshooting

**Agent not responding to @gita?**
- Ensure the agent file is merged to the default branch (main)
- Try mentioning `@gita` explicitly in your message
- Check that you have GitHub Copilot access

**Nano editor not opening during commits?**
- gita automatically configures git to use nano
- If issues persist, manually run: `git config --global core.editor nano`
- The agent will detect and fix configuration issues

**Workflow stops after nano?**
- Ensure you properly save (Ctrl+O) and exit (Ctrl+X) nano
- The automated push should happen immediately after nano closes
- Check for any git errors in the terminal output

**Need help with complex git scenarios?**
- Be specific about your current branch and desired target
- Mention what changes you want to commit and push
- gita handles most scenarios automatically but can adapt to special cases

---

For more information about GitHub Custom Agents, visit: [GitHub Custom Agents Documentation](https://gh.io/customagents/config)