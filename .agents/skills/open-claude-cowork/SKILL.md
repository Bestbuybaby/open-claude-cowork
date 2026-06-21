```markdown
# open-claude-cowork Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development conventions and workflows used in the `open-claude-cowork` repository. The project is built with TypeScript using the Express framework, and follows clear, consistent patterns for file naming, imports, exports, and commit messages. You'll learn how to structure code, write and organize tests, and understand the project's workflow conventions.

## Coding Conventions

### File Naming
- All files are named using **kebab-case**.
- Example:  
  ```
  user-controller.ts
  api-routes.ts
  ```

### Import Style
- Use **relative imports** for referencing local modules.
- Example:
  ```typescript
  import { getUser } from './user-service';
  import { apiRoutes } from '../routes/api-routes';
  ```

### Export Style
- Use **named exports** for all modules.
- Example:
  ```typescript
  // user-service.ts
  export function getUser(id: string) { ... }

  // Usage
  import { getUser } from './user-service';
  ```

### Commit Messages
- Follow the **Conventional Commits** specification.
- Use prefixes such as `build`.
- Example:
  ```
  build: add Dockerfile for containerization
  ```

## Workflows

### Build Process
**Trigger:** When you need to build the project for deployment or testing  
**Command:** `/build`

1. Ensure all dependencies are installed.
2. Run the TypeScript compiler to transpile code.
3. Bundle or prepare assets as needed.

### Adding a New Feature
**Trigger:** When implementing a new feature  
**Command:** `/feature`

1. Create a new branch for your feature.
2. Implement the feature following coding conventions.
3. Write corresponding tests in a `*.test.*` file.
4. Commit changes using a conventional commit message.
5. Open a pull request for review.

### Writing Tests
**Trigger:** When adding or updating code that requires testing  
**Command:** `/test`

1. Create a test file matching the pattern `*.test.*` in the relevant directory.
2. Write tests for your code (testing framework is currently unknown).
3. Run the test suite to ensure all tests pass.

## Testing Patterns

- Test files follow the pattern: `*.test.*` (e.g., `user-service.test.ts`).
- Place test files alongside or near the modules they test.
- The specific testing framework is not detected, so follow existing patterns in the repository.

## Commands
| Command   | Purpose                                         |
|-----------|-------------------------------------------------|
| /build    | Build the project for deployment or testing     |
| /feature  | Start a new feature implementation workflow     |
| /test     | Run or add tests for your code                  |
```
