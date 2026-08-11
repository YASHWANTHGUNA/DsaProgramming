## [First Occurrence in Sorted | Practice | GeeksforGeeks](https://www.geeksforgeeks.org/problems/binary-search-1587115620/1)

### Submitted: Aug 12, 2026, 12:07 AM

- **Language:** Unknown
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(1) (estimated)

```
class Solution {
    public int firstSearch(int[] arr, int k) {
        // Code Here
        int n = arr.length; 
        
        int low  = 0; 
        int high = n-1; 
        int res = -1; 
        
        while(low <= high) {
            int mid = low + (high-low)/2; 
            if(arr[mid]== k) {
                res = mid; 
                high = mid-1; 
            } else if(arr[mid] > k) {
                high = mid-1; 
            } else {
                low = mid+1; 
            }
        }
        return res; 
    }
}
```
