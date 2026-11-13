# Repository Guidelines

## Project Structure & Module Organization

This repository is currently empty. As code is added, group related source files by feature or component, keep tests close to the code they cover or in a clearly named `tests/` directory, and place reusable assets in `assets/`. Document any new top-level directories here.

## Build, Test, and Development Commands

No build system, development server, or test runner is configured yet. When introducing one, document the prerequisites and exact commands in this section and in the project README. Prefer commands that work from the repository root and make setup reproducible.

## Coding Style & Naming Conventions

Follow the conventions of the language and surrounding code. Use consistent indentation within each file, descriptive names, and lowercase, hyphenated names for general documentation files where practical. Add formatter or linter configuration alongside the first implementation, and document how to run it. Avoid committing generated files unless they are needed by the project.

## Testing Guidelines

No testing framework or coverage target is currently defined. Add automated tests for new behavior and regression fixes when a test framework is introduced. Name tests to identify the component and behavior being checked, and document the command for running the full suite. Report any checks that could not be run in the pull request.

## Commit & Pull Request Guidelines

There is no Git history available from which to infer a commit convention. Write short, imperative commit subjects that describe the change, such as `Add firmware parsing utility`. Keep commits focused. Pull requests should explain the purpose and behavior of the change, link relevant issues, and describe verification performed. Include screenshots when a change affects a visual interface.

## Security & Configuration

Keep credentials, private keys, and machine-specific configuration out of the repository. Provide sanitized examples for required settings and document how contributors should supply them locally.