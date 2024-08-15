# Problem Statement

### Given an integer array `nums` of size `n`, return the number with the value closest to 0 in `nums`. If there are multiple answers, return the number with the largest value.

## Example 1

**Input:**

```python
nums = [-4, -2, 1, 4, 8]

```
**Output**

```python
1
```
**Solution**
```python
def closest_to_zero(nums):
    if not nums:
        return None  # Handle case of empty list if necessary
    
    # Initialize with the first element
    closest_num = nums[0]
    
    for curr_num in nums:
        # Check if the current number is closer to zero
        if abs(curr_num) < abs(closest_num):
            closest_num = curr_num
        # If absolute values are the same, take the larger number
        elif abs(curr_num) == abs(closest_num):
            closest_num = max(closest_num, curr_num)
    
    return closest_num

