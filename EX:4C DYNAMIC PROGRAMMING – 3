# EX:4C DYNAMIC PROGRAMMING – 3

### DATE:

## AIM:
To find the length of the longest palindromic subsequence from the given sequence.

## ALGORITHM:

1. Reverse the input string to get a second string s2.
2. Initialize a 2D memoization table dp with -1.
3. Define a recursive function lps(s1, s2, n1, n2) to find the LCS of s1 and s2.
4. If either n1 or n2 is 0, return 0 (base case).
5. If dp[n1][n2] is already computed, return it.
6. If characters match, store 1 + lps(s1, s2, n1-1, n2-1) in dp[n1][n2].
7. If not, store the max of lps(s1, s2, n1-1, n2) and lps(s1, s2, n1, n2-1).
8. Return the value at dp[n1][n2] which is the LPS length.

## PROGRAM:

```
# Program to implement to find the length of the longest palindromic subsequence in it.
# Developed by: SWATHI D
# Register Number: 212222230154
```
```

dp = [[-1 for i in range(1001)]for j in range(1001)]
def lps(s1, s2, n1, n2):
    if (n1 == 0 or n2 == 0):
        return 0
    if (dp[n1][n2] != -1):
        return dp[n1][n2]
    if (s1[n1 - 1] == s2[n2 - 1]):
        dp[n1][n2] = 1 + lps(s1, s2, n1 - 1, n2 - 1)
        return dp[n1][n2]
    else:
        dp[n1][n2] = max(lps(s1, s2, n1 - 1, n2), lps(s1, s2, n1, n2 - 1))
        return dp[n1][n2]
seq = input()
n = len(seq)
s2 = seq
s2 = s2[::-1]
print(f"The length of the LPS is",lps(s2, seq, n, n))
```

## OUTPUT:

![image](https://github.com/user-attachments/assets/1905213d-a1f8-449d-84bc-fcbbd1d7812e)

## RESULT:
Thus the program was executed successfully for finding the length of longest palindromic string.
