# LeetCode 239 - Sliding Window Maximum

## Problem

You are given an integer array `nums` and an integer `k`.

There is a sliding window of size `k` that moves from the beginning to the end of the array.

Return the maximum value in each window.

## Example

### Input

```text
nums = [1,3,-1,-3,5,3,6,7]
k = 3
```

### Output

```text
[3,3,5,5,6,7]
```

## Approach

Use a deque to store the indices of useful elements.

The deque is maintained so that:

* The indices are within the current window.
* Values are stored in decreasing order.
* The first index always contains the maximum value of the current window.

When a new element is added, smaller elements at the back are removed because they cannot become the maximum while the new element is present.

## Algorithm

1. Create an empty deque and result list.
2. Remove indices that are outside the current window.
3. Remove smaller elements from the back of the deque.
4. Add the current index.
5. Once the first window is complete, add its maximum to the result.
6. Continue until all windows are processed.
7. Return the result.

## Complexity

* Time Complexity: `O(n)`
* Space Complexity: `O(k)`

Where `n` is the number of elements in the array.

## Language

Python

## LeetCode

Problem: 239 - Sliding Window Maximum

## Author

**T.Nandhini**
