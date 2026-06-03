# Contributing to EdgeGrid Client for Java

Thank you for your interest in contributing!

## Getting Started

1. Fork the repository and clone your fork.
2. Make sure you have **Java 21+** installed.
3. Build and run tests:

   ```bash
   ./mvnw clean verify -Ddependency-check.skip=true
   ```

4. Create a feature branch from `master`.

## Pull Requests

- Keep changes focused — one logical change per PR.
- Add or update tests for any new functionality.
- Ensure `./mvnw clean verify` passes before submitting.
- Follow the existing code style (4-space indentation, no tabs).

## Reporting Issues

Open an [issue](https://github.com/jkinley24/AkamaiOPEN-edgegrid-java/issues) with a clear description and, if applicable, a minimal reproduction.

## License

By contributing, you agree that your contributions will be licensed under the [Apache License 2.0](LICENSE).
