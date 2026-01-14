# Contributing to Circle

First off, thanks for taking the time to contribute!

The following is a set of guidelines for contributing to Circle and its packages. These are mostly guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

## Table of Contents
1.  [Code of Conduct](#code-of-conduct)
2.  [Getting Started](#getting-started)
3.  [How to Contribute](#how-to-contribute)
4.  [Style Guides](#style-guides)

## Code of Conduct
This project and everyone participating in it is governed by the [Circle Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code.

## Getting Started

### Prerequisites
*   Node.js (LTS version recommended)
*   npm or yarn
*   Git

### Development Setup
1.  Clone the repo: `git clone https://github.com/MDF05/circle.git`
2.  Navigate to the folder: `cd circle`
3.  Install dependencies for both backend and frontend.

## How to Contribute

### Reporting Bugs
This section guides you through submitting a bug report.
*   **Use the Issues tab**: Check if the bug is already reported.
*   **Clear Title and Description**: Explain what happened and what you expected to happen.
*   **Reproduction Steps**: Provide step-by-step instructions to reproduce the bug.

### Suggesting Enhancements
*   **Feature Request**: specific improvements or new features.
*   **Explain**: Why you want this feature and how it benefits the project.

### Pull Requests
1.  Fork the repo and create your branch from `main`.
2.  If you've added code that should be tested, add tests.
3.  Ensure the test suite passes.
4.  Make sure your code lints.
5.  Update documentation if relevant.

## Style Guides

### Git Commit Messages
*   Use the present tense ("Add feature" not "Added feature").
*   Use the imperative mood ("Move cursor to..." not "Moves cursor to...").
*   Limit the first line to 72 characters or less.
*   Reference issues and pull requests liberally after the first line.

### JavaScript/TypeScript Style
*   We use **ESLint** and **Prettier** to enforce code style.
*   Run `npm run lint` before committing.
*   Prefer functional components for React.
*   Use `const` over `let`.

### Documentation Style
*   Use Markdown.
*   Keep it concise and clear.
