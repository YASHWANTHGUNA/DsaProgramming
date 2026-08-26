## [2904. Shortest and Lexicographically Smallest Beautiful String](https://leetcode.com/problems/shortest-and-lexicographically-smallest-beautiful-string/submissions/2121235981)

### Submitted: Aug 27, 2026, 01:00 AM

- **Language:** Java
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
class Solution {
    public String shortestBeautifulSubstring(String s, int k) {
        int n = s.length(); 
        String ans= "";
        int left = 0;
        int right = 0; 
        int minLen = Integer.MAX_VALUE; 
        int count = 0; 
        while(right < n) {
             if(s.charAt(right)=='1') {
                count++; 
             }
           
            if(count == k) {
            while( s.charAt(left)=='0') {
                
                    left++;
                     
               
            } 
             int length = right-left+1; 
             if(length < minLen) {
                ans = s.substring(left, right+1); 
             }
             if(length == minLen) {
                String current  = s.substring(left, right+1);
               if( current.compareTo(ans) < 0) {
                  ans = current; 
               }
             }
             minLen = Math.min(minLen, length);

              count--;
              left++; 



            }
            right++; 
           
             
          
             

        }
        return ans; 


        
    }
}
```
