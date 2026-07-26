```markdown
# mergepay-web Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill introduces the core development conventions and workflows for the `mergepay-web` TypeScript codebase. It covers file naming, import/export styles, commit patterns, and testing approaches, providing practical examples and command suggestions to streamline your development process.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userProfile.ts`, `paymentGateway.ts`

### Import Style
- Use **alias imports** for modules.
  ```typescript
  import { fetchUser } from '@services/userService';
  ```

### Export Style
- Prefer **named exports**.
  ```typescript
  // In userProfile.ts
  export function getUserProfile(id: string) { ... }
  ```

### Commit Patterns
- Use **Conventional Commits** with the `feat` prefix for new features.
  - Example commit message:
    ```
    feat: add user profile page with payment integration
    ```

## Workflows

### Creating a New Feature
**Trigger:** When adding a new feature to the codebase  
**Command:** `/new-feature`

1. Create a new file using camelCase naming.
2. Implement the feature using TypeScript.
3. Use alias imports for dependencies.
4. Export your functions or components as named exports.
5. Write corresponding tests in a `.test.ts` file.
6. Commit your changes using the `feat` prefix and a descriptive message.

### Writing Tests
**Trigger:** When adding or updating functionality  
**Command:** `/write-test`

1. Create a test file with the `.test.ts` suffix.
   - Example: `userProfile.test.ts`
2. Write test cases for your functions or components.
3. Use the project's preferred (unknown) testing framework.
4. Run tests to ensure correctness.

## Testing Patterns

- Test files are named with the `.test.ts` suffix and placed alongside the code they test.
- The specific testing framework is not detected, but follow the pattern:
  ```typescript
  // userProfile.test.ts
  import { getUserProfile } from './userProfile';

  describe('getUserProfile', () => {
    it('should return user data for a valid ID', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command        | Purpose                                     |
|----------------|---------------------------------------------|
| /new-feature   | Scaffold and commit a new feature           |
| /write-test    | Create and run tests for new functionality  |
```
