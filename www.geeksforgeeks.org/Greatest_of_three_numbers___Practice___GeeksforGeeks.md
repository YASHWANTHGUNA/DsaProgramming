## [Greatest of three numbers | Practice | GeeksforGeeks](https://www.geeksforgeeks.org/problems/greatest-of-three-numbers2520/1)

### Submitted: Aug 11, 2026, 12:17 PM

- **Language:** Unknown
- **Time Complexity:** O(1) (estimated)
- **Space Complexity:** O(1) (estimated)

```
import java.util.Scanner;

class GFG {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();

        if(a > b && a > c) {
            System.out.println(a);
        } else if(b >  a && b > c) {
            System.out.println(b);
        } else {
            System.out.println(c); 
        }
        
    }
}
```
