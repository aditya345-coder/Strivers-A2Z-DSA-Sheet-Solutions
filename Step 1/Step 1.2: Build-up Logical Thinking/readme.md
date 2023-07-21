# Patterns

## [Pattern 12](https://practice.geeksforgeeks.org/problems/double-triangle-pattern-1662664259/1?utm_source=youtube&utm_medium=collab_striver_ytdescription&utm_campaign=pattern_12)
```
1                 1
1 2             2 1
1 2 3         3 2 1
1 2 3 4     4 3 2 1
1 2 3 4 5 5 4 3 2 1
```
### Code:
```
class Solution:
    def printTriangle(self, N):
        for i in range(N):
            for j in range(0,i+1):
                print(j+1,end=" ")
            for k in range(2*(N-i-1),0,-1):
                print(" ",end=" ")
            for l in range(i,-1,-1):
                print(l+1,end=" ")
            print()
```

## [Pattern 13](https://practice.geeksforgeeks.org/problems/triangle-pattern-1661718712/1?utm_source=youtube&utm_medium=collab_striver_ytdescription&utm_campaign=pattern_13)
```
1 
2 3 
4 5 6 
7 8 9 10 
11 12 13 14 15
```
### Code:
```
```
## [Pattern 14](https://practice.geeksforgeeks.org/problems/triangle-pattern-1662284916/1?utm_source=youtube&utm_medium=collab_striver_ytdescription&utm_campaign=pattern_14)
```
A
AB
ABC
ABCD
ABCDE
```
### Code:
```
class Solution:
    def printTriangle(self, N):
        for i in range(1,N+1):
            for j in range(97, 97+i):
                print(chr(j).upper(), end="")
            print()
```
## [Pattern 15](https://practice.geeksforgeeks.org/problems/triangle-pattern-1662285196/1?utm_source=youtube&utm_medium=collab_striver_ytdescription&utm_campaign=pattern_15)
```
ABCDE
ABCD
ABC
AB
A
```
### Code:
```
class Solution:
    def printTriangle(self, N):
        for i in range(1, N+1):
            for j in range(97, 97+(N-i)+1):
                print(chr(j).upper(),end="")
            print()
```
## [Pattern 16](https://practice.geeksforgeeks.org/problems/triangle-pattern-1662285334/1?utm_source=youtube&utm_medium=collab_striver_ytdescription&utm_campaign=pattern_16)
```
A
BB
CCC
DDDD
EEEEE
```
### Code:
```

```

## [Pattern 17](https://practice.geeksforgeeks.org/problems/triangle-pattern-1662285911/1?utm_source=youtube&utm_medium=collab_striver_ytdescription&utm_campaign=pattern_17)
```
   A
  ABA
 ABCBA
ABCDCBA
```
### Code:
```
class Solution:
    def printTriangle(self, N):
        for i in range(1, N+1):
            for j in range(N-i,0,-1):
                print(" ",end="")
            for k in range(97, 97+i):
                print(chr(k).upper(),end="")
            if (i>1):
                for l in range(97+i-1,97,-1):
                    print(chr(l-1).upper(),end="")
            print()
```
## [Pattern 18]()
```
```
### Code:
```
```
## [Pattern 19](https://practice.geeksforgeeks.org/problems/double-triangle-pattern/1?utm_source=youtube&utm_medium=collab_striver_ytdescription&utm_campaign=pattern_19)
```
**********
****  ****
***    ***
**      **
*        *
*        *
**      **
***    ***
****  ****
**********
```
### Code:
```
class Solution:
    def printTriangle(self, N):
        for i in range(0,N):
            for j in range(N,i,-1):
                print("*",end="")
            if (i>0):
                for k in range(i):
                    print(" ",end=" ")
            for l in range(N,i,-1):
                print("*",end="")
            print()
        for i in range(0,N):
            for j in range(i+1):
                print("*",end="")
            if (i<N-1):
                for k in range(N*2-2-i, i, -1):
                    print(" ",end="")
            for l in range(i+1):
                print("*",end="")
            print()
```
## [Pattern 20](https://practice.geeksforgeeks.org/problems/double-triangle-pattern-1662287416/1?utm_source=youtube&utm_medium=collab_striver_ytdescription&utm_campaign=pattern_20)
```
*        *
**      **
***    ***
****  ****
**********
****  ****
***    ***
**      **
*        *
```
## Code
```
class Solution:
    def printTriangle(self, N):
        for i in range(N):
            for j in range(i+1):
                print("*",end="")
            for k in range(N-1,i,-1):
                print(" ",end=" ")
            for l in range(i+1):
                print("*",end="")
            print()
        for i in range(N-1):
            for j in range(N-1,i,-1):
                print("*",end="")
            for k in range(i+1):
                print(" ",end=" ")
            for l in range(N-1,i,-1):
                print("*",end="")
            print()
```
