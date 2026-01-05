# Contributing to DevTrackr

Thank you for your interest in contributing to DevTrackr! This document provides guidelines and instructions for contributing.

## Code of Conduct

By participating in this project, you agree to maintain a respectful and inclusive environment for all contributors.

## Getting Started

1. Fork the repository
2. Clone your fork: `git clone https://github.com/YOUR_USERNAME/Devtrackrnpm.git`
3. Install dependencies: `npm install`
4. Create a branch: `git checkout -b feature/your-feature-name`

## Development Workflow

### Running Tests

```bash
# Run all tests
npm test

# Run unit tests only
npm run test:unit

# Run integration tests only
npm run test:integration

# Watch mode
npm run test:watch
```

### Type Checking

```bash
npm run type-check
```

### Building

```bash
npm run build
```

### Code Style

We use ESLint and Prettier for code formatting:

```bash
# Check formatting
npm run format:check

# Fix formatting
npm run format

# Lint code
npm run lint

# Fix linting issues
npm run lint:fix
```

## Making Changes

### Before You Start

- Check existing issues and pull requests to avoid duplicate work
- For major changes, open an issue first to discuss the approach
- Ensure your changes align with the project's goals and architecture

### Commit Messages

Follow conventional commits:

- `feat:` New feature
- `fix:` Bug fix
- `docs:` Documentation changes
- `test:` Test additions or changes
- `refactor:` Code refactoring
- `chore:` Maintenance tasks

Example: `feat: add input validation for username parameter`

### Pull Request Process

1. Ensure all tests pass: `npm test`
2. Ensure type checking passes: `npm run type-check`
3. Ensure build succeeds: `npm run build`
4. Update documentation if needed
5. Create a pull request with a clear description

### PR Checklist

- [ ] Tests pass locally
- [ ] Type checking passes
- [ ] Build succeeds
- [ ] Code follows project style
- [ ] Documentation updated
- [ ] No new warnings or errors

## Testing Guidelines

### Unit Tests

- Test normalization functions thoroughly
- Test edge cases (empty data, null values, etc.)
- Never mock normalization logic
- Use fixtures from `tests/fixtures/`

### Integration Tests

- Mock `fetch` at the test level (not in source)
- Test all error paths (401, 403, network errors)
- Use fixtures for API responses
- Never make real API calls in tests

## Architecture Guidelines

### Public API

- Only export from `src/index.ts`
- No internal modules should be importable
- Maintain backward compatibility for 1.x versions

### Error Handling

- Use typed error classes
- Include helpful error messages
- Expose rate limit information when available

### Type Safety

- Use strict TypeScript
- Export all public types
- Avoid `any` types

## Questions?

Open an issue with the `question` label, and we'll be happy to help!
