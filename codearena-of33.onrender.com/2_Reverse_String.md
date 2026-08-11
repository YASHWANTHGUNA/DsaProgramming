## [2. Reverse String](https://codearena-of33.onrender.com/problems/2)

### Submitted: Aug 12, 2026, 12:21 AM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
import java.util.*;

public class Main {
    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        char[] s = sc.next().toCharArray();

        int left = 0;
        int right = s.length - 1;

        while (left < right) {

            char temp = s[left];
            s[left] = s[right];
            s[right] = temp;

            left++;
            right--;
        }

        System.out.println(new String(s));
    }
}
```
