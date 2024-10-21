# Assignment 1: GitHub and GIT

In this assignment you will learn basics of code collaboration using of GitHub and GIT.

## Changes in GitHub Webpage

For the team leader:

* Go to your repository in the webpage.
* Open the file `pyproject.toml`.
* Choose to edit the file.
* In the `project` section, change the author `Tony Xiang` and email adress to your own one.
  * **Note: DO NOT change the other author `Peter Salemink` yet.**
* Now commit the changes.
  * Type a meaningful commit message.
  * You cannot commit directly to `main`. So choose a branch name and click `Propose changes`.
* A pull request is now opened.

For the teammate:

* Go to repository and go to the pull request.
* Review and approve the PR.
* Merge the PR.
* Delete the temporary branch.


## Changes in Local PC

For both team members:

* Clone the repository in your local WSL folder.
* Go to the folder using `cd`, and open the folder using `vscode` by running `code .`.

For teammate:

* In `vscode`:
  * Open the file `pyproject.toml`
  * In the `project` section, change the author `Peter Salemink` and email adress to your own one.
  * Save the file.
  * Execute the following `git` actions using either command line, or the `vscode` version control tab.
    * Create a new branch.
    * Stage the changes of the files.
    * Commit the changes.
    * Push the new branch.
* In GitHub webpage
  * Go to pull request tab.
  * Create a new pull request.
    * Source branch is the one you created.
    * Target branch is `main`.

For team leader:

* Go to repository and go to the pull request.
* Review and approve the PR.
* Merge the PR.
* Delete the temporary branch.

For both team members:

* Execute the following `git` actions using either command line, or the `vscode` version control tab.
  * Pull/sync the latest changes in `main`.
  * Delete not needed local branches.
