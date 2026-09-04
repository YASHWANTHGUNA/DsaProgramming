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

---

### Submitted: Sep 4, 2026, 08:33 PM

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
        // if(costs[0] > coins) {
        //     return 0; 
        // }
        
            
            while(i < n && coins >= costs[i]) {
               
                    coins -= costs[i];
                    count++; 
                    
                    i++;
                
            }
        
        return count; 
        
    }
}
```

---

### Submitted: Sep 4, 2026, 09:34 PM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
class Solution {
    public int maxIceCream(int[] costs, int coins) {
        int n = costs.length; 
        int maxCost = costs[0]; 
        for(int i = 0; i < n; i ++) {
            if(costs[i] > maxCost) {
                maxCost = costs[i];
            }
        }
        int[] freq = new int[maxCost+1]; 
        for(int cost : costs) {
            freq[cost]++;
        }
        int iceCreamCount = 0; 
        for(int cost = 1; cost <= maxCost;cost++)  {
            if(freq[cost]==0) continue; 
            long canBuy = coins/cost; 
            long countToBuy = Math.min(canBuy, freq[cost]);
            iceCreamCount += (int) countToBuy; 
            coins -= countToBuy * cost; 
            if(coins <= 0) {
                break; 
            }
        }
        return iceCreamCount;

        
    }
}
```
