## [ACE Engineering College](https://ace.campustrack.in/question/check-if-both-numbers-are-negative)

### Submitted: Aug 13, 2026, 12:43 PM

- **Language:** Java
- **Time Complexity:** O(1) (estimated)
- **Space Complexity:** O(1) (estimated)

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.io.IOException;

//===== Declare Imports here if required =====


public class Main {

    //===== Declare Global Variables / Functions here if required =====


    public static void main(String[] args) throws IOException {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int a = Integer.parseInt(br.readLine());
        int b = Integer.parseInt(br.readLine());

        //===== Declare Local Variables / Functions here if required =====


        //===== Write Your Logic Here =====

            if(a < 0  && b <0) {
                System.out.println("True");
            } else {
                System.out.println("False");
            }
    }
}
```

---

### Submitted: Aug 13, 2026, 03:01 PM

- **Language:** Java
- **Time Complexity:** O(n) (estimated)
- **Space Complexity:** O(n) (estimated - uses extra data structure)

```java
import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.StringTokenizer;
import java.util.Arrays;

//===== Declare Imports here if required =====


public class Main {

    //===== Declare Global Variables / Functions here if required =====


    public static void main(String[] args) throws Exception {
        BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
        int n = Integer.parseInt(br.readLine());
        StringTokenizer stA = new StringTokenizer(br.readLine());

        //===== Declare Local Variables / Functions here if required =====


        int[] A = new int[n];
        for (int i = 0; i < n; i++) {
            A[i] = Integer.parseInt(stA.nextToken());
        }
        StringTokenizer stB = new StringTokenizer(br.readLine());
        int[] B = new int[n];
        for (int i = 0; i < n; i++) {
            B[i] = Integer.parseInt(stB.nextToken());
        }

        //===== Write Your Logic Here =====
        Arrays.sort(A);
        Arrays.sort(B);
        if(Arrays.equals(A, B)) {
            System.out.print("YES");
        } else {
            System.out.print("NO");
        }
 
    }
}
```
