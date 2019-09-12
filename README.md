## Parallel-Sum-Reduction-in-OpenCL
OpenCL implemention of the Parallel Sum Reduction operator that computes the sum of a large array of values.

In this assignment one has to develop an efficient implemention of the Parallel Sum Reduction operator that computes the sum of a large array of values in OpenCL. A prime criterion in the assignment will be the efficiency of both the implementations and the evidence presented to substantiate claims that implementations are efficient.

## Implementation
In this algorithm, the program is implemented such that rather than a simple linear summation of array values, the summation is done as in the below algorithm:

Step 1: A “slider” value is calculated as (veryLongArraySize/2). Step 2: An array value at (i)th location is added with an array value of (i+slider)th location and stored back to (i)th location. Now half the array values are processed stored. So now this half should be processed again. Step 3: Reduce array size, veryLongArraySize, by 2 and continue with step 1. If array size is 1 go to step 4. Step 4: Value at veryLongArray[0] gives the sum of the very large array values.

### For a detailed results and conclusion, please refer the report in the repo

### Reference
https://dournac.org/info/gpu_sum_reduction
