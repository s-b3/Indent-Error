

# Problem Statement

Write a function to find the longest common prefix string amongst an array of strings. If there is no common prefix, return an empty string `""`.

## Example 1

**Input:**

```python
strs = ["flower", "flow", "flight"]
```

**Output:**

```python
"fl"
```

## Code:
```python

def longest_common_prefix(arr_of_strings):
    if not arr_of_strings:
        return ""
    
    prefix = arr_of_strings[0]
    
    for string in arr_of_strings[1:]:
        while not string.startswith(prefix):
            prefix = prefix[:-1]
            if not prefix:
                return ""
    
    return prefix
