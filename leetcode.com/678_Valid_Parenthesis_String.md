## [678. Valid Parenthesis String](https://leetcode.com/problems/valid-parenthesis-string/submissions/2162420758)

### Submitted: Oct 4, 2026, 11:45 PM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
class Solution {
    public boolean checkValidString(String s) {
        Stack<Integer> openStack = new Stack<>();
        Stack<Integer> starStack = new Stack<>(); 
        for(int i = 0; i < s.length(); i++) {
            char c = s.charAt(i);
            if(c=='(') {
                openStack.push(i);
            } else if(c=='*') {
                starStack.push(i);
            } else {
                if(!openStack.isEmpty()) {
                    openStack.pop();
                } else if(!starStack.isEmpty()) {
                    starStack.pop();
                } else {
                    return false; 
                }
            }
        }
        while(!openStack.isEmpty() && !starStack.isEmpty()) {
            if(openStack.peek() < starStack.peek()) {
                openStack.pop();
                starStack.pop(); 
            } else {
                break; 
            }
        }
        return openStack.isEmpty(); 
        
    }
}
```
