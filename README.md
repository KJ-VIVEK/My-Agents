# My Agents

A specialized team of AI agents designed to accelerate development workflows. Each agent is optimized for specific tasks and operates within VS Code for seamless integration.

## Core Agents

### 1. **Developer Assistant**
Analyzes code architecture and design patterns. Provides recommendations for scalability, modularity, separation of concerns, and code flow optimization. Reviews code structure against SOLID principles and best practices without implementing changes.

**Capabilities**:
- Architectural analysis and recommendations
- Code flow and data flow analysis
- Scalability and modularity assessments
- Design pattern evaluation
- Structured guidance format (Issue → Rationale → Recommendation → Benefits)

### 2. **Clean Code Executioner**
Enforces clean code principles and language quality standards. Reviews code structure against Uncle Bob's clean code standards and improves written communication in documentation, comments, and user-facing strings.

**Capabilities**:
- Grammar, spelling, and clarity review
- Naming convention validation (meaningful names)
- Function design analysis (single responsibility, parameter limits)
- Error handling patterns
- Testing patterns and code formatting
- C language-specific guidance

### 3. **Git Executioner**
Manages source control workflows with precision. Handles git operations including branching, committing, and pushing changes to remote repositories.

**Capabilities**:
- Branch management
- Staged and unstaged change handling
- Commit creation with descriptive messages
- Remote repository operations
- Git workflow automation

### 4. **Code Architect**
Provides high-level architectural guidance and design patterns for complex systems.

### 5. **Code Gatekeeper**
Enforces coding standards and review gates to maintain quality thresholds.

### 6. **English Janitor**
Refines written content, documentation, and communication materials for clarity and professionalism.

## Usage

Each agent can be invoked through VS Code's chat interface with the `#agent` command or through the VS Code command palette. Agents are designed to work independently or in coordination for comprehensive code review and development support.

## Design Principles

- **Analysis Only**: Agents provide recommendations without implementing changes (unless specified)
- **Token Efficiency**: Optimized for minimal token usage while maintaining clarity
- **Deterministic Output**: Structured guidance formats for predictable, consistent results
- **Integration**: Seamless VS Code integration for workflow efficiency
- **Specialization**: Each agent optimized for specific development tasks