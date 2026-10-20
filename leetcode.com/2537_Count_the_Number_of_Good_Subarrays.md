## [2537. Count the Number of Good Subarrays](https://leetcode.com/problems/count-the-number-of-good-subarrays/submissions/2177391470)

### Submitted: Oct 21, 2026, 12:52 AM

- **Language:** Java
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
class Solution {
    public long countGood(int[] nums, int k) {
        int n = nums.length; 
        int left = 0; 
        int pairs = 0; 
        long ans = 0; 
        HashMap<Integer, Integer> map = new HashMap<>();
        for(int right = 0; right < n; right++) {
        pairs += map.getOrDefault(nums[right],0);  
        map.put(nums[right], map.getOrDefault(nums[right],0)+1);
            

            while(pairs >= k) {
                ans += n-right; 
                int removed = nums[left]; 
                map.put(removed, map.get(removed) - 1);
                pairs -= map.get(removed); 
                
                left++;
                 
            }
        }
        return ans; 

        
    }
}
```
