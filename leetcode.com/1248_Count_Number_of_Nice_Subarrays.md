## [1248. Count Number of Nice Subarrays](https://leetcode.com/problems/count-number-of-nice-subarrays/description)

### Submitted: Nov 11, 2026, 08:03 PM

- **Language:** Java
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
class Solution {
    public int numberOfSubarrays(int[] nums, int k) {
        int n = nums.length; 
        int count= 0; 
        int left = 0; 
        int right = 0; 
        int oddCount = 0; 
        int total = 0; 
        
        while(right < n ) {
            if(nums[right] % 2 == 1) {
                oddCount++; 
                count = 0; 

            }
            while(oddCount > k) {
                if(nums[left] % 2 == 1) {
                    oddCount--; 
                }
                left++; 
            }
            if(oddCount == k) {
                while(nums[left] % 2 == 0 ) {
                    count++; 
                    left++; 
                }
                 total += (count + 1);
            }
           
            right++; 
        }
        return total; 
        
    }
}
```
