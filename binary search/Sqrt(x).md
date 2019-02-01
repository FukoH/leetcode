
Implement int sqrt(int x).

Compute and return the square root of x, where x is guaranteed to be a non-negative integer.

Since the return type is an integer, the decimal digits are truncated and only the integer part of the result is returned.


*Example1*：

>Input: 4
>Output: 2

*Example2*：

>Input: 8
>Output: 2
>Explanation: The square root of 8 is 2.82842..., and since 
             the decimal part is truncated, 2 is returned.

    class Solution:
        def mySqrt(self, x):
            """
            :type x: int
            :rtype: int
            """
            if x<=1:
                return x
            low = 1
            high = x
            while low<=high :
                mid = (low + high)//2
                if mid * mid >x:
                    high= mid - 1
                else:
                    if (mid+1)*(mid+1)>x:
                        return mid
                    low = mid + 1
            return x