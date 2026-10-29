## 01. Floor in Sorted Array

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/floor-in-a-sorted-array-1587115620/1)

### Problem Description

**Task:** Given a sorted array arr[] and an integer x, find the index (0-based) of the largest element in arr[] that is less than or equal to x. This element is called the floor of x. If such an element does not exist, return -1.Note: In case of multiple occurrences of floor of x, return the index of the last occurrence.ExamplesInput: arr[] = [1, 2, 8, 10, 10, 12, 19], x = 5

#### Examples

##### Example 1

- **Output:**
```text
4
```
- **Explanation:** No element less than or equal to 0 is found. So, output is -1.Constraints:1 ≤ arr.size() ≤ 10⁶¹ ≤ arr[i] ≤ 10⁶⁰ ≤ x ≤^ arr[n-1]

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (1)

#### Solution 1 (Java)

- **Submitted:** 2026-10-29 21:58:03
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    static int findFloor(int[] arr, int x) {
        // code here
        int n = arr.length;
        int low = 0 , high = n-1;
        int indx = -1;
        while(low<=high){
            int mid = (low+high)/2;
            if(arr[mid]>x) high = mid-1;
            else if (arr[mid]<=x) {
                indx=mid;
                low = mid +1;
            }
            else 
                return -1;
        }
        return indx;
    }
}
```

*Generated on: 10/29/2026, 9:58:34 PM*