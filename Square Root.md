## 01. Square Root

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/square-root/1)

### Problem Description

**Task:** Given a positive integer n, find the square root of n. If n is not a perfect square, then return the floor value.Floor value of any number is the greatest Integer which is less than or equal to that number.Examples: Input: n = 4

#### Examples

##### Example 1

- **Output:**
```text
1Explanation: 1 is a perfect square, so its square root is 1.
```
- **Explanation:** Since, 11 is not a perfect square, floor of square root of 11 is 3.Input: n = 1

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-29 22:15:01
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    int floorSqrt(int n) {
        // code here
        //root always small from the given numbers
        int root = 0;
        for (int i=0;i<=n;i++){
            if(i*i>n) break;
            root=i;
        }
        return root;
    }
}
```

*Generated on: 10/29/2026, 10:18:05 PM*