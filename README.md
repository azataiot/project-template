# project-template

<a href="https://github.com/azataiot/project-template/generate"><img src="https://img.shields.io/badge/use%20this-template-blue?logo=github" alt="use-this-repo-badge"></a>
[![Code Quality](https://github.com/azataiot/project-template/actions/workflows/code-quality.yml/badge.svg)](https://github.com/azataiot/project-template/actions/workflows/code-quality.yml)
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
- [x] Makefile (try `make help`)

## Usage

### Create a new repository from this template



1. [Click here](https://github.com/azataiot/project-template/generated) to create a new repository with this template.
2. Select and Add a license.

### Initialize and install `pre-commit` hooks

1. Install [pre-commit](https://pre-commit.com/#install). (skip this step if you already have pre-commit installed)
2. Run `pre-commit install` to install the pre-commit hooks.
3. Run `make pre-commit` to run the pre-commit hooks on all files.

### Setup GitHub Branch Protection

1. Go to `Settings` > `Branches` > `Branch protection rules` > `Add rule`
2. Add the following rules:
   - `main`
     - Require a pull request before merging
     - Require status checks to pass before merging
     - Require branches to be up-to-date before merging
     - Add `linting` status checks ( and others if you created them )
     - Do not allow bypassing the above settings
   - `dev`
     - Require a pull request before merging
     - Require status checks to pass before merging
     - Add `linting` status checks ( and others if you created them )


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
