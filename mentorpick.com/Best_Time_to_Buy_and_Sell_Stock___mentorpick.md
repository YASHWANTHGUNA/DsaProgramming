## [Best Time to Buy and Sell Stock - mentorpick](https://mentorpick.com/problemset/bz-best-time-to-buy-and-sell-stock)

### Submitted: Aug 13, 2026, 02:47 PM

- **Language:** Unknown
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```
import java.util.*;
import java.io.*;

class Main {

    public static int maxProfit(int[] prices) {
        int maxProfit = 0;
        int minPrice = Integer.MAX_VALUE;

        for (int price : prices) {

            if (price < minPrice) {
                minPrice = price;
            } 
            else {
                int profit = price - minPrice;

                if (profit > maxProfit) {
                    maxProfit = profit;
                }
            }
        }

        return maxProfit;
    }

    public static void main(String[] args) {

        Scanner sc = new Scanner(System.in);

        int T = sc.nextInt();

        while (T-- > 0) {

            int N = sc.nextInt();

            int[] prices = new int[N];

            for (int i = 0; i < N; i++) {
                prices[i] = sc.nextInt();
            }

            System.out.println(maxProfit(prices));
        }

        sc.close();
    }
}
```
