# Contributing <!-- omit in toc -->

First of all, thanks for contributing and making the project better!

As a contributor, we would like you to follow the following guidelines.

- [Using the issue tracker](#using-the-issue-tracker)
  - [Bug report](#bug-report)
  - [Feature proposal](#feature-proposal)
  - [Question](#question)
- [Coding guidelines](#coding-guidelines)
  - [Coding style](#coding-style)
  - [Coding rules](#coding-rules)
  - [Documentation rules](#documentation-rules)
- [Commit guidelines](#commit-guidelines)
  - [Commit message format](#commit-message-format)
- [Versioning](#versioning)

# Using the issue tracker

The issue tracker is the channel for bug reports, features proposals and questions. Before opening an issue or a pull request, please use the [GitHub issue and pull requests search](https://docs.github.com/en/free-pro-team@latest/github/searching-for-information-on-github/searching-issues-and-pull-requests) to make sure the bug, feature or pull request hasn't already been reported or implemented.

## Bug report

A good bug report shouldn't leave others needing to chase you for more information. Please try to be as detailed as possible in your report and fill the information requested in the Bug report template.

## Feature proposal

Feature proposals are welcome, but take a moment to find out whether your idea fits in with the scope and aims of the project. It's up to you to make a strong case to convince the project's developers of the merits of this feature. Please provide as much detail and context as possible and fill the information requested in the Feature proposal template.

## Question

Any questions regarding this project are welcome. Please fill the information requested in the Question template.

# Coding guidelines

## Coding style

The coding style should be enforced through tools as much as possible. Please make sure to use editor extensions, e.g. on the VS Code marketplace, to visualise code linting on the fly. You can of course always manually run the linter with `npm run lint`.

- For TypeScript code, documentation, YAML, etc. we conform to the [XO code style](https://github.com/xojs/xo), based off of [ESLint](https://eslint.org/).
- For C/C++ code we conform to the [Clang tidy](https://clang.llvm.org/extra/clang-tidy/) code style, with [Clang format](https://clang.llvm.org/docs/ClangFormat.html) for formatting the source code.

## Coding rules

In order to keep the source code consistent and high quality, all source code should:

- be easy to read and understand, ideally without requiring comments
  - use functions to simplify and structure complex code
  - simplify and/or remove code to make it more readable
  - source code should not require any documentation, if it does it is probably not simplified enough
- use verbose variable names (e.g. `referenceVoltage` instead of `vRef`)
- follow the [Return early pattern](https://medium.com/swlh/return-early-pattern-3d18a41bba8)
- have no linting errors
- have a test for every possible case introduced by the code change
- result in none, or negliable, decrease in test coverage
- have its public API documentation updated, if necessary

## Documentation rules

In order to keep the documentation consistent and high quality, all documentation should:

- refer to brands in [bold](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax#styling-text) with the corresponding capitalisation, e.g. **GitHub**, **npm**, **Node.js**
- use [links](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax#links) when you are referring to:
  - a product, brand or service, e.g. we use [GitHub](https://github.com/)
  - a concept or feature, e.g. create a [pull request](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request)
  - a package or module, e.g. the [`@commitlint/load`](https://github.com/conventional-changelog/commitlint/tree/master/%40commitlint/load) module
- use [single backtick `code` quoting](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax#quoting-code) for:
  - programming language keywords, e.g. `function`, `async`, `string`
  - commands inside sentences, e.g. the `git` command
  - packages or modules, e.g. the [`@commitlint/load`](https://github.com/conventional-changelog/commitlint/tree/master/%40commitlint/load) module
- use [triple backtick `code` formatting](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/creating-and-highlighting-code-blocks), with corresponding language for [syntax highlighting](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/creating-and-highlighting-code-blocks#syntax-highlighting), for:
  - code examples
    ```ts
    function square(value: number): number {
      return value ** 2;
    }
    ```
  - sequences of commands
    ```shell
    $ mkdir test
    $ cd test
    ```

# Commit guidelines

Please use atomic commits as much as possible. An atomic commit is a commit that follows the following rules.

- Contain exactly one self-contained change.
- Does not create an inconsistent state, such as build failure, test failures, linting errors, etc.

> In short, all your tests need to be green on every commit and your application shouldn’t break. Every commit has a clear commit message and a description detailing what the purpose of these changes was. Lastly, the commit should only have changes pertaining to one fix or feature (or whatever you were working on). Don’t have commits where you “fixed that bug and also implemented the feature and then also refactored some class”.
>
> [Atomic commits will help you git legit](https://www.pauline-vos.nl/atomic-commits/)

## Commit message format

We use the [`Conventional Commits 1.0.0`](https://www.conventionalcommits.org/en/v1.0.0/) specification for our commit messages. The commit message format is checked pre-commit using [`commitlint`](https://commitlint.js.org/#/). The rules for the commit messages are specified in the [`@vidavidorra/commitlint-config`](https://github.com/vidavidorra/commitlint-config) [rules](https://github.com/vidavidorra/commitlint-config/blob/master/docs/rules.md), which modifies [`@commitlint/config-conventional`](https://github.com/conventional-changelog/commitlint/tree/master/@commitlint/config-conventional) rules.

In short, commit messages should be structured as follows:

```
<type>[optional scope]: <description>

[optional body]

[optional footer(s)]
```

Where type must be one of the following types.

| Type     | Description (used to ...)                                       |
| -------- | --------------------------------------------------------------- |
| build    | Change that affects the build system.                           |
| ci       | Change or add CI configuration fies and scripts.                |
| chore    | Change something witout impacting the user (e.g. bump version). |
| docs     | Change or add documentation.                                    |
| feat     | Add a new feature.                                              |
| fix      | Fix a bug.                                                      |
| perf     | Improve code performance.                                       |
| refactor | Refactor code without changing the public API.                  |
| revert   | Revert a previous commit, referencing the reverted commit SHA.  |
| style    | Change code style (formatting, missing semicolons, etc.).       |
| test     | Add missing tests or modifying existing tests.                  |

The body and/or footer can be used to reference issues and pull requests or close issues using the keywords listed below, originating from the GitHub documentation [Using keywords in issues and pull requests](https://docs.github.com/en/get-started/writing-on-github/working-with-advanced-formatting/using-keywords-in-issues-and-pull-requests).

- `closes`: closes the linked issue, for example, `Closes #10`, `Closes vidavidorra/commitlint-config#10` or `Closes #10, closes #11`. Note that closing multiple issues requires the full syntax for each issue.
- `refs`: reference an issue or pull request, for example `Refs #10`, `Refs withthegrid/support#10` or `Refs #10, refs #11`.

### Examples <!-- omit in toc -->

Simple commit message without scope.

```
docs: add contributing guidelines
```

Commit message with scope and closing an issue.

```
feat(Renovate): group linters

Closes #123.
```

Commit message with scope and breaking change.

```
feat(node-test)!: rename `node-version` input to `nodeVersion`, defaulting to 18

Make the `node-test` inputs consistent with all other workflows.

Closes #123, refs #111.
```

# Versioning

We follow the [Semantic Versioning 2.0.0](https://semver.org/spec/v2.0.0.html) standard and have automated releases using [`semantic-release`](https://github.com/semantic-release/semantic-release). This uses the commit messages to determine what type of release to create, so it is very important to follow the [Commit message format](#commit-message-format). Regular releases are based on the `main` branch, where pre-releases are based on the `beta` branch.

> **Note** For hardware, anything except documentation and drop-in part number changes is a breaking change as it results in different PCB fabrication files, for example Gerbers.
