# Contributing to Hiero

First off, thanks for taking the time to contribute! ❤️

All types of contributions are encouraged and valued.
Please make sure to read the relevant section before making your contribution.
It will make it a lot easier for us maintainers and smooth out the experience for all involved.
The community looks forward to your contributions. 🎉

> And if you like the project, but just don't have time to contribute, that's fine.
> There are other easy ways to support the project and show your appreciation, which we would also be very happy about:
> - Star the project
> - Tweet about it
> - Refer this project in your project's readme
> - Mention the project at local meetups and tell your friends/colleagues

## Code of Conduct

This project and everyone participating in it is governed by the
[Linux Foundation Decentralized Trust Code of Conduct](https://www.lfdecentralizedtrust.org/code-of-conduct).
By participating, you are expected to uphold this code.
Please report unacceptable behavior to Mike Dolan (mdolan@linuxfoundation.org) or Angela Brown (angela@linuxfoundation.org).

## Pull Requests
Like most open source projects, we use
[pull requests](https://docs.github.com/en/github/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests) (
PRs) to track code changes.

### Forking

1. [Fork](https://guides.github.com/activities/forking/) the repository. Go to the project page then hit the `Fork`
   button to fork your own copy of the repository to your GitHub account.

2. Clone the forked repository to your local working directory.

```sh
$ git clone https://github.com/${owner}/${repo}.git
```

3. Add an `upstream` remote to keep your fork in sync with the main repo.

```sh
$ git remote add upstream https://github.com/hiero-ledger/${repo}.git
```

4. Sync your local `main` branch.

```sh
$ git pull upstream main
```

5. Create a branch to add a new feature or fix issues.

```sh
$ git checkout -b new-feature
```

6. Make any change on the branch `new-feature` then build and test your code locally.

7. Add files that you want to be committed.

```sh
$ git add <file>
```

We do not have a hard definition for commit messages but it is best practice to use the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification.

8. Enable [GPG signing](https://docs.github.com/en/github/authenticating-to-github/managing-commit-signature-verification/signing-commits) of your commits within the repo.
   Signing all your commits with your public key allows the comunity to verify it's really you. If you forgot to sign some
   commits that are part of the contribution, you can
   ask [git to rewrite your commit history](https://git-scm.com/book/en/v2/Git-Tools-Rewriting-History).

```sh
$ git config commit.gpgsign true
```

9. Use [sign-off](#sign-off) when making each of your commits. Additionally,
   [GPG sign](https://docs.github.com/en/github/authenticating-to-github/managing-commit-signature-verification/signing-commits) of
   all your commits is a must.

```sh
$ git commit --signoff -S -m "Your commit message"
```

10. [Submit](#pr-lifecycle) a pull request.

### Sign Off

The sign-off is a simple line at the end of a commit message. All commits needs to be signed. Your signature certifies
that you wrote the code or otherwise have the right to contribute the material. First, read the
[Developer Certificate of Origin](https://developercertificate.org/) (DCO) to fully understand its terms.

Contributors sign-off that they adhere to these requirements by adding a `Signed-off-by` line to commit messages (as
seen via `git log`):

```
Author: Joe Smith <joe.smith@example.com>
Date:   Thu Feb 2 11:41:15 2018 -0800

    Update README

    Signed-off-by: Joe Smith <joe.smith@example.com>
```

Use your real name and email (sorry, no pseudonyms or anonymous contributions). Notice the `Author` and `Signed-off-by`
lines match. If they don't your PR will be rejected by the automated DCO check.

If you set your `user.name` and `user.email` git configs, you can sign your commit automatically with `-s`
or `--sign-off` command line option:

```sh
$ git config --global user.name "Joe Smith"
$ git config --global user.email "joe.smith@example.com"
$ git commit -s -S -m 'Update README'
```

### PR Lifecycle

Now that you've got your [forked](#forking) branch, you can proceed to submit it.

#### Submitting

- It is preferred, but not required, to have a PR tied to a specific issue. There can be circumstances where if it is a
  quick fix then an issue might be overkill. The details provided in the PR description would suffice in this case.
- The PR description or commit message should contain
  a [keyword](https://help.github.com/en/articles/closing-issues-using-keywords)
  to automatically close the related issue.
- Commits should be as small as possible, while ensuring that each commit is correct independently
  (i.e., each commit should compile and pass tests).
- Add tests and documentation relevant to the fixed bug or new feature. Code coverage should stay the same or increase
  for the PR to be approved.
- We more than welcome PRs that are currently in progress. If a PR is a work in progress, it should be opened as
  a [Draft PR](https://help.github.com/en/articles/about-pull-requests#draft-pull-requests). Once the PR is ready for
  review, mark it as ready to convert it to a regular PR.
- After submitting, ensure all GitHub checks pass before requesting a review. Also double-check all static analysis and
  coverage tools show a sufficient coverage and quality level.
- When creating a pull request the name of the PR must follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification.
- Several GitHub Actions will be triggered automatically for each PR.
  If a GitHub Action fails and you do not understand the cause of that error do not hesitate to add a comment to the PR and ask the Hiero developer community for support.

#### Triage

- The maintainer in charge of triaging will apply the proper labels for the PR.
- The maintainer can assign a reviewer, or a reviewer can assign themselves.

#### Reviewing

- All reviews will be completed using the GitHub review tool.
- A "Comment" review should be used when there are questions about the code that should be answered, but that don't
  involve code changes. This type of review does not count as approval.
- A "Changes Requested" review indicates that changes to the code need to be made before they will be merged.
- For documentation, special attention will be paid to spelling, grammar, and clarity
  (whereas those things don't matter *as* much for comments in code).
- Reviews are also welcome from others in the community. In the code review, a message can be added, as well as `LGTM`
  if the PR is good to merge. It’s also possible to add comments to specific lines in a file, for giving context to the
  comment.
- PR owner should try to be responsive to comments by answering questions or changing code. If the owner is unsure of
  any comment, please ask for clarification in the PR comments.
- Once all comments have been addressed and all reviewers have approved, the PR is ready to be merged.

#### Merge or Close

- PRs should stay open until they are merged or closed. The issue may be closed if the submitter has not been responsive
  for more than 30 days. This will help keep the PR queue to a manageable size and reduce noise.

## I Have a Question

Before you ask a question, it is best to search for existing Issues that might help you.
In case you have found a suitable issue and still need clarification, you can write your question in this issue.
It is also advisable to search the internet for answers first.

If you then still feel the need to ask a question and need clarification, we recommend the following:

- Open an Issue.
- Provide as much context as you can about what you're running into.

We will then take care of the issue as soon as possible.

## Reporting Bugs Or Suggesting Enhancements

If you found a bug in our code or want to suggest a new feature or improvement please create a new Issue.

## Your First Code Contribution

We reserve issues for people who have never contributed to this project or any open source project in general.
We know that creating a pull request (PR) is a major barrier for new contributors.
The goal of issues labeled by **'good first issue'** is to help you make your first contribution.
You can read about or workflows for **'good first issue'** handling [here](https://github.com/hiero-ledger/governance/blob/main/guidelines/good-first-issues.md).

This does not mean that contribution is only welcome for those issues.
We are happy with any contribution.
The most important point is that an issue exists for the contribution.
If that is not the case please create an issue for a bug or enhancement.
Please comment on the given issue that you want to work on it.
Once a member of the team has assigned you to the issue you can start working on it.

## Attribution
This guide is based on the **contributing-gen**. [Make your own](https://github.com/bttger/contributing-gen)!
