# Assignment 4: matrix factorization and linear equation

In this assignment we want to solve the linear equation:

$$
\mathbf{A}\boldsymbol{x} = \boldsymbol{b}
$$

where $\mathbf{A}$ is a $N \times N$ matrix, $\boldsymbol{x}$ and $\boldsymbol{b}$ are $N \times 1$ vectors.

With the same matrix $\mathbf{A}$, we want to solve multiple different $\boldsymbol{x}$ with different $\boldsymbol{b}$. To do that, we firstly do a LU-factorization:

$$
\mathbf{A} = \mathbf{P} \mathbf{L} \mathbf{U}
$$

where $\mathbf{P}$ is the row-permutation matrix, $\mathbf{L}$ lower triangular matrix and $\mathbf{U}$ is the upper triangular matrix.

Once we have the factorization of $\mathbf{A}$, we can use the factorization to solve multiple equations of $\boldsymbol{x}$ and $\boldsymbol{b}$.

In this assignment, we use the object-oriented programming pattern. Given the input matrix in the constructor, we decompose it and store the factorization and permutation into class members. The class can have a method `solve` to solve different equations of $\boldsymbol{x}$ and $\boldsymbol{b}$.

## Class skeleton

We use the following class skeleton to implement:

```python
import numpy as np


class LUSolver:
    def __init__(self, input_matrix: np.ndarray):
        """
        Constructor of the class. It takes the input matrix and decompose it into LU factorization.
        Store the factorization and permutation into class members.
        """
        pass

    def solve(self, b: np.ndarray) -> np.ndarray:
        """
        Solve the linear equation with the input matrix and the given vector b.
        """
        pass
```

## Implementation

To implement the class, you need two `scipy` functions: 
[`scipy.linalg.lu_factor`](https://docs.scipy.org/doc/scipy/reference/generated/scipy.linalg.lu_factor.html)
and
[`scipy.linalg.lu_solve`](https://docs.scipy.org/doc/scipy/reference/generated/scipy.linalg.lu_solve.html).
Have a look at their documentations about how to use them.

## Error checking

You should check the following conditions in the constructor. If a condition is not satisfied, you should raise an error with a meaningful message.

* `input_matrix` should be an instance of `np.ndarray`.
* `input_matrix` should be a square matrix.
* `input_matrix` should have the `dtype` of `np.float64`.
* The size of `input_matrix` should be at least `1`.
* `input_matrix` should not contain any `inf`.
* `input_matrix` should not contain any `nan`.
* `input_matrix` should not be singular.

You should check the following conditions in the `solve` method. If a condition is not satisfied, you should raise an error with a meaningful message.

* `b` should be an instance of `np.ndarray`.
* `b` should be a one-dimensional vector.
* `b` should have the `dtype` of `np.float64`.
* The size of `b` should be the same as the size of the input matrix.
* `b` should not contain any `inf`.
* `b` should not contain any `nan`.

## Testing

Same as [Assignment 2](./assignment_2.md), you should test the class with happy flow and all error conditions. In the happy flow, try to test with manually created input in the test script, and pre-defined input in a `json` file.