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
