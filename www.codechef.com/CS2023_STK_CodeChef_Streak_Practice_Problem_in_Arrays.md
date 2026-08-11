## [CS2023_STK. CodeChef Streak Practice Problem in Arrays](https://www.codechef.com/practice/course/arrays-new/ARRAYSP01/problems/CS2023_STK)

### Submitted: Aug 11, 2026, 10:30 PM

- **Language:** Unknown
- **Time Complexity:** O(1) (estimated)
- **Space Complexity:** O(1) (estimated)

```
        Scanner scanner = new Scanner(System.in);
```

---

### Submitted: Aug 11, 2026, 10:39 PM

- **Language:** Unknown
- **Time Complexity:** O(1) (estimated)
- **Space Complexity:** O(1) (estimated)

```
        Scanner scanner = new Scanner(System.in);
```

---

### Submitted: Aug 11, 2026, 10:57 PM

- **Language:** Unknown
- **Time Complexity:** O(n^2) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        int t = scanner.nextInt();

        while (t-- > 0) {
            int n = scanner.nextInt();

            int[] a = new int[n];
            int[] b = new int[n];

            for (int i = 0; i < n; i++) {
                a[i] = scanner.nextInt();
            }

            for (int i = 0; i < n; i++) {
                b[i] = scanner.nextInt();
            }

            int omStreak = 0;
            int maxOmStreak = 0;

            for (int i = 0; i < n; i++) {
                if (a[i] > 0) {
                    omStreak++;
                    maxOmStreak = Math.max(maxOmStreak, omStreak);
                } else {
                    omStreak = 0;
                }
            }

            int addyStreak = 0;
            int maxAddyStreak = 0;

            for (int i = 0; i < n; i++) {
                if (b[i] > 0) {
                    addyStreak++;
                    maxAddyStreak = Math.max(maxAddyStreak, addyStreak);
                } else {
                    addyStreak = 0;
                }
            }

            if (maxOmStreak > maxAddyStreak) {
                System.out.println("OM");
            } else if (maxAddyStreak > maxOmStreak) {
                System.out.println("ADDY");
            } else {
                System.out.println("DRAW");
            }
        }

        scanner.close();
    }
}
```
