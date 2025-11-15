
# EX 1B Power of 2

## DATE:21/08/2025
## AIM:

To write a Java program to for given constraints.Given an integer n, return true if it is a power of two. Otherwise, return false.
An integer n is a power of two, if there exists an integer x such that n == 2x.

## Algorithm

1.Start the program.

2.Read an integer n from the user.

3.If n ≤ 0, display false and terminate the program.

4.Use a bitwise check: compute n & (n - 1).

5.If the result is 0, then n is a power of two.

6.Display true or false accordingly and end the program.

## Program:
```
Program to implement Reverse a String
Developed by: Easwari M
Register Number:  212223240033
```
```
import java.util.Scanner;

public class Solution {

    public boolean isPowerOfTwo(int n) {
     //Type your code here
     if(n<=0)
     {
         return false;
     }
     return (n &(n-1))==0;
    }
     //
    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        Solution sol = new Solution();
        int n = scanner.nextInt();

        boolean result = sol.isPowerOfTwo(n);
        System.out.println(result);

        scanner.close();
    }
}

```

## Output:
<img width="501" height="221" alt="image" src="https://github.com/user-attachments/assets/18f21732-99ed-4096-8bfa-d321a21d9e1c" />

## Result:
The program successfully implemented and the expected output is verified.
