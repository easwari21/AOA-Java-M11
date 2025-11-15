
# EX 1D Sorted Array using Divide and Conquer Approach.
## DATE: 26.08.2025

## AIM:

To write a Java program to for given constraints.
Given two sorted arrays nums1 and nums2 of size m and n respectively, return the median of the two sorted arrays.

The overall run time complexity should be O(log (m+n)).

## Algorithm

1.Start the program and read the sizes of the two sorted arrays, m and n, then input the elements of nums1 and nums2.
2.Initialize two pointers: p1 = 0 and p2 = 0 to traverse both arrays.
3.Use a helper function getMin() to return the smaller of the current elements from the two arrays and advance the corresponding pointer.
4.If m + n is even, skip (m + n)/2 − 1 elements, then take the average of the next two smallest values as the median.
5.If m + n is odd, skip (m + n)/2 elements, then take the next smallest value as the median.
6.Display the calculated median and end the program.  

## Program:
```
Program to implement Reverse a String
Developed by: Easwari M
Register Number: 212223240033
```
```
import java.util.*;

public class Solution {
    public static double findMedianSortedArrays(int[] nums1, int[] nums2) {
        int m = nums1.length, n = nums2.length;
        int[] merged = new int[m + n];
        int i = 0, j = 0, k = 0;
        while (i < m && j < n) {
            if (nums1[i] <= nums2[j]) {
                merged[k++] = nums1[i++];
            } else {
                merged[k++] = nums2[j++];
            }
        }
        while (i < m) merged[k++] = nums1[i++];
        while (j < n) merged[k++] = nums2[j++];
        int total = m + n;
        if (total % 2 == 1) {
            return merged[total / 2];
        } else {
            return (merged[(total / 2) - 1] + merged[total / 2]) / 2.0;
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int m = sc.nextInt();
        int[] nums1 = new int[m];
        for (int i = 0; i < m; i++) {
            nums1[i] = sc.nextInt();
        }
        int n = sc.nextInt();
        int[] nums2 = new int[n];
        for (int i = 0; i < n; i++) {
            nums2[i] = sc.nextInt();
        }

        double median = findMedianSortedArrays(nums1, nums2);
        System.out.println("Median of the two sorted arrays = " + median);

        sc.close();
    }
}

```
## Output:
<img width="911" height="355" alt="image" src="https://github.com/user-attachments/assets/7c5bbb25-2dcb-4545-a089-bea766f8b85b" />

## Result:
The program successfully implemented and the expected output is verified.
