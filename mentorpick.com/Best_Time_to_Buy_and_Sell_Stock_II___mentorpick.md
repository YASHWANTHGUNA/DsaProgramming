## [Best Time to Buy and Sell Stock II - mentorpick](https://mentorpick.com/problemset/bz-best-time-to-buy-and-sell-stock-ii)

### Submitted: Aug 13, 2026, 02:58 PM

- **Language:** Unknown
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```
import java.util.*;
import java.io.*;

class Main {
    public static void main(String[] args) {
         Scanner sc = new Scanner(System.in);

        int T = sc.nextInt();

        while (T-- > 0) {
            int n = sc.nextInt();

            int[] prices = new int[n];

            for (int i = 0; i < n; i++) {
                prices[i] = sc.nextInt();
            }

            int profit = 0;

            for (int i = 1; i < n; i++) {
                if (prices[i] > prices[i - 1]) {
                    profit += prices[i] - prices[i - 1];
                }
            }

            System.out.println(profit);
        }

        sc.close();
    }
}
```
