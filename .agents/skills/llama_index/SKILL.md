```markdown
# llama_index Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns, conventions, and workflows used in the `llama_index` TypeScript codebase. You'll learn how to structure files, write imports and exports, and understand the project's approach to testing. This guide is ideal for contributors who want to maintain consistency and quality in their code contributions.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `dataProcessor.ts`, `indexBuilder.ts`

### Import Style
- Use **relative imports** for modules within the repository.
  - Example:
    ```typescript
    import { processData } from './dataProcessor';
    ```

### Export Style
- Use **named exports** for functions, classes, and constants.
  - Example:
    ```typescript
    export function buildIndex(data: DataType): IndexType { ... }
    export const DEFAULT_CONFIG = { ... };
    ```

### Commit Messages
- Commit messages are **freeform** with no strict prefix, averaging around 55 characters.
  - Example: `Fix bug in index builder for empty datasets`

## Workflows

### Adding a New Module
**Trigger:** When you need to introduce new functionality.
**Command:** `/add-module`

1. Create a new file using camelCase naming (e.g., `myNewModule.ts`).
2. Implement your logic using named exports.
3. Use relative imports for any dependencies within the repo.
4. Write corresponding tests in a file named `myNewModule.test.ts`.
5. Commit your changes with a clear, concise message.

### Updating an Existing Feature
**Trigger:** When modifying or extending current functionality.
**Command:** `/update-feature`

1. Locate the relevant module using camelCase file names.
2. Make your changes, ensuring you use named exports.
3. Update or add tests as needed in the corresponding `*.test.ts` file.
4. Commit with a descriptive message.

### Running Tests
**Trigger:** When you want to verify code correctness.
**Command:** `/run-tests`

1. Identify test files matching the `*.test.*` pattern.
2. Use the project's test runner (framework unknown; check project docs or package.json).
3. Run all or specific tests to ensure your changes are correct.

## Testing Patterns

- Test files follow the pattern: `*.test.*` (e.g., `dataProcessor.test.ts`).
- The specific testing framework is unknown; refer to project documentation for details.
- Place tests alongside or near the modules they cover.
- Example test file name: `indexBuilder.test.ts`

## Commands

| Command         | Purpose                                      |
|-----------------|----------------------------------------------|
| /add-module     | Scaffold a new module with tests             |
| /update-feature | Guide for updating existing functionality     |
| /run-tests      | Run all tests in the repository              |
```
