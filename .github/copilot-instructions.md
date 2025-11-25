# Copilot Instructions for test-github-action

## Repository Overview

This repository is for testing GitHub Actions and related workflows. It serves as a testing ground for CI/CD configurations and automation.

## Development Workflow

- Follow conventional commits for commit messages
- Create feature branches for new functionality
- Use pull requests for code review before merging to main

## Code Style and Conventions

- Keep code clean and well-documented
- Follow the principle of least surprise
- Write self-documenting code with clear variable and function names
- Add comments only when necessary to explain complex logic

## Testing Guidelines

- Write tests for new features and bug fixes
- Ensure all tests pass before submitting a pull request
- Include both positive and negative test cases
- Mock external dependencies appropriately

## Documentation Standards

- Keep the README.md up to date with any new features or changes
- Document configuration options and environment variables
- Include examples for common use cases
- Update documentation as part of the same pull request as code changes

## GitHub Actions Specific Guidelines

- Test action workflows locally when possible before committing
- Use descriptive names for workflow files and jobs
- Include appropriate triggers for workflows
- Add comments to explain complex workflow logic
- Keep secrets secure and never commit them to the repository
- Use environment variables for configuration
- Pin action dependencies to specific versions for stability

## Best Practices

- Make atomic commits that represent a single logical change
- Write clear, descriptive commit messages
- Keep pull requests focused and reasonably sized
- Respond to code review feedback promptly
- Update or close stale issues and pull requests
