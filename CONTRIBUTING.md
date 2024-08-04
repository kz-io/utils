# Contributing

Thank you for your interest in contributing to the kz libraries. There
are multiple ways to contribute, including reporting or resolving issues,
requesting or adding new features, improving documentation, creating guides,
adding translations, and more.

## Found an issue?

If you find an issue in a kz library source code, you can help by
[submitting an issue][issues] to its GitHub Repository. If you have a fix for
the issue, you can submit a [Pull Request][pulls].

## Want a feature?

You can request a new feature in a library by [submitting an issue][feature] to
a kz library's GitHub Repository. If you are unsure which library a
feature should be requested in, you can [submit an issue][feature-new] on the
`kz-io/please` repo.

## What you need to know

If you are interested in contributing with code, you only need to be familiar
with [TypeScript][typescript] and [Deno][deno].

You can contribute to documentation by looking at
[documentation issues][documentation].


### Code reviews

Things we look for when reviewing a pull request into the `dev` branch:

* Dependencies and imports
* Supporting features
* DRY practices
* Performance
* Error/exception handling
* Test coverage

Outside of the Deno standard library, kz depends on no 3rd party codebases. This forces accountability
on integereleven and other kz contributors in regard to the performance and security of the libraries.

If you develop supporting features that are more
generic in nature, you may be asked to contribute the supporting features to an appropriate repo for
publishing, and then including the newly release package containing the supporting features and using them.

You may also be asked to revise your pull request in these cases:

* You've re-used a functionality or technique in multiple places, when it may be better suited as a supporting feature.
* The performance of a feature can be improved using other techniques.
* A feature may have an unhandled error or exception that may be gracefully handled.
* The testing of the feature is not sufficient.

# Making code contributions

New to contributing to open source projects?

Find an issue of interest, or a feature that you'd like to implement. You can
use [the "good first issue" view][first-issue] to help ease into the project.

## 1. Fork it

Fork the repository to your GitHub organization. This means that you'll have a
copy of the repository under _**username/repo-name**_.

## 2. Clone it

```bash
git clone https://github.com/{username}/repo-name.git
```

## 3. Branch it

Create a new branch for your fix or feature.

```bash
git checkout -b branch-name-here
```

## 4. Setup dev environment

A supported version of [Deno][deno] must be installed. View the [Requirements][reqs] in the [README.md][readme].

## 5. Do it

Update the code with your issue fix or new feature implementation.

Ensure there are tests with adequate coverage.

### Helpful tasks

The repo provides several tasks to assist with development.

Simply run `deno task <task>`, where `<task>` is one of the following (e.g. `deno task fmt`):

* `fmt` - Formats source code and confirms. If format checks fail, the branch will not merge.
* `lint` - Lints source code and examples in documentation and the `README.md`. If linting fails, the branch will not merge.
* `test` - Runs tests, lints documentation examples, traces memory leaks, and if compatible, runs coverage. If tests fail, the branch will not merge.
* `cov` - Runs the `test` task, generating coverage and a coverage report. Coverage will not be commited. This is simply for coverage review.
* `docs` - Build HTML documentation. Documentation will not be commited. This is simply for reviewing documentation before potential publishing.
* `jsr:check` - Performs a dry-run testing the readiness of the package to be published to JSR.
* `pre-commit` - Runs the `cov`, `docs`, `jsr:check`, `lint`, and `fmt` tasks. Used to prepare the branch for a successful merge.

## 6. Stage it

Run the [Deno][deno] pre-commit task (`deno task pre-commit`).

Stage the changes to be committed:

```bash
git add .
```

## 7. Commit it

Commit the changes with a brief message. (See
[commit messages](#commit-messages) on how to structure commit messages)

```bash
git commit -m "<type>: <description>"
```

## 8. Push it

Push the changes.

```bash
git push origin branch-name-here
```

## 9. Create a pull request

1. [Create a pull request][pulls] into the `dev` branch.
   - Title the pull request and provide a brief summary of the changes made.
   - Reference the issue the change is associated with.
   - Explain the changes made, and any potential issues that may arise with the
     pull request.
2. Wait for the pull request to be reviewed.
3. Make any changes recommended to the pull request.

# Commit messages

We follow the [Conventional Commits][conventional-commit] commit message
convention.

Commit messages should be structured like this:

```bash
<type>: <description>
```

Example

```
fix: fix IPv4 CIDR-to-mask resolution on /32 masks.
```

## Types:

- **chore**: Changes to the build process or auxiliary tools and libraries such
  as documentation generation
- **docs**: Documentation only changes
- **feat**: A new feature
- **fix**: A bug fix
- **perf**: A code change that improves performance
- **refactor**: A code change that neither fixes a bug nor adds a feature
- **style**: Changes that do not affect the meaning of the code (white-space,
  formatting, missing semi-colons, etc...)
- **test**: Adding missing or correcting existing tests

# Code of conduct

Please note that this project is released with a Contributor Code of Conduct. By
participating in this project you agree to abide by its terms.

[Code of Conduct][code-of-conduct]

Our Code of Conduct means that you are responsible for treating everyone on the
project with respect and courtesy.

<!-- tech -->
[typescript]: https://www.typescriptlang.org/docs "TypeScript: The JavaScript superset for the future"
[deno]: https://deno.com "Deno: The next-generation JavaScript runtime"

<!-- issues -->
[issues]: https://github.com/kz-io/mod-name/issues/new?template=issue.yaml&title= "Report an issue in kz/mod-name"
[feature]: https://github.com/kz-io/mod-name/issues/new?template=feature.md&title= "Request a new feature in kz/mod-name"
[feature-new]: https://github.com/kz-io/please/issues/new?template=feature.yaml&title= "Request a new feature in kz"
[first-issue]: https://github.com/kz-io/mod-name/issues?q=is%3Aopen+is%3Aissue+label%3A%22good+first+issue%22 "Good first issues in kz/mod-name"
[documentation]: https://github.com/kz-io/mod-name/labels/type%3A%20docs "Documentation issues in kz/mod-name"

<!-- prs -->
[pulls]: https://github.com/kz-io/mod-name/compare "Create a pull request on @kz/mod-name"

<!-- dev -->
[code-of-conduct]: https://github.com/kz-io/.github/blob/main/.github/CODE_OF_CONDUCT.md "Contributor Code of Conduct"
[conventional-commit]: https://www.conventionalcommits.org/en/v1.0.0/ "Conventional Commits: A guide to commit messages"

<!-- repo-->
[readme]: https://github.com/kz-io/mod-name/blob/main/README.md "@kz/mod-name readme"
[reqs]: https://github.com/kz-io/mod-name/blob/main/README.md#requirements "@kz/mod-name requirements"