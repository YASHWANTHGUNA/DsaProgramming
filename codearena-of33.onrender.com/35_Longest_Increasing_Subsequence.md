## [35. Longest Increasing Subsequence](https://codearena-of33.onrender.com/problems/35)

### Submitted: Aug 13, 2026, 03:02 PM

- **Language:** Java
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
// Java Solution
import java.util.*;
import java.io.*;

public class Main {
    public static void main(String[] args){
        Scanner sc = new Scanner(System.in);

        ArrayList<Integer> list = new ArrayList<>();

        while (sc.hasNextInt()) {
            list.add(sc.nextInt());
        }

        int n = list.size();

        int[] nums = new int[n];

        for (int i = 0; i < n; i++) {
            nums[i] = list.get(i);
        }

        int[] dp = new int[n];

        Arrays.fill(dp, 1);

        int maxLen = 1;

        for (int i = 0; i < n; i++) {

            for (int j = 0; j < i; j++) {

                if (nums[j] < nums[i]) {
                    dp[i] = Math.max(dp[i], dp[j] + 1);
                }
            }

            maxLen = Math.max(maxLen, dp[i]);
        }

        System.out.println(maxLen);

        sc.close();
    }
}
```
