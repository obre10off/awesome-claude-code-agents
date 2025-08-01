# Quality Sprint - Comprehensive Code Quality Improvement

Run a complete quality improvement sprint on your codebase using multiple specialized agents in sequence.

## Usage

```bash
quality-sprint           # Run on current directory
quality-sprint @src/     # Run on specific directory  
quality-sprint @file.js  # Run on specific file
```

## Workflow

This command orchestrates the following agents in sequence:

1. **code-reviewer** - Identifies all quality issues, security vulnerabilities, and improvements
2. **refactoring-expert** - Implements improvements and applies best practices
3. **test-generator** - Creates comprehensive test coverage for refactored code
4. **documentation-writer** - Updates documentation to reflect changes
5. **code-reviewer** (final) - Validates all improvements meet quality standards

## What Gets Improved

- **Code Quality**: SOLID principles, DRY, clean code patterns
- **Security**: Input validation, authentication, SQL injection prevention
- **Performance**: Algorithm optimization, caching, query optimization  
- **Testing**: Unit tests, integration tests, edge cases
- **Documentation**: Updated comments, API docs, README sections

## Example Output

```
🚀 Quality Sprint Starting...

📊 Initial Analysis (code-reviewer)
- 15 code smells detected
- 3 security vulnerabilities found
- 8 performance improvements identified

🔧 Refactoring Phase (refactoring-expert)
✅ Extracted 5 methods for clarity
✅ Implemented proper error handling
✅ Optimized database queries
✅ Applied SOLID principles

🧪 Test Generation (test-generator)
✅ Created 25 unit tests (95% coverage)
✅ Added 8 integration tests
✅ Included edge case testing

📝 Documentation Update (documentation-writer)
✅ Updated function documentation
✅ Added API examples
✅ Improved README sections

✨ Final Review (code-reviewer)
- All issues resolved
- Code quality: A+
- Security: Passed
- Test coverage: 95%

🎉 Quality Sprint Complete!
```

## Options

- `--focus security` - Emphasize security improvements
- `--focus performance` - Emphasize performance optimization
- `--skip-tests` - Skip test generation phase
- `--interactive` - Approve changes at each step

## When to Use

- Before major releases
- After inheriting legacy code
- During refactoring sprints
- When technical debt is high
- For code review preparation