# project-template

A project template to use for new GitHub repositories

## Features

- [x] LICENSE
- [x] SECURITY
- [x] CODE OF CONDUCT
- [x] CONTRIBUTING
- [x] ISSUE TEMPLATE
- [x] PULL REQUEST TEMPLATE
- [x] README GUIDE
- [x] dependabot.yml
- [x] FOUNDING

## Usage

<a href="https://github.com/azataiot/project-template/generate"><img src="https://img.shields.io/badge/use%20this-template-blue?logo=github" alt="use-this-repo-badge"></a>

1. [Use this template](https://github.com/azataiot/project-template/generated) to create a new repository.
2. Select and Add a license.

## Branching Strategy

- `main`: The main branch. This branch is protected and cannot be pushed directly. (PRs must be made to `dev` instead
  of `main`)
- `dev`: The development branch. This branch is protected and cannot be pushed directly. (PRs must be made to this
  branch)
- `feature/*`: The 'feature/*' branches are used to develop new features for the upcoming or a distant future release.
  These branches are branched off from 'dev' and must merge back into `dev`.
- `release/*`: The 'release/*' branches are used to prepare the next release. They allow for last-minute changes and
  minor bug fixes. These branches are branched off from 'dev' and must merge back into `main` and `dev`.
- `hotfix/*`: The 'hotfix/*' branches are used to develop fixes for the current release. These branches are branched off
  from `main` and must merge back into `main`.