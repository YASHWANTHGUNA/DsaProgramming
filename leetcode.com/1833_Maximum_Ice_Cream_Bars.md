## [1833. Maximum Ice Cream Bars](https://leetcode.com/problems/maximum-ice-cream-bars/submissions/2130819719)

### Submitted: Sep 4, 2026, 08:28 PM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
class Solution {
    public int maxIceCream(int[] costs, int coins) {
        int n = costs.length; 
        int count = 0; 
        Arrays.sort(costs); 
        int i = 0; 
        if(costs[0] > coins) {
            return 0; 
        }
        
            
            while(i < n && coins >= costs[i]) {
               
                    coins -= costs[i];
                    count++; 
                    
                    i++;
                
            }
        
        return count; 
        
    }
}
```
