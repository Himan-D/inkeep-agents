```markdown
# inkeep-agents Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns and workflows used in the `inkeep-agents` TypeScript codebase. You'll learn about file naming, import/export conventions, commit message standards, and how to write and run tests. This guide is ideal for contributors aiming for consistency and maintainability in the project.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `myAgent.ts`, `userProfile.test.ts`

### Import Style
- Use **relative imports** for modules within the repository.
  - Example:
    ```typescript
    import { fetchData } from './utils/fetchData';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // In utils/fetchData.ts
    export function fetchData() { ... }
    ```

### Commit Messages
- Follow **Conventional Commits** with the `build` prefix.
  - Example:
    ```
    build: update dependencies for security patch
    ```

## Workflows

### Code Contribution
**Trigger:** When adding new features or making changes
**Command:** `/contribute`

1. Create a new branch from `main`.
2. Write code using camelCase file naming and relative imports.
3. Use named exports for all modules.
4. Write or update corresponding test files (`*.test.ts`).
5. Commit changes using the conventional commit format with the `build` prefix.
6. Open a pull request for review.

### Running Tests
**Trigger:** After making code changes or before merging
**Command:** `/run-tests`

1. Locate test files matching the `*.test.*` pattern.
2. Run the test suite using your preferred test runner (framework is not specified).
   - Example (if using Jest):
     ```
     npx jest
     ```
3. Ensure all tests pass before submitting changes.

## Testing Patterns

- Test files follow the `*.test.*` pattern (e.g., `userProfile.test.ts`).
- The testing framework is unspecified; check project documentation or scripts for details.
- Place tests alongside the code they cover or in a dedicated `tests` directory.

### Example Test File
```typescript
// userProfile.test.ts
import { getUserProfile } from './userProfile';

describe('getUserProfile', () => {
  it('should return user data', () => {
    const result = getUserProfile('user123');
    expect(result).toBeDefined();
  });
});
```

## Commands
| Command        | Purpose                                   |
|----------------|-------------------------------------------|
| /contribute    | Start the code contribution workflow      |
| /run-tests     | Run all test files in the repository      |
```
