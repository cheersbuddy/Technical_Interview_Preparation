```
long num = 954200L;
```
- Explanation:
- The correct syntax to declare a long variable is (data type)long (variable name)num = (value)954200L;
**Using Scanner**
  
Number Mirror
Write a program that takes a number 
𝑁
N as the input, and prints it to the output.

Input Format
The only line of input contains a single integer.

Output Format
Output the answer in a single line.

Constraints
0
≤
𝑁
≤
1
0
5
0≤N≤10 
5
 
Sample 1:
Input
Output
123
123
Explanation:
The input is 123. So the output is also 123.

Sample 2:
Input
Output
15
15
Explanation:
The input is 15. So the output is also 15.

```
  import java.util.Scanner;
class Codechef
{
	public static void main (String[] args)
	{
	    // Do not print anything here before taking input
	    Scanner sc = new Scanner(System.in);
	    
		int n = sc.nextInt();
		System.out.println(n);
		
		// Print the value of n
		
	}
 ```
Sample Input
123

Your Output
123

# Functions

```
import java.util.Scanner;

public class Main 
{
    public static void n (int nu){
            if (nu>=1){
                System.out.println("Positive\n");
            }
            else if (nu==0){
                System.out.println("Zero\n");
            }
            else{
                System.out.println("Negative\n");
            }
           
        }
        
    public static void main(String[] args) 
    {
        Scanner scanner = new Scanner(System.in);
        int num, num1, num2;

        
        
        num = scanner.nextInt(); // input first number
        // Check first number
        n(num);
        num1 = scanner.nextInt(); // input second number
        // Check second number
        n(num1);
        
        num2 = scanner.nextInt(); // input third number
        // Check third number
        n(num2);
        
    }
}
```
# QUESTION

Positive and Negative
Write a program to check whether the three given numbers as input are Positive, Negative, or Zero.

Sample 1:
Input
Output

20  Positive  
0    Zero  
-95  Negative

- Note: create a function outside the main class;;; and function should be declared static ``` public static void n (int nu)```
  
**running the loop with the input values times**

- Add Two Numbers
  
Your task is very simple: given two integers 
𝐴
A and 
𝐵
B, write a program to add these two numbers and output the sum.

Input Format
The first line contains an integer 
𝑇
T, the total number of test cases.
Then follow 
𝑇
T lines, each line contains two integers, 
𝐴
A and 
𝐵
B.
Output Format
For each test case, add 
𝐴
A and 
𝐵
B and display the sum in a new line.

Constraints
1
≤
𝑇
≤
1000
1≤T≤1000
0
≤
𝐴
,
𝐵
≤
10000
0≤A,B≤10000
Sample 1:
Input
Output
3
1 2
100 200
10 40
3
300
50
Explanation:
Testcase 1: 
1
+
2
=
3
1+2=3. Hence the first output is 
3
3.

Testcase 2: 
100
+
200
=
300
100+200=300. Hence the second output is 
300
300.

```
import java.util.*;
import java.lang.*;
import java.io.*;


class Codechef
{
    public static void n(int x, int y){
        System.out.println(x+y);
    }
	public static void main (String[] args)
	{
		Scanner sc = new Scanner(System.in);
		int t = sc.nextInt();
		while(t-->0)
		{
    		int a = sc.nextInt();
    		int b = sc.nextInt();
    		// write your code here
    		n(a,b);
		}
		
	}
}

```
