# index.mdc

This file offers guidelines for Cursor when interacting with code in this repository. The rules outlined below are consistently applied during every chat session.

## Core Principles
- DRY (Don’t Repeat Yourself): eliminate duplicated logic; extract shared utilities.
- Separation of Concerns: each module handles one kind of responsibility.
- Single Responsibility: one reason to change per class/module/function/file.
- Clear Abstractions & Contracts: expose intent via small, stable interfaces; hide implementation details.
- Low Coupling, High Cohesion: minimize cross-module knowledge; keep related code together.
- Explicit Boundaries: keep core logic independent from I/O, UI, frameworks, storage, and transport.

## Fundamentals
- Write clean simple, readable code
- Implement feature in the simplest possible way
- Keep files small and focused (<200 lines)
- Test after every meaningful change
- Focus and core functionality before optimization
- Use clear, consistent naming
- Think thoroughly before coding, Write 2-3 reasoning paragraphs
- ALWAYS write simple, clean and modular code
- Use clear and easy-to-understand language, write in short sentences

## Comments
- ALWAYS try to add more helpful and explanatory comments into our codebase
- NEVER delete old comments - unless they are obviously wrong / Obsolete
- Include LOTS of explanatory comments in your code. ALWAYS write well documented code.
- Document all changes and their reasoning IN THE COMMENTS YOU WRITING
- When writing comments, use clear and easy-to-understand language, with sort sentences.

# Testing Guidelines
- Use Vitest as the unit testing framework.
- Import testing functions (e.g., `test`, `describe`) explicitly instead of relying on the global Vitest API.
- Name unit test files with the `.spec.ts` suffix (or `.spec.js` for JavaScript).
- Keep unit test files in the same directory as their corresponding source files, rather than in a separate `__tests__` directory.
- Isolate dependencies by using mocking and stubbing where necessary. Prefer `vi.spyOn` over `vi.mock` for more targeted mocking.
- DON'T run unit test with `pnpm test` or `npm run test`, it will required user input to continue. Use `pnpm run test:ci` instead for a single run. 
- Each test should be independent
- Use descriptive test names
- Clean up mocks between tests when not done automatically
- After creating a unit test, test them by running `pnpm test:ci`
- Limit the summary of changes.
  
# Commit Guidelines

We follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) style for our commit messages

Rules:  
- use lower case for the complete commit messages (summary line and description)
- use the imperative mood in the summary line
- keep the summary line concise

The first line of the commit message should be a short summary of the changes made. This should be followed by a blank line and then a more detailed description of the changes, if necessary.

The summary line starts with a type** (`feat`, `fix`, `docs`, etc.) based on the primary intent 
Use these types:
- `feat: add new user authentication module`
- `fix: resolve issue with data fetching.`
- `docs: update README with installation instructions`
- `style: format code with Prettier`
- `refactor: improve performance of data processing`
- `test: add unit tests for user service`
- `chore: update dependencies, scripts and build stuff`

Additionally, a scope is added to the commit message in parentheses to specify the area of the codebase that is affected. The scope should be a short, lowercase identifier that describes the part of the codebase being modified. For example, if you are making changes to the authentication module, you might use `auth` as the scope.
An example would be:
- `fix(auth): resolve issue with user login`
- `feat(auth): add new user authentication module`

The commit message should also include a detailed description of the changes made in the commit after the summary line if necessary.
Always use a bullet list to describe the changes made in the commit. This makes it easier to read and understand the changes at a glance.
