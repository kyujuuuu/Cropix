# Contributing to Cropix

Thanks for helping improve Cropix. This project is a Flutter app for pechay
(Bok Choy) growers, and contributions to the app, documentation, and content
are welcome.

## Before you start

Please read the [README](README.md) first. It explains the project structure,
the current gaps, and how to reconstruct a runnable Flutter project because
`pubspec.yaml`, platform folders, and assets are not yet committed.

## Workflow

1. Fork the repository or create a branch from `main` if you have write access.
2. Use a descriptive branch name:
   - `feature/pest-filter`
   - `fix/weather-spray-warning`
   - `docs/setup-guide`
3. Keep pull requests focused on one change. Small, reviewable PRs are easier
   to test and merge.
4. Run checks before pushing:

   ```bash
   flutter analyze
   flutter test
   ```

   If the Flutter toolchain is not set up yet, say so in the pull request and
   describe what you could verify manually.

5. Open a pull request against `main` and complete the PR checklist.

## What to work on

The README's roadmap lists the main gaps. Good places to start:

- Restore the missing `pubspec.yaml`, platform folders, and `images/` assets.
- Add the whitefly screen and the Shanghai pechay variety guide.
- Finish the insect tracker and community feed.
- Add tests for models, Firebase services, and weather parsing.
- Improve accessibility, error handling, and loading states.

For larger changes, open an issue first so the approach can be discussed.

## Code guidelines

- Follow the existing folder structure under `lib/`.
- Keep widgets and services consistent with the surrounding code.
- Never commit API keys, signing files, or other secrets. The current weather
  key should be moved to `--dart-define`.
- Add or update documentation when behavior changes.
- Prefer clear names and small methods over deeply nested widgets.

## Reporting bugs

Include:

- What you expected to happen.
- What actually happened.
- Steps to reproduce the issue.
- Flutter version, platform, and relevant logs or screenshots.

## Commit messages

Use a short imperative subject and an optional body:

```text
fix: handle empty weather city

Avoid a null crash when geocoding returns no locality.
```

By contributing, you agree that your changes can be distributed under the
project's license. See the README for the current licensing status.
