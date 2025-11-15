
# EX 1C Valid Pairs using Brute Force Approach
## DATE:23.08.2025

## AIM:
To write a Java program to for given constraints.
Given an integer array nums and an integer k, return the number of pairs (i, j) where i < j such that |nums[i] - nums[j]| == k.

The value of |x| is defined as:

x if x >= 0.
-x if x < 0.

## Algorithm

1.Start the program.
2.Input the size of the array n, the n array elements, and an integer k.
3.Initialize a counter variable count = 0.
4.Compare each pair of elements:
5.Use two loops: For each i from 0 to n-1, and for each j from i+1 to n-1, check if the absolute difference |nums[i] - nums[j]| == k.If true, increment count by 
6.Display the total count of such pairs and stop the program.   

## Program:
```
Program to implement Reverse a String
Developed by: Easwari M
Register Number: 212223240033
```
```
import java.util.Scanner;
public class CountPairsWithDifference {
    public static int countKDifference(int[] nums, int k) {
        int count=0;
        for(int i=0;i<nums.length;i++)
        {
            for(int j=i+1;j<nums.length;j++)
            {
                if(Math.abs(nums[i]-nums[j])==k)
                {
                    count++;
                }
            }
        }
        return count;
    }
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int n = sc.nextInt();
        int[] nums = new int[n];
        for (int i = 0; i < n; i++) {
            nums[i] = sc.nextInt();
        }
        int k = sc.nextInt();
        int result = countKDifference(nums, k);
        System.out.println(result);
        sc.close();
    }
}
```
## Output:
<img width="466" height="302" alt="image" src="https://github.com/user-attachments/assets/3da710b4-8565-42fd-b97d-89c7e3165576" />

## Result:
The program successfully implemented and the expected output is verified.
