## [2139. Minimum Moves to Reach Target Score](https://leetcode.com/problems/minimum-moves-to-reach-target-score/submissions/2115429521)

### Submitted: Aug 22, 2026, 12:13 AM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
class Solution {
    public int minMoves(int target, int maxDoubles) {
        int moves = 0; 
        while(target > 1 ) {
            if(maxDoubles == 0) {
                moves += target-1; 
                break; 
            } else {
                if(target % 2 == 0) {
                    target /= 2; 
                    maxDoubles--; 
                    moves++;
                } else {
                    target -= 1; 
                    moves++; 
                }
            }
            
        }
        return moves;
        
    }
}
```
