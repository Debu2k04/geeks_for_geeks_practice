## 01. First and Last in Sorted

The problem can be found at the following link: [Question Link](https://www.geeksforgeeks.org/problems/first-and-last-occurrences-of-x3116/1)

### Problem Description

**Task:** Given a sorted array arr[] with possibly some duplicates, find the first and last occurrences of an element x in the given array.Note: If the number x is not found in the array then return both the indices as -1.Examples:Input: arr[] = [1, 3, 5, 5, 5, 5, 67, 123, 125], x = 5

#### Examples

##### Example 1

- **Output:**
```text
[2, 5]
```
- **Explanation:** First occurrence of 5 is at index 2 and last occurrence of 5 is at index 5

##### Example 2

- **Input:**
```text
arr[] = [1, 3, 5, 5, 5, 5, 7, 123, 125], x = 7
```
- **Output:**
```text
[-1, -1]
```
- **Explanation:** No occurrence of 4 in the array, so, output is [-1, -1]

### Time and Auxiliary Space Complexity

- **Expected Time Complexity:** O(log n)
- **Expected Auxiliary Space Complexity:** O(1)

### Accepted Solutions (2)

#### Solution 1 (Java)

- **Submitted:** 2026-10-28 21:56:19
- **Status:** Correct
- **Marks:** 0

```java
class Solution {
	ArrayList<Integer> find(int arr[], int x) {
		// code here
		// find first index
		int n = arr.length;
		int low = 0, high = n - 1;
		int indx1 = -1;
		int indx2 = -1;
		while (low <= high) {
			int mid = (low + high)/2;
			if (arr[mid]> x) {
				high = mid - 1;
			}
			else if (arr[mid]<x) {
				low = mid + 1;
			}
			else { // arr[mid]== k
				indx1 = mid;
			high = mid - 1;
			    
			}
		}
	       low =0 ; high= n-1;
			while (low <= high) {
			int mid = (low + high)/2;
			if (arr[mid]> x) {
				high = mid - 1;
			}
			else if (arr[mid]<x) {
				low = mid + 1;
			}
			else {// arr[mid]== k
				indx2 = mid;
			    low = mid+1;
			}
			}
	       
		ArrayList<Integer> ans = new ArrayList<>();
	      ans.add(indx1);
          ans.add(indx2);
          return ans ;
	}
}
```

#### Solution 2 (Java)

- **Submitted:** 2026-10-26 12:53:23
- **Status:** Correct
- **Marks:** 4

```java
class Solution {
	ArrayList<Integer> find(int arr[], int x) {
		// code here
		// find first index
		int n = arr.length;
		int low = 0, high = n - 1;
		int indx1 = -1;
		int indx2 = -1;
		while (low <= high) {
			int mid = (low + high)/2;
			if (arr[mid]> x) {
				high = mid - 1;
			}
			else if (arr[mid]<x) {
				low = mid + 1;
			}
			else { // arr[mid]== k
				indx1 = mid;
			high = mid - 1;
			    
			}
		}
	
		 low =0 ; high= n-1;
			while (low <= high) {
			int mid = (low + high)/2;
			if (arr[mid]> x) {
				high = mid - 1;
			}
			else if (arr[mid]<x) {
				low = mid + 1;
			}
			else {// arr[mid]== k
				indx2 = mid;
			    low = mid+1;
			}
			    
		}
		ArrayList<Integer> ans = new ArrayList<>();
	      ans.add(indx1);
          ans.add(indx2);
          return ans ;
	}
}
```

*Generated on: 10/28/2026, 9:56:46 PM*