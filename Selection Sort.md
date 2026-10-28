## 01. Selection Sort

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/selection-sort/1)

### Problem Description

**Task:** Given an array arr[], use selection sort to sort arr[] in increasing order.Examples :Input: arr[] = [4, 1, 3, 9, 7]

#### Examples

##### Example 1

- **Output:**
```text
[14, 20, 30, 31, 38]
```
- **Explanation:** Maintain sorted (in bold) and unsorted subarrays. Select 1. Array becomes 1 4 3 9 7. Select 3. Array becomes 1 3 4 9 7. Select 4. Array becomes 1 3 4 9 7. Select 7. Array becomes 1 3 4 7 9. Select 9. Array becomes 1 3 4 7 9.Input: arr[] = [10, 9, 8, 7, 6, 5, 4, 3, 2, 1]

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(n^2)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (3)

#### Solution 1 (Java)

- **Submitted:** 2026-10-28 21:33:47
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    void selectionSort(int[] arr) {
        // code here
        int n = arr.length;
        for (int i=0; i<n-1; i++){
             int min = Integer.MAX_VALUE;
             int indx=0;
             for(int j=i; j<n; j++){
                 if (arr[j]<min) {
                     min = arr[j];
                     indx=j;
                 }
             }
             int temp = arr[i];
             arr[i] = arr[indx];
             arr[indx] = temp;
        } 
    }
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-24 11:56:22
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
    void selectionSort(int[] arr) {
        // code here
        int n = arr.length;
        for (int i=0; i<n-1; i++){
             int min = Integer.MAX_VALUE;
             int indx=0;
             for(int j=i; j<n; j++){
                 if (arr[j]<min) {
                     min = arr[j];
                     indx=j;
                 }
             }
             int temp = arr[i];
             arr[i] = arr[indx];
             arr[indx] = temp;
        } 
    }
}
```

#### Solution 3 (Java)

- **Submitted:** 2026-10-23 11:26:26
- **Status:** Correct
- **Marks:** 2

```java
class Solution {
    void selectionSort(int[] arr) {
        // code here
        int n = arr.length;
        for (int i=0; i<n-1; i++){
             int min = Integer.MAX_VALUE;
             int indx=0;
             for(int j=i; j<n; j++){
                 if (arr[j]<min) {
                     min = arr[j];
                     indx=j;
                 }
             }
             int temp = arr[i];
             arr[i] = arr[indx];
             arr[indx] = temp;
        } 
    }
}
```

*Generated on: 10/28/2026, 9:39:54 PM*