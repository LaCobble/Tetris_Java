# Contributing

Thanks for your interest! This is an archived school project, kept as a portfolio piece: small fixes and improvements are welcome, large rewrites are not the goal.

## Prerequisites

- JDK 17 with JavaFX 17: either a JDK that bundles JavaFX (for example Azul Zulu "JDK FX"), or a plain JDK plus the [JavaFX SDK](https://gluonhq.com/products/javafx/).

## Build and run

```bash
# With a plain JDK, add: --module-path /path/to/javafx-sdk/lib --add-modules javafx.controls,javafx.fxml
javac -encoding UTF-8 -d out $(find Tetris/src/main/java -name '*.java' ! -name module-info.java)
java -cp out:Tetris/src/main/resources com.example.tetris.Main
```

## Workflow

1. Open an issue first for anything beyond a small fix.
2. Create a branch from `main` named `type/short-topic` (`fix/…`, `feat/…`, `docs/…`, `chore/…`).
3. Write commits following [Conventional Commits](https://www.conventionalcommits.org/) (`type(scope): description`), the body explaining *why*.
4. Open a pull request using the template; the CI must be green.
5. Pull requests are merged with **squash and merge**.

## Versioning

The project follows [Semantic Versioning](https://semver.org/). Record user-visible changes under `## [Unreleased]` in [CHANGELOG.md](CHANGELOG.md). A release is published by pushing a `vX.Y.Z` tag on `main`: the Release workflow creates the GitHub Release from the matching CHANGELOG section.

## Rules

- Never commit secrets, credentials or personal data.
- By contributing, you agree to follow the [Code of Conduct](CODE_OF_CONDUCT.md) and that your contribution is licensed under the [MIT License](LICENSE).
