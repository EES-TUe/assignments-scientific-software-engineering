# Assignment 3: documentation and error handeling

In this assignment we are adding documentation and error handeling 
for the `rms` function
which we have implemented in [Assignment 2](./assignment_2.md).

## Documentation

* Create a new branch.
* In file `pyproject.toml`, remove the `disable` line in the `[tool.pylint.main]` section, around Line 60.
* Create a pull request.
* Your build will fail because the `pylint` now complains that you do not have in-code documentation.
* Now add necessary documentation so the build passes. Review, approve, and merge pull request.

## Error handeling

We want to check the following conditions on the `input_array`. If a condition is not satisified, you should raise an error with a meaningful message.

* `input_array` should be an instance of `np.ndarray`.
* `input_array` should be one-dimentional.
* `input_array` should have the `dtype` of `np.float64`.
* The size of `input_array` should be at least `1`.
* `input_array` should not contain any `inf`.
* `input_array` should not contain any `nan`.

## Testing

In the error conditions, you should test all individual errors by creating a faulty input and check if the correct error is raised with the correct error message.

We create one PR for each error condition, including error handeling code and test. The team leader and team member should work on different sub-tasks, create different PR's and review each other's PR's.