## [238. Product of Array Except Self](https://leetcode.com/problems/product-of-array-except-self/submissions/2100694033)

### Submitted: Aug 9, 2026, 11:26 PM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
class Solution {
    public int[] productExceptSelf(int[] nums) {
        int n = nums.length; 
        int[] arr = new int[n]; 
        int lp = 1; 
        for(int i = 0; i < n; i++) {
            arr[i] = lp;
            lp = lp * nums[i];
        }
        int rp = 1;
        for(int i  = n-1; i >= 0; i--) {
            arr[i] = arr[i]*rp; 
            rp = rp * nums[i];
        }
        return arr; 
        
    }
}
```
