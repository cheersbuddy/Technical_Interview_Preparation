Second Max of Three Numbers
Problem Statement
Write a program that accepts sets of three numbers, and prints the second-maximum number among the three.

Input
First line contains the number of triples, N.
The next N lines which follow each have three space separated integers.
Output
For each of the N triples, output one new line which contains the second-maximum integer among the three.

Constraints
1 ≤ N ≤ 6
1 ≤ every integer ≤ 10000
The three integers in a single triplet are all distinct. That is, no two of them are equal.
Sample 1:
Input
Output
3
1 2 3
10 15 5
100 999 500
2
10
500

```java
import java.util.Scanner;

public class Codechef {
    public static void main(String[] args) throws java.lang.Exception {
        Scanner s = new Scanner(System.in);
        int t = s.nextInt();
        
        for (int i = 0; i < t; i++) {
            int a = s.nextInt();
            int b = s.nextInt();
            int c = s.nextInt();
            
            int secondMax;
            if ((a > b && a < c) || (a > c && a < b)) {
                secondMax = a;
            } else if ((b > a && b < c) || (b > c && b < a)) {
                secondMax = b;
            } else {
                secondMax = c;
            }
            
            System.out.println(secondMax);
        }
    }
}
```

### Explanation:
1. **Input Handling**: We use a `Scanner` to read the input. We first read the number of triples `t`.
2. **Processing Each Triple**: For each triple, we read the three integers `a`, `b`, and `c`.
3. **Finding the Second Maximum**:
   - We use conditional statements to determine the second maximum value by comparing the integers directly.
4. **Output**: We print the second maximum for each triple.

This solution directly compares the three numbers and finds the second largest among them, which is more efficient and easier to understand than the previous logic.
