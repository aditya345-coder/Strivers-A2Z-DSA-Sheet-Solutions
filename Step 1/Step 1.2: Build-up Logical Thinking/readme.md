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

## Pattern 13
```
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
