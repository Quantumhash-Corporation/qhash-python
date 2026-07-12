```markdown
# qhash-python Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and conventions used in the `qhash-python` repository, which is a TypeScript codebase. You'll learn about file naming, import/export styles, commit message practices, and how to structure and run tests. This guide is ideal for contributors aiming for consistency and maintainability in this project.

## Coding Conventions

### File Naming
- **PascalCase** is used for file names.
  - Example: `HashUtils.ts`, `QHashCore.ts`

### Imports
- **Relative import paths** are preferred.
  - Example:
    ```typescript
    import { HashFunction } from './HashUtils';
    ```

### Exports
- **Named exports** are used instead of default exports.
  - Example:
    ```typescript
    export function qhash(input: string): string { ... }
    export { qhash, HashFunction };
    ```

### Commit Messages
- **Freeform style** with no enforced prefixes.
- Average commit message length is about 35 characters.
  - Example:  
    ```
    Improve hash collision handling
    ```

## Workflows

### Adding a New Feature
**Trigger:** When implementing a new capability or function.
**Command:** `/add-feature`

1. Create a new TypeScript file using PascalCase (e.g., `NewFeature.ts`).
2. Use relative imports to include dependencies.
3. Export your functions or classes using named exports.
4. Write corresponding tests in a file named `NewFeature.test.ts`.
5. Commit your changes with a clear, concise message.

### Fixing a Bug
**Trigger:** When resolving a defect or issue.
**Command:** `/fix-bug`

1. Identify the affected file(s).
2. Make code changes, following coding conventions.
3. Update or add relevant test cases in `*.test.ts` files.
4. Commit the fix with a descriptive message.

### Writing Tests
**Trigger:** When adding or updating tests.
**Command:** `/write-tests`

1. Create or update a test file matching `*.test.ts` for the module.
2. Write test cases using the project's preferred (unknown) test framework.
3. Ensure all tests pass before committing.

## Testing Patterns

- Test files follow the pattern: `*.test.ts`
  - Example: `HashUtils.test.ts`
- The specific test framework is not detected; follow existing patterns in the repo.
- Place tests alongside or near the code they test.

## Commands
| Command       | Purpose                                      |
|---------------|----------------------------------------------|
| /add-feature  | Start the workflow for adding a new feature  |
| /fix-bug      | Begin the process for fixing a bug           |
| /write-tests  | Guide for writing or updating tests          |
```
