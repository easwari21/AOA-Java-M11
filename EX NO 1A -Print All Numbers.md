
# EX 1A Print All Numbers 
## DATE: 15.08.2025
## AIM:
To Write a Java program that takes an integer input N from the user and prints all the numbers from 1 to N, separated by spaces, on a single line..

## Algorithm
1.Start the program.

2.Input an integer N from the user.

3.Check condition: If N <= 0, display "Invalid input. N must be greater than 0." and stop.

4.Initialize a variable i = 1.

5.Use a loop to print numbers from 1 to N:
  While i <= N, print i followed by a space.
  Increment i by 1.

6.End loop and stop the program. 

## Program:
```
Program to implement Reverse a String
Developed by: Easwari M
Register Number: 212223240033
```
```
import java.util.Scanner;
public class GFG {
    public static void main(String[] args)
    {
    
      Scanner sc = new Scanner(System.in); 
      int n= sc.nextInt();
      if(n<=0)
      {
         System.out.println("invalid");
      }
      else
      {
          for(int i=1;i<=n;i++){
              System.out.print(i + " ");
          }
          System.out.println();
      }
        
    }
}
```
## Output:
<img width="578" height="178" alt="image" src="https://github.com/user-attachments/assets/db81a7d9-e411-4ad2-abb0-3a141440027e" />


## Result:
The program successfully print all the numbers from 1 to N. 
