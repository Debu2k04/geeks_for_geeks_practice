## 01. First Occurrence in Sorted

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/binary-search-1587115620/1)

### Problem Description

**Task:** Given a sorted array arr[] and an integer k, find the position(0-based indexing) at which k is present in the array using binary search. If k doesn't exist in arr[] return -1. Note: If multiple occurrences are there, please return the smallest index.Examples:Input: arr[] = [1, 2, 3, 4, 5], k = 4

#### Examples

##### Example 1

- **Output:**
```text
0
```
- **Explanation:** 1 appears at index 0.

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-10-28 21:49:23
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    public int firstSearch(int[] arr, int k) {
        // Code Here
        int n = arr.length;
        int low = 0, high = n-1;
        int indx= -1;
        while(low<=high){
            int mid = (low+high)/2;
            if (arr[mid]>k){
                high = mid-1;
            }
            else if(arr[mid]<k){
                low = mid +1;
                
            }
            else{ // arr[mid]==k
               
                indx = mid;
                high = mid-1;
                
            }
        }
        return indx;
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-26 12:04:09
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    public int firstSearch(int[] arr, int k) {
        // Code Here
        int n = arr.length;
        int low = 0, high = n-1;
        int indx= -1;
        while(low<=high){
            int mid = (low+high)/2;
            if (arr[mid]>k){
                high = mid-1;
            }
            else if(arr[mid]<k){
                low = mid +1;
                
            }
            else{ // arr[mid]==k
               
                indx = mid;
                high = mid-1;
                
            }
        }
        return indx;
    }
}
```

*Generated on: 10/28/2026, 9:49:45 PM*