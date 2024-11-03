# GCD-Quest-in-Subarray

In a small village, Aarav loved solving number puzzles. One day, his friend Meera gave him an array A of size N and posed an interesting challenge. She asked Aarav to find out if there was any subarray within the array whose greatest common divisor (GCD) was equal to 1. Intrigued by the challenge, Aarav set out to solve it. Can you help Aarav find if such a subarray exists?

Input
The first line of the input contains a single integer N.
The second line of the input contains N space-separated integers.

Constraints
1 ≤ N ≤ 105
1 ≤ Ai ≤ 109
Output
Print "YES" if there is any subarray in the array whose GCD is equal to 1, else print "NO", without the quotes.

import math
from functools import reduce

def gcd_of_array(arr):
    return reduce(math.gcd, arr)

N = int(input())
A = list(map(int, input().split()))

if gcd_of_array(A) == 1:
    print("YES")
else:
    print("NO")
