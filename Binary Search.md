## 01. Binary Search

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/who-will-win-1587115621/1)

### Problem Description

**Task:** Given a sorted array arr[] of distinct integers and an integer k, return the 0-based index of k if it is present in the array. Otherwise, return -1.Examples:Input: arr[] = [1, 2, 3, 4, 6], k = 6

#### Examples

##### Example 1

- **Output:**
```text
-1
```
- **Explanation:** 3 is not present in the array.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-10-28 21:47:49
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public int binarySearch(int[] arr, int k) {
        // code here
        int n = arr.length;
        int low = 0 , high = n-1;
        while(low<= high){
            int mid=(low+high)/2;
            if(arr[mid]==k){
                return mid;
            }
            else if (arr[mid]>k){
                high = mid-1;
            }
            else 
                low = mid+1;
        }
        return -1;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-26 11:40:48
- **Status:** Correct
- **Marks:** 1

```java
class Solution {
    public int binarySearch(int[] arr, int k) {
        // code here
        int n = arr.length;
        int low = 0 , high = n-1;
        while(low<= high){
            int mid=(low+high)/2;
            if(arr[mid]==k){
                return mid;
            }
            else if (arr[mid]>k){
                high = mid-1;
            }
            else 
                low = mid+1;
        }
        return -1;
    }
}
```

*Generated on: 10/28/2026, 9:48:21 PM*