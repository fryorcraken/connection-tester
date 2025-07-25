# AGENTS.md - Development Guidelines

## Build/Test Commands
- `npm run build` - Build the project
- `npm run test` - Run all tests
- `npm run test -- --testNamePattern="specific test"` - Run single test
- `npm run lint` - Run ESLint
- `npm run typecheck` - Run TypeScript compiler check
- `npm run dev` - Start development server

## Code Style Guidelines
- Use TypeScript with strict mode enabled
- Import order: external libraries, internal modules, relative imports
- Use camelCase for variables/functions, PascalCase for classes/types
- Prefer `const` over `let`, avoid `var`
- Use async/await over Promises.then()
- Handle errors with try/catch blocks, don't ignore Promise rejections
- Use descriptive variable names (e.g., `connectionStatus` not `status`)
- Export types and interfaces explicitly
- Use JSDoc comments for public APIs
- Prefer composition over inheritance
- Use optional chaining (`?.`) and nullish coalescing (`??`)
- Keep functions small and focused (single responsibility)
- Use meaningful commit messages following conventional commits format