# Update Progress Documentation

## Alias
`update` = Update the progress.md file with current session accomplishments

## Description
This command analyzes the current Claude Code session and updates the `specs/progress.md` file with:
- Current date and timestamp (Claude automatically knows today's date from the environment)
- Summary of features implemented
- Files created or modified
- Key architectural decisions made
- Next steps or pending tasks

## How Date/Time Works
Claude has access to the current date through the environment context. When you run the `update` command, Claude will:
1. Check the current date from the environment in format "Today's date: YYYY-MM-DD"
   - YYYY = 4-digit year
   - MM = 2-digit month (01=Jan, 02=Feb, ..., 07=Jul, ..., 12=Dec)
   - DD = 2-digit day
2. Extract and use this exact date for the progress entry header
3. Example: "Today's date: 2025-07-14" → "## 2025-07-14 - Session Summary"

IMPORTANT: Always use the exact date from the environment. Do not modify or misinterpret the month value.

## Usage
Simply type `update` at the end of a coding session to document your progress.

## What it does
1. Reviews the conversation history
2. Identifies completed tasks and implementations
3. Lists all files that were created or modified
4. Appends a new entry to `specs/progress.md` with timestamp
5. Preserves all previous progress entries

## File Format
The progress.md file will be structured with entries like:
```markdown
## [Date] - Session Summary
### Features Implemented
- Feature 1
- Feature 2

### Files Modified
- `path/to/file1.ts` - Description of changes
- `path/to/file2.tsx` - Description of changes

### Key Decisions
- Decision 1
- Decision 2

### Next Steps
- Task 1
- Task 2
```

## Notes
- Each update appends to the file, creating a chronological log
- The file serves as a development journal for the project
- Useful for tracking progress over time and onboarding new developers