# Debug and Fix - Intelligent Error Resolution Pipeline

Systematically debug, fix, test, and prevent errors using specialized agents working in coordination.

## Usage

```bash
debug-and-fix "TypeError: Cannot read property 'name'"   # Debug specific error
debug-and-fix @error.log                                # Debug from log file
debug-and-fix --last-error                              # Debug most recent error
debug-and-fix @sentry-link                              # Debug from error tracking
```

## Workflow

### Phase 1: Investigation
1. **debugger** - Root cause analysis and investigation
2. **code-reviewer** - Identifies related code quality issues

### Phase 2: Resolution  
3. **typescript-expert** / **python-expert** - Implements type-safe fix
4. **refactoring-expert** - Improves code to prevent similar issues

### Phase 3: Validation
5. **test-generator** - Creates tests to prevent regression
6. **code-reviewer** - Validates fix and identifies edge cases

### Phase 4: Prevention
7. **documentation-writer** - Documents the issue and solution

## Error Categories

### Runtime Errors
```bash
debug-and-fix "ReferenceError: user is not defined"

# Agents will:
- Trace variable scope issues
- Add proper declarations
- Implement null checks
- Add TypeScript types
```

### Type Errors
```bash
debug-and-fix "Type 'string' is not assignable to type 'number'"

# Agents will:
- Fix type mismatches
- Add proper type guards
- Improve type definitions
- Add runtime validation
```

### Async Errors
```bash
debug-and-fix "UnhandledPromiseRejectionWarning"

# Agents will:
- Add proper error handling
- Implement try-catch blocks
- Fix async/await usage
- Add error boundaries
```

### Performance Issues
```bash
debug-and-fix "Maximum call stack exceeded"

# Agents will:
- Identify infinite loops
- Optimize recursive functions  
- Implement iterative solutions
- Add performance monitoring
```

## Advanced Features

### Pattern Detection
The system identifies common error patterns:
- N+1 queries → Batch loading
- Memory leaks → Proper cleanup
- Race conditions → Synchronization
- Null pointer → Optional chaining

### Multi-File Analysis
```bash
debug-and-fix "Module not found" --deep
```
Analyzes import chains and dependencies

### Historical Analysis
```bash
debug-and-fix --analyze-patterns @logs/
```
Identifies recurring issues and systemic problems

## Output Example

```
🔍 Debugging: TypeError: Cannot read property 'map' of undefined

📊 Investigation Phase:
- Error location: UserList.tsx:45
- Cause: API returns null instead of empty array
- Related issues: 3 similar patterns found

🛠️ Resolution:
✅ Added null check with default value
✅ Implemented proper TypeScript types
✅ Added loading and error states
✅ Refactored to use optional chaining

🧪 Test Coverage:
✅ Test for null response
✅ Test for empty array
✅ Test for error response
✅ Integration test added

🛡️ Prevention:
✅ Added API response validation
✅ Created error boundary component
✅ Documented in troubleshooting guide

✨ Issue Resolved!
- Root cause fixed
- Tests prevent regression
- Similar issues prevented
```

## Options

- `--deep` - Deep analysis across codebase
- `--prevent` - Focus on prevention strategies
- `--performance` - Include performance analysis
- `--security` - Check for security implications
- `--history` - Analyze error history

## Error Sources

### From Error Tracking
```bash
debug-and-fix @sentry:12345      # Sentry issue ID
debug-and-fix @rollbar:error-id  # Rollbar error
debug-and-fix @bugsnag:crash-id  # Bugsnag crash
```

### From CI/CD
```bash
debug-and-fix @github-action:failed
debug-and-fix @jenkins:build-123
```

### From Logs
```bash
debug-and-fix @production.log --filter "ERROR"
debug-and-fix @nginx/error.log
```

## Prevention Strategies

The command implements:
1. **Error Boundaries** - React error boundaries
2. **Type Safety** - TypeScript strict mode
3. **Validation** - Input/output validation
4. **Monitoring** - Error tracking setup
5. **Documentation** - Troubleshooting guides

## When to Use

- Production errors
- Development bugs
- Test failures
- Performance issues
- Recurring problems
- Complex debugging scenarios