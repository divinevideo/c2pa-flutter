# Repository Guidelines

## Project Structure & Module Organization
- Flutter plugin source lives in `lib/`, with platform code under `android/` and `ios/`.
- Tests live in `test/`.
- The example app lives in `example/`.
- Keep plugin API, platform channel, and manifest-validation logic separated where practical instead of growing broad shared files.

## Build, Test, and Development Commands
- `flutter pub get`: install Dart and Flutter dependencies.
- `flutter analyze`: run static analysis.
- `flutter test`: run the test suite.
- Use the example app for manual validation when changing platform integration or signing behavior.
- Keep `README.md` and `example/` aligned with any public API changes.

## Coding Style & Naming Conventions
- Use idiomatic Dart and Flutter patterns, with clear public API types and focused classes.
- Prefer small platform-specific changes over mixing iOS and Android concerns in the same refactor unless the change truly spans both.
- Keep PRs tightly scoped. Do not mix unrelated cleanup, formatting churn, or speculative refactors into the same change.
- Temporary or transitional code must include `TODO(#issue):` with the tracking issue for removal.

## Pull Request Guardrails
- PR titles must use Conventional Commit format: `type(scope): summary` or `type: summary`.
- Set the correct PR title when opening the PR. Do not rely on fixing it afterward.
- If a PR title changes after opening, verify that the semantic PR title check reruns successfully.
- PR descriptions must include a short summary, motivation, linked issue, and manual test plan.
- Changes to plugin API, signing behavior, supported MIME types, or example flows should include representative code snippets or migration notes when helpful.

## Security & Sensitive Information
- Do not commit private keys, certificates, tokens, or sensitive sample media.
- Public issues, PRs, branch names, screenshots, and descriptions must not mention corporate partners, customers, brands, campaign names, or other sensitive external identities unless a maintainer explicitly approves it. Use generic descriptors instead.
