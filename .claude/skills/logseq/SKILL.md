```markdown
# logseq Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `logseq` codebase, a TypeScript project built with React. You'll learn about file naming, import/export styles, commit message conventions, and how to write and organize tests. This guide also provides command suggestions for common workflows.

## Coding Conventions

### File Naming
- **Style:** camelCase
- **Example:**  
  ```bash
  userSettings.ts
  noteEditor.tsx
  ```

### Import Style
- **Relative imports are preferred**
- **Example:**
  ```typescript
  import { getUserSettings } from './userSettings';
  import { NoteEditor } from '../components/noteEditor';
  ```

### Export Style
- **Named exports are used**
- **Example:**
  ```typescript
  // userSettings.ts
  export function getUserSettings() { ... }
  export const DEFAULT_SETTINGS = { ... };
  ```

### Commit Messages
- **Conventional commits with type prefixes**
- **Common prefix:** `chore`
- **Average length:** ~77 characters
- **Example:**
  ```
  chore: update dependencies to latest versions
  ```

## Workflows

### Creating a New Feature
**Trigger:** When adding new functionality
**Command:** `/new-feature`

1. Create a new file using camelCase naming.
2. Use relative imports to include dependencies.
3. Export your functions or components using named exports.
4. Write or update corresponding test files (`*.test.*`).
5. Commit your changes with a conventional commit message.

### Refactoring Code
**Trigger:** When improving or restructuring existing code
**Command:** `/refactor`

1. Identify the code to refactor.
2. Rename files using camelCase if needed.
3. Update imports to remain relative.
4. Ensure all exports remain named.
5. Update or add tests as necessary.
6. Commit with a message like `chore: refactor [module] for clarity`.

### Writing Tests
**Trigger:** When adding or updating tests
**Command:** `/write-test`

1. Create or update a test file matching the pattern `*.test.*`.
2. Write tests for your functions or components.
3. Run the test suite to ensure all tests pass.
4. Commit with a message like `chore: add tests for [feature]`.

## Testing Patterns

- **Test file naming:** Files follow the pattern `*.test.*` (e.g., `userSettings.test.ts`).
- **Testing framework:** Not explicitly detected; use standard TypeScript/React testing tools (e.g., Jest or React Testing Library).
- **Example:**
  ```typescript
  // userSettings.test.ts
  import { getUserSettings } from './userSettings';

  test('returns default settings', () => {
    expect(getUserSettings()).toEqual(DEFAULT_SETTINGS);
  });
  ```

## Commands
| Command         | Purpose                                      |
|-----------------|----------------------------------------------|
| /new-feature    | Scaffold a new feature following conventions |
| /refactor       | Refactor code according to project patterns  |
| /write-test     | Add or update tests for a module/component   |
```
