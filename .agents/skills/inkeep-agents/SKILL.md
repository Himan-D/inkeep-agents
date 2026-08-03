```markdown
# inkeep-agents Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides guidance on contributing to the `inkeep-agents` TypeScript codebase. It covers repository-specific coding conventions, commit message patterns, file organization, and testing approaches. By following these patterns, contributors can ensure consistency and maintainability across the project.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `myAgent.ts`, `userProfile.test.ts`

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { myFunction } from './utils';
    ```

### Export Style
- Use **named exports**.
  - Example:
    ```typescript
    // In utils.ts
    export function myFunction() { ... }

    // In another file
    import { myFunction } from './utils';
    ```

### Commit Messages
- Follow **Conventional Commits**.
- Use prefixes such as `build`.
- Keep commit messages concise (average ~75 characters).
  - Example:
    ```
    build: update dependencies to latest versions
    ```

## Workflows

### Building the Project
**Trigger:** When you want to build or update the project dependencies.
**Command:** `/build`

1. Ensure your dependencies are up to date.
2. Run the build command (typically `npm run build` or `yarn build`).
3. Commit changes with a `build:` prefix in the commit message.

### Writing and Running Tests
**Trigger:** When adding new features or fixing bugs.
**Command:** `/test`

1. Create or update test files following the `*.test.*` naming pattern.
2. Use the project's preferred testing framework (not specified; check existing tests).
3. Run the test suite (commonly `npm test` or `yarn test`).
4. Ensure all tests pass before committing.

## Testing Patterns

- Test files are named using the `*.test.*` pattern (e.g., `myAgent.test.ts`).
- The specific testing framework is not detected; refer to existing test files for guidance.
- Place tests alongside the code they test or in a dedicated `tests` directory if present.

**Example:**
```typescript
// myAgent.test.ts
import { myAgent } from './myAgent';

describe('myAgent', () => {
  it('should perform expected behavior', () => {
    expect(myAgent()).toBe(true);
  });
});
```

## Commands
| Command   | Purpose                                 |
|-----------|-----------------------------------------|
| /build    | Build the project and update dependencies|
| /test     | Run the test suite                      |
```
