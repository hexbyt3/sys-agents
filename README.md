# SysBot.NET Claude Agents

A collection of specialized AI agents designed to assist with SysBot.NET development, providing expert guidance for Pokemon automation, bot development, and code quality.

## 📋 Table of Contents

- [Installation](#installation)
- [Available Agents](#available-agents)
- [How to Invoke Agents](#how-to-invoke-agents)
- [Agent Descriptions](#agent-descriptions)
- [Usage Examples](#usage-examples)
- [Best Practices](#best-practices)
- [Contributing](#contributing)

## 🚀 Installation

### Prerequisites

- Claude Desktop app installed
- Git installed on your system
- SysBot.NET project repository

### Installation Steps

1. **Clone the agents repository:**
   ```bash
   git clone https://github.com/hexbyt3/sys-agents.git
   cd sys-agents
   ```

2. **Copy agents to your SysBot.NET project:**
   ```bash
   # Navigate to your SysBot.NET project root
   cd /path/to/your/sysbot-project
   
   # Create .claude directory if it doesn't exist
   mkdir -p .claude/agents
   
   # Copy all agent files
   cp -r /path/to/sys-agents/*.md .claude/agents/
   ```

3. **Verify installation:**
   - Open Claude Desktop
   - Navigate to your SysBot.NET project
   - The agents should now be available in Claude

## 🤖 Available Agents

| Agent | Description | Primary Use Cases |
|-------|-------------|-------------------|
| **bug-hunter** | Bug detection and fixing specialist | Finding race conditions, memory leaks, debugging automation failures |
| **csharp-optimizer** | Performance optimization expert | Memory optimization, async improvements, bottleneck resolution |
| **csharp-reviewer** | Code review specialist | Security reviews, best practices, memory management |
| **feature-developer** | Feature implementation expert | New functionality, API integration, Discord commands |
| **pokemon-specialist** | Pokemon automation expert | Game mechanics, PKHeX integration, trade optimization |
| **refactoring-expert** | Code modernization specialist | SOLID principles, C# 13 features, architecture improvements |
| **security-auditor** | Security specialist | Vulnerability detection, secure coding, data protection |
| **winforms-enhancer** | UI/UX specialist | Modern interfaces, responsive design, visual enhancements |

## 🎯 How to Invoke Agents

### Basic Invocation

To use an agent, simply mention their specific use case in your request to Claude:

```
"I need help debugging a race condition in my trade queue"
→ Claude will automatically invoke the bug-hunter agent
```

### Direct Invocation

You can also explicitly request a specific agent:

```
"Use the security-auditor agent to review my Discord command implementation"
```

### Multiple Agent Collaboration

For complex tasks, Claude can coordinate multiple agents:

```
"I want to add a new batch trading feature with proper security and performance optimization"
→ May invoke feature-developer, security-auditor, and csharp-optimizer agents
```

## 📖 Agent Descriptions

### 🐛 bug-hunter
**Expertise:** Race conditions, memory leaks, automation failures, thread safety issues

**When to use:**
- Bot crashes or hangs unexpectedly
- Memory usage grows over time
- Discord commands timeout
- Trade sequences fail intermittently
- UI freezes during operations

**Example invocation:**
```
"My bot crashes when multiple users trade simultaneously"
"The UI freezes when I stop a bot while it's trading"
"Memory usage keeps growing during long bot sessions"
```

### ⚡ csharp-optimizer
**Expertise:** Performance optimization, memory allocations, async patterns, bottleneck analysis

**When to use:**
- Slow bot response times
- High CPU/memory usage
- Laggy UI updates
- Inefficient Pokemon searches
- Network operation delays

**Example invocation:**
```
"Pokemon box searches are taking too long"
"The UI becomes unresponsive with many bots running"
"How can I optimize my trade queue processing?"
```

### 🔍 csharp-reviewer
**Expertise:** Code quality, security review, best practices, C# 13/.NET 9 features

**When to use:**
- After implementing new features
- Before major releases
- When refactoring existing code
- For security-sensitive changes
- To ensure code consistency

**Example invocation:**
```
"Review my new Discord command implementation"
"Check this trade validation logic for security issues"
"Is my async/await usage correct here?"
```

### 🚀 feature-developer
**Expertise:** New features, Discord/Twitch integration, API design, bot automation

**When to use:**
- Adding new bot functionality
- Implementing Discord commands
- Creating new trade modes
- Integrating external services
- Designing plugin systems

**Example invocation:**
```
"I want to add a wondertrade feature"
"How do I implement a custom Discord embed for trades?"
"Create a batch trade system that supports up to 10 Pokemon"
```

### 🎮 pokemon-specialist
**Expertise:** Game mechanics, PKHeX library, trade logic, memory offsets, RNG manipulation

**When to use:**
- Game-specific implementations
- PKHeX data handling
- Trade sequence optimization
- Memory offset updates
- Legality checking issues

**Example invocation:**
```
"How do I handle the new DLC Pokemon in Scarlet/Violet?"
"Implement shiny hunting detection for BDSP"
"The trade offset changed in the latest game update"
```

### 🔧 refactoring-expert
**Expertise:** Code modernization, SOLID principles, design patterns, C# 13 features

**When to use:**
- Legacy code updates
- Architecture improvements
- Reducing code duplication
- Improving maintainability
- Modernizing to latest C#

**Example invocation:**
```
"Refactor this switch statement to use pattern matching"
"How can I apply SOLID principles to my bot architecture?"
"Modernize this code to use C# 13 features"
```

### 🔒 security-auditor
**Expertise:** Security vulnerabilities, input validation, authentication, data protection

**When to use:**
- Handling user input
- Storing sensitive data
- Network communications
- API endpoint security
- Trade validation logic

**Example invocation:**
```
"Review my token storage implementation"
"Is this Pokemon file upload handler secure?"
"How do I prevent trade exploitation?"
```

### 🎨 winforms-enhancer
**Expertise:** UI/UX design, WinForms modernization, responsive layouts, visual effects

**When to use:**
- UI performance issues
- Adding visual enhancements
- Improving user experience
- Creating custom controls
- Implementing animations

**Example invocation:**
```
"Make my bot status cards more visually appealing"
"Add a dark mode to the application"
"Create a responsive layout for the bot grid"
```

## 💡 Usage Examples

### Example 1: Debugging a Complex Issue
```
User: "My bot randomly disconnects during trades and the UI stops updating"

Claude will:
1. Invoke bug-hunter to identify the race condition
2. Use csharp-optimizer to suggest performance improvements
3. Provide a comprehensive solution with code examples
```

### Example 2: Implementing a New Feature
```
User: "I want to add a queue priority system for subscribers"

Claude will:
1. Use feature-developer to design the implementation
2. Invoke security-auditor to ensure secure permission checking
3. Have csharp-reviewer validate the approach
```

### Example 3: Performance Optimization
```
User: "Box operations are slow when searching for specific Pokemon"

Claude will:
1. Use pokemon-specialist for game-specific optimizations
2. Invoke csharp-optimizer for general performance improvements
3. Suggest caching strategies and parallel processing
```

## 🏆 Best Practices

### 1. **Be Specific**
The more specific your request, the better the agent can help:
- ❌ "Fix my code"
- ✅ "Fix the memory leak in my trade queue that occurs after 100+ trades"

### 2. **Provide Context**
Include relevant information:
- Which game (SV, SWSH, BDSP, etc.)
- Which component (Discord bot, WinForms UI, trade logic)
- Error messages or symptoms

### 3. **Use Multiple Agents**
Don't hesitate to request multiple perspectives:
```
"Implement a new feature and have it reviewed for security and performance"
```

### 4. **Follow Agent Recommendations**
Each agent provides specific output formats and checklists - use them to ensure completeness.

### 5. **Test Incrementally**
When implementing agent suggestions:
1. Make changes incrementally
2. Test after each change
3. Use the provided test cases
4. Monitor performance metrics

## 🤝 Contributing

To contribute new agents or improve existing ones:

1. Fork the repository at https://github.com/hexbyt3/sys-agents
2. Create a new branch for your changes
3. Follow the existing agent format:
   ```yaml
   ---
   name: agent-name
   description: Brief description
   model: sonnet
   ---
   
   [Agent instructions and expertise]
   ```
4. Submit a pull request with a clear description

### Agent Guidelines

- Focus on specific expertise areas
- Include practical code examples
- Reference actual SysBot.NET components
- Provide actionable recommendations
- Use consistent formatting

## 📚 Additional Resources

- [SysBot.NET Repository](https://github.com/kwsch/SysBot.NET)
- [PKHeX Documentation](https://github.com/kwsch/PKHeX)
- [Discord.Net Documentation](https://docs.stillu.cc/)
- [.NET 9 Documentation](https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-9)

## 📝 License

These agents are designed specifically for SysBot.NET development and follow the same license terms as the main project.

---

*Happy coding with SysBot.NET Claude Agents! 🚀*