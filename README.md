# Valid Parentheses

LeetCode #20: given a string containing only `()[]{}`, determine whether the brackets are valid.

## Rules
1. Open brackets must be closed by the same type of bracket.
2. Open brackets must be closed in the correct order.
3. Every close bracket has a matching open bracket of the same type.

## Approach
- Use a stack that stores the **expected closing bracket**.
- On an opener, push its matching closer.
- On a closer, the stack must be non-empty and the popped value must equal the current character.
- Return `True` only if the stack is empty at the end.
- If the length is odd, return `False` immediately.

## Complexity
- Time: O(n)
- Space: O(n)

## Usage
```python
from valid_parentheses import Solution

print(Solution().isValid("()[]{}"))  # True
print(Solution().isValid("([)]"))    # False
```

## Examples
| Input    | Output |
|----------|--------|
| `"()"`     | true   |
| `"()[]{}"` | true   |
| `"(]"`     | false  |
| `"([])"`   | true   |
| `"([)]"`   | false  |

## Constraints
- `1 <= s.length <= 10^4`
- `s` consists only of `()[]{}`
