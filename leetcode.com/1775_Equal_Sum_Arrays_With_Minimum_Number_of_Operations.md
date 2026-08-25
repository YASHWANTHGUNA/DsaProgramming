## [1775. Equal Sum Arrays With Minimum Number of Operations](https://leetcode.com/problems/equal-sum-arrays-with-minimum-number-of-operations/submissions/2120119792)

### Submitted: Aug 26, 2026, 01:12 AM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
import java.util.Arrays;

class Solution {
    public int minOperations(int[] nums1, int[] nums2) {
        int n = nums1.length; 
        int m = nums2.length; 
        Arrays.sort(nums1);
        Arrays.sort(nums2); 
        int minOps = 0; 
        int sum1 = 0; 
        int sum2 = 0; 
        
        if((n > m * 6) || (m > n * 6)) {
            return -1; 
        }
        
        for(int i = 0; i < n; i++) {
            sum1 += nums1[i]; 
        } 
        for(int i = 0; i < m; i++) {
            sum2 += nums2[i]; 
        }
        
        if(sum1 == sum2) {
            return 0; 
        } else {
            int largerSum = Math.max(sum1, sum2); 
            int smallerSum = Math.min(sum1, sum2); 
            int difference = largerSum - smallerSum; 
            
            if(sum1 < sum2) {
                int i = 0; 
                int j = m - 1; 
                
                while(difference > 0 && i < n && j >= 0) { 
                    int increaseCapacity = 6 - nums1[i];
                    int decreaseCapacity = nums2[j]-1; 
                    if(increaseCapacity > decreaseCapacity) {
                        difference -= increaseCapacity; 
                        i++; 
                    } else {
                        difference -= decreaseCapacity; 
                        j--; 
                    }
                    minOps++; 
                } 
                
                while(difference > 0 && j >= 0) {
                    difference -= nums2[j] - 1; 
                    j--;
                    minOps++; 
                } 
                while(difference > 0 && i < n) {
                    difference -= 6 - nums1[i]; 
                    i++; 
                    minOps++; 
                }
            } else {
                if(sum2 < sum1) {
                    int i = n - 1; 
                    int j = 0; 
                    
                    while(difference > 0 && i >= 0 && j < m) { 
                        int increaseCapacity = nums1[i]-1; 
                        int decreaseCapacity = 6-nums2[j]; 
                        
                        
                        if(increaseCapacity > decreaseCapacity) {
                            difference -= increaseCapacity; 
                            i--; 
                        } else {
                            difference -= decreaseCapacity; 
                            j++; 
                        }
                        minOps++; 
                    } 
                    while(difference > 0 && j < m) { 
                        difference -= 6-nums2[j]; 
                        j++;
                        minOps++; 
                    } 
                    while(difference > 0 && i >= 0) {
                        difference -= nums1[i]-1; 
                        i--; 
                        minOps++; 
                    }
                }
            }
        }
      
        return minOps; 
    }
}
```
