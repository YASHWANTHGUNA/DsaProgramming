## [713. Subarray Product Less Than K](https://leetcode.com/problems/subarray-product-less-than-k/submissions/2178954151)

### Submitted: Oct 22, 2026, 09:24 PM

- **Language:** Java
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
class Solution {
    public int numSubarrayProductLessThanK(int[] nums, int k) {
        int n = nums.length; 
        int left = 0; 
        int product = 1;
        int count = 0; 
        if(k <= 1) return 0; 
        for(int right = 0; right < n; right++) {
            product *= nums[right]; 
            while(product >= k) {
                product /= nums[left];
                left++;

                
            } 
            int added = right-left+1; 
            count += added;
        }
        return count; 

    }
}
```
