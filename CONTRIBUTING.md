<div align="center">
  <h1
    style="font-size: 3rem; font-weight: bold;"
    >
    Contributing To Projects
  </h1>
</div>

Thank you for considering contributing to [Project Name]! Your help is valuable, and we appreciate your effort to make this project better.

Please read through this guide to ensure that your contribution is consistent with our coding standards and process.

## Table of Contents

1. [Code Style Guidelines](#code-style-guidelines)
2. [How to Contribute](#how-to-contribute)
3. [Shell Script Guidelines](#shell-script-guidelines)


    Pull Request Process

    Reporting Bugs

    Suggesting Enhancements

    Code of Conduct

## Code Style Guidelines

- Indentation: Use 4 spaces for indentation. Do not use tab characters (\t).
- Line Length: Code strings (lines) must not exceed 110 characters.
- Naming Conventions:
  - Use `snake_case` for function names.
  - Use `UPPER_SNAKE_CASE` for constants.
  - Use `PascalCase` for class names.
- Comments:
  - Write clear and concise comments that is brief and to the point.
  - Use English for all comments and documentation.
- Consistency: Follow the style of the existing code.

If you are unsure about any style rules, refer to existing files as examples or ask in an issue.

## How to Contribute

1. Fork the repository.
2. Clone your fork to your local machine:

    ```bash
    git clone https://github.com/your-username/[project-name].git
    cd [project-name]
    ```

3. Create a new branch for your feature or bugfix:

    ```bash
    git checkout -b feature/my-new-feature
    ```

4. Make your changes following the [Code Style Guidelines](#code-style-guidelines).

5. Commit your changes with a clear commit message:

    ```bash
    git commit -m "feat: add new feature [short description]"
    ```

6. Push to your fork:

    ```bash
    git push origin feature/my-new-feature
    ```

7. Open a Pull Request (PR) on the main repository.

## Shell Script Guidelines

If you are contributing Bash or shell scripts to this project, please also follow these rules:

- Shebang: Always use `#!/bin/env bash` at the top, not `/bin/sh`.
- Use `set -eo pipefail` at the start of scripts for safer execution:

    ```bash
    set -euo pipefail
    ```

- Quoting:
  - Always quote and contain with '{}' expressions: `${var}`instead of `$var`.
  - Use "$@" instead of $@ and "$*" unless specifically needed.

- Command Substitution: Use $(...) instead of backticks `...`.

- Functions:

    Define functions using the function keyword:

    ```bash
    function my_function() {
        # code
    }
    ```

- Indentation:
  - Use 4 spaces per level (never tabs).

- Line Length: Shell code lines must also not exceed 110 characters.

- Error Handling:
  - Use checks for commands that might fail and if possible use `trap` to handle errors gracefully:

    ```bash

    command -v foo &>/dev/null || { echo "foo is required but not installed" >&2; exit 1; }

    trap error_handler ERR
    ```

- Temporary Files:
  - Use mktemp for temporary files and clean them up properly.

- Portability:
  - Prefer POSIX-compliant syntax unless using Bash-specific features is necessary.

## Pull Request Process

- Ensure your changes pass all existing tests and do not break the build.
- Link any related issues in the PR description (e.g., Closes #42).
- Keep PRs focused and small. Larger changes should be split into smaller PRs when possible.
- PRs will be reviewed by maintainers. You may be asked to make changes before they are merged.

## Reporting Bugs

If you encounter a bug:

- Open an issue with the title prefixed by BUG: (e.g., BUG: crashes when loading config).
- Include clear steps to reproduce the bug.
- Add details about your environment (OS, version, etc.).
- Screenshots or error logs are very helpful.

## Suggesting Enhancements

- Open an issue prefixed by BUG: (e.g., BUG: crashes on startup).
- Include steps to reproduce the bug.
- Add environment details (OS, version, etc.).
- Attach logs or screenshots if possible.

## Code of Conduct

Please read our [CODE OF CONDUCT](CODE_OF_CONDUCT.md) before contributing. Be respectful and inclusive in all interactions.
Thank You!

We are grateful for your contributions! ❤️
