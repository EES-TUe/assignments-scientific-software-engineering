# Assignment 2: root mean square

In this assignment we are going to implement a simple function to calculate
the root mean square(RMS) of an array.

Mathemtically, given an array $[x_i],0 \le i < N$, the RMS value of the array is calculated as shown below:

$$
\sqrt{\frac{1}{N} \sum_{i=0}^{N-1}x_i^2}
$$

## Function signature

We are implementing a function (in a new Python file/module) with the signature as below:

```python
import numpy as np


def rms(input_array: np.ndarray) -> float:
    pass
```

## Implementation

You should think about how to implement this function efficiently using `numpy` vectorization technique. In principle, you should not use any `for` loop in this function.

## Testing

You should test the function happy flow and all error conditions.

* In the happy flow, you should test it in two ways.
  * You create the input array and expected result manually in the test script self.
  * You create the input array and expected result in a `json` file. Your test script reads the `json` file and test them.

## Pull requests

You should make pull request as small as possible. Specifically, make one individual PR per task as the following:

* Implement the calculation and test with manually created input.
* Add more test with `json` file.
