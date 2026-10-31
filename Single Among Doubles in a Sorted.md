## 01. Single Among Doubles in a Sorted

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/find-the-element-that-appears-once-in-sorted-array0624/1)

### Problem Description

**Task:** Given a sorted array arr[]. Find the element that appears only once in the array. All other elements appear exactly twice.

#### Examples

##### Example 1

- **Input:**
```text
arr[] = [1, 1, 2, 2, 3, 3, 4, 50, 50, 65, 65]
```
- **Output:**
```text
4
```
- **Explanation:** 4 is the only element that appears exactly once.

##### Example 2

- **Input:**
```text
arr[] = [5]
```
- **Output:**
```text
5
```

##### Example 3

- **Input:**
```text
arr[] = [1, 2, 2, 3, 3]
```
- **Output:**
```text
1
```

#### Constraints

- **1.** `1 ≤ arr.size() ≤ 2 * 10⁶¹ ≤ arr[i] ≤ 10⁶`

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-31 10:38:34
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
    int single(int[] arr) {
        // code here
        int n = arr.length;
        if(n==1) return arr[0];
        if(arr[0] != arr[1]) return arr[0];
        if(arr[n-1] != arr[n-2]) return arr[n-1];
        int low =0,high=n-1;
        while(low<=high){
            int mid = low +(high-low)/2;
            if (arr[mid] != arr[mid-1] && arr[mid] != arr[mid+1]) return arr[mid];
            int f = mid , s = mid;
            if(arr[mid]==arr[mid-1]) f= mid-1;
            else s = mid+1;
            int leftElement= f - low;
            int rightElement= high - s;
            if(leftElement%2==0) low = s+1;
            else high = f-1;
        }
        return -1;
    }
}
```

*Generated on: 10/31/2026, 10:38:54 AM*