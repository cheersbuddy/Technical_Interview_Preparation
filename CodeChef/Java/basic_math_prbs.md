- ![WhatsApp Image 2024-07-02 at 11 41 26_2ba5f2c6](https://github.com/cheersbuddy/Technical_Interview_Preparation/assets/126586644/ce4fdec5-8c29-4dbc-accb-911504f6d5e6)

- ![WhatsApp Image 2024-07-02 at 11 41 26_91f46d2f](https://github.com/cheersbuddy/Technical_Interview_Preparation/assets/126586644/4d63bf8d-9e81-47e4-99cc-c004e6ba8f33)

- ![WhatsApp Image 2024-07-02 at 11 41 26_8a296daf](https://github.com/cheersbuddy/Technical_Interview_Preparation/assets/126586644/06e06800-b294-4e4c-95a5-43148315f039)


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
--- 
Sum of Digits
You're given an integer N. Write a program to calculate the sum of all the digits of N.

Input Format
The first line contains an integer T, the total number of testcases. Then follow T lines, each line contains an integer N.

Output Format
For each test case, calculate the sum of digits of N, and display it in a new line.

Constraints
1
≤
𝑇
≤
1000
1≤T≤1000
1
≤
𝑁
≤
1000000
1≤N≤1000000
Sample 1:
Input
Output
3 
12345
31203
2123
15
9
8
```
import java.util.*;
import java.lang.*;
import java.io.*;

class Codechef
{
	public static void main (String[] args) throws java.lang.Exception
	{
		// your code goes here
		Scanner s= new Scanner(System.in);
		int t=s.nextInt();
		
		for(int i=0;i<t;i++){
		    int sum=0;
		    int a=s.nextInt();
		    while(a>0){
		        int temp=a%10;
		        sum+=temp;
		        a/=10;
		        //if(a==1)
		        // sum+=1;
		        
		    }
		    System.out.println(sum);
		}

	}
}
```
Your Output

15

9

8
