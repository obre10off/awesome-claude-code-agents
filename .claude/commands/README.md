# 🎯 Claude Code Custom Commands

Powerful slash commands that orchestrate multiple agents to deliver complete development workflows.

## 📋 Available Commands

### 🏆 Quality & Refactoring

#### `/quality-sprint`
Run a comprehensive code quality improvement sprint using multiple agents.
```bash
quality-sprint @src/          # Improve entire source directory
quality-sprint @file.js       # Focus on specific file
```
**Agents**: code-reviewer → refactoring-expert → test-generator → documentation-writer

---

### 🎨 Design & UI

#### `/design-to-code`
Transform mockups and screenshots into production-ready components with design systems.
```bash
design-to-code @mockup.png              # Convert single design
design-to-code @designs/ --framework react  # Batch conversion
```
**Agents**: visual-design-extractor → typescript-expert → test-generator → documentation-writer

---

### 🚀 Feature Development

#### `/full-stack-feature`
Implement complete features with backend, frontend, tests, and documentation.
```bash
full-stack-feature "user authentication"    # Auth system
full-stack-feature "payment processing"     # Payment feature
```
**Agents**: Multiple specialists working in coordinated phases

---

### 🐛 Debugging & Fixes

#### `/debug-and-fix`
Systematic debugging with root cause analysis, fixes, and prevention.
```bash
debug-and-fix "TypeError: Cannot read property"  # Specific error
debug-and-fix @error.log                        # From logs
```
**Agents**: debugger → language-expert → test-generator → documentation-writer

---

### 🔌 API Development

#### `/api-first`
Design-first API development with OpenAPI spec, implementation, and docs.
```bash
api-first "user management API"        # REST API
api-first "products API" --graphql    # GraphQL API
```
**Agents**: documentation-writer → language-expert → test-generator → code-reviewer

---

### 🔧 Utility Commands

#### `/gemini-cli`
Analyze large codebases using Gemini's massive context window.
```bash
gemini -p "@src/ Analyze the architecture"
gemini -p "@./ Is rate limiting implemented?"
```
**Note**: Requires Gemini CLI installation

---

## 🎯 Quick Selection Guide

| Goal | Command | Time |
|------|---------|------|
| Improve code quality | `/quality-sprint` | 10-20 min |
| Implement UI from design | `/design-to-code` | 5-15 min |
| Build new feature | `/full-stack-feature` | 20-40 min |
| Fix bugs | `/debug-and-fix` | 5-15 min |
| Create API | `/api-first` | 15-30 min |
| Analyze large codebase | `/gemini-cli` | 2-5 min |

## 💡 Pro Tips

### Combine Commands
```bash
# Design → Implementation → Quality
design-to-code @mockup.png
full-stack-feature "dashboard using new components"
quality-sprint @src/dashboard/
```

### Use Options
Most commands support options:
- `--framework [react|vue|angular]`
- `--language [typescript|python|go]`
- `--focus [security|performance|quality]`
- `--interactive` - Approve changes at each step

### Batch Operations
```bash
# Process multiple files
quality-sprint @src/**/*.js
design-to-code @designs/*.png
```

## 🔮 Coming Soon

- `/performance-boost` - Comprehensive performance optimization
- `/security-audit` - Security vulnerability scanning and fixes
- `/test-coverage` - Achieve 100% test coverage
- `/modernize-legacy` - Upgrade legacy codebases
- `/ci-cd-setup` - Complete CI/CD pipeline setup

## 🛠️ Creating Custom Commands

1. Create a markdown file in `.claude/commands/`
2. Describe the workflow and agent orchestration
3. Follow the existing command format
4. Test thoroughly

Example structure:
```markdown
# Command Name - Brief Description

## Usage
\```bash
command-name [arguments] [options]
\```

## Workflow
1. **agent-name** - What it does
2. **agent-name** - What it does

## Options
- `--option` - Description

## When to Use
- Scenario 1
- Scenario 2
```

## 📚 Command Categories

### Development Acceleration
- `full-stack-feature` - Complete feature implementation
- `api-first` - API development
- `design-to-code` - UI implementation

### Quality Improvement  
- `quality-sprint` - Code quality enhancement
- `debug-and-fix` - Error resolution
- `test-coverage` - Testing improvement

### Analysis & Understanding
- `gemini-cli` - Large codebase analysis
- `architecture-review` - System design analysis

### Maintenance & Operations
- `modernize-legacy` - Legacy code updates
- `security-audit` - Security scanning
- `performance-boost` - Performance optimization

---

**Remember**: These commands are designed to make you incredibly productive. Use them liberally!