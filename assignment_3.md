# Assignment 3: documentation

In this assignment we are adding documentations for the `rms` function
which we have implemented in [Assignment 2](./assignment_2.md).

Concretely, we do the following:

* Create a new branch.
* In file `pyproject.toml`, remove the `disable` line in the `[tool.pylint.main]` section, around Line 60.
* Create a pull request.
* Your build will fail because the `pylint` now complains that you do not have in-code documentation.
* Now add necessary documentation so the build passes. Review, approve, and merge pull request.
