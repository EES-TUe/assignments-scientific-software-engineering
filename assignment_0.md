# Assignment 0: create your repository

## Create repository

For the team leader:

* Go to [project template](https://github.com/EES-TUe/ees-scientific-software-engineering)
* Click `Use this template` and `Create a new repository`.
* In the `Owner` section, choose your own account.
* In the `Repository name` section, put `ees-scientific-software-engineering`.
* Put something meaningful in the `description`.
* Then create the repository

## Invite collaborator

The team leader should invite your teammate as [collaborator](https://docs.github.com/en/account-and-profile/setting-up-and-managing-your-personal-account-on-github/managing-access-to-your-personal-repositories/inviting-collaborators-to-a-personal-repository).

The other teammate should accept the invitation.

## Set branch protection

Follow the [ruleset instructions](https://docs.github.com/en/repositories/configuring-branches-and-merges-in-your-repository/managing-rulesets/creating-rulesets-for-a-repository#creating-a-branch-or-tag-ruleset) to create a **branch ruleset**.
Specifically, use the following options:

* Ruleset name: main protection
* Enforcement status: active
* Target branches: Add target -> include default branch
* Enable the following rules
  * Restrict creations
  * Restrict deletions
  * Require a pull request before merging
    * Required approvals: 1
    * Dismiss stale pull request approvals when new commits are pushed
    * Require conversation resolution before merging
  * Require status checks to pass
    * Require branches to be up to date before merging
    * Status checks that are required -> Add checks -> manually type `build-and-test` and select from the list
  * Block force pushes
