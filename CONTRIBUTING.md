# Contributing

- [Coding rules](#coding-rules)
  - [Source code](#source-code)
  - [Documentation](#documentation)
  - [Commit guidelines](#commit-guidelines)
  - [Commit message format](#commit-message-format)

# Coding rules

## Source code

In order to keep the source code consistent and high quality, all source code modifications must have:

- no linting errors;
- a test for every possible case introduced by the code change;
- no decrease in test coverage;
- documentation updated or added;
- [valid commit message(s)](#commit-message-guidelines).

## Documentation

To ensure consistency and quality, all documentation modification must:

- Refer to brands in [bold](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax#styling-text) with the corresponding capitalisation, e.g. **GitHub**, **npm**, **Node.js**.
- Use [links](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax#links) when you are referring to:
  - a product, brand or service, e.g. we use [GitHub](https://github.com/);
  - a concept or feature, e.g. create a [pull request](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request);
  - a package or module, e.g. the [`@commitlint/load`](https://github.com/conventional-changelog/commitlint/tree/master/%40commitlint/load) module.
- Use [single backtick `code` quoting](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/basic-writing-and-formatting-syntax#quoting-code) for:
  - programming language keywords, e.g. `function`, `async`, `string`;
  - commands inside sentences, e.g. the `git` command;
  - packages or modules, e.g. the [`@commitlint/load`](https://github.com/conventional-changelog/commitlint/tree/master/%40commitlint/load) module.
- Use [triple backtick `code` formatting](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/creating-and-highlighting-code-blocks), with corresponding language for [syntax highlighting](https://docs.github.com/en/free-pro-team@latest/github/writing-on-github/creating-and-highlighting-code-blocks#syntax-highlighting), for:
  - code examples;
  - sequences of commands.

## Commit guidelines

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
