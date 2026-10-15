## [845. Longest Mountain in Array](https://leetcode.com/problems/longest-mountain-in-array/submissions/2173299363)

### Submitted: Oct 15, 2026, 11:52 PM

- **Language:** Java
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
class Solution {
    public int longestMountain(int[] arr) {
        int n = arr.length; 
        int maxLen = 0; 
        for(int i = 1; i < n-1; i++) {
            if(arr[i] > arr[i-1] && arr[i] > arr[i+1]) {
                int left= i; 
                int right = i; 
                while(left > 0 && arr[left-1] < arr[left]) {
                    left--; 
                }
                while(right < n-1 && arr[right] > arr[right+1]) {
                    right++; 
                }
                int len = right-left+1; 
                maxLen = Math.max(maxLen, len); 

            }
        }
        return maxLen; 
        
    }
}
```
