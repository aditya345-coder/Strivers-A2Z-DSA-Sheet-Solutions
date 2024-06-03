# 1. [1 to N Without Loop](https://www.geeksforgeeks.org/problems/print-1-to-n-without-using-loops-1587115620/1)

## Java Solution:
```java
class Solution{
  public void printNos(int N){
        if (N<1){
            return;
        }
        printNos(N-1);
        System.out.print(N+" ");
  }
}
```

## Python Solution:
```python
from typing import List

def array(x):
    if (x==1):
        return [1]
    return array(x-1)+[x]

def printNos(x: int) -> List[int]: 
    return array(x)
```


# 2. [Print GFG n times](https://www.geeksforgeeks.org/problems/print-gfg-n-times/1)

## Java Solution:
```java
class Solution {

    void printGfg(int N) {
        if(N==0){
            return;
        }
        System.out.print("GFG ");
        printGfg(N-1);
    }
}
```

## Python Solution:
```python

```


# 3. [Print 1 To N Without Loop](https://www.geeksforgeeks.org/problems/print-1-to-n-without-using-loops-1587115620/1)

## Java Solution:
```java
class Solution
{
  public void printNos(int N){
        if (N==0){
            return;
        }
        printNos(N-1);
        System.out.print(N+" ");
  }
}
```

## Python Solution:
```python

```

# 4. [Print N to 1 without loop](https://www.geeksforgeeks.org/problems/print-n-to-1-without-loop/1)

## Java Solution:
```java
class Solution {

    void printNos(int N) {
        if (N==0){
            return;
        }
        System.out.print(N+" ");
        printNos(N-1);
    }
}
```

## Python Solution:
```python

```

# 5. [Sum of first n terms](https://www.geeksforgeeks.org/problems/sum-of-first-n-terms5843/1)

## Java Solution:
```java
class Solution {
    long sumOfSeries(long n) {
        if (n==0){
            long sum = n;
            return sum;
        }
        long sum = sumOfSeries(n-1);
        sum = sum + (long)Math.pow(n,3);
        return sum;
    }
}
```

## Python Solution:
```python

```

# 6. []()

## Java Solution:
```java

```

## Python Solution:
```python

```

# 7. []()

## Java Solution:
```java

```

## Python Solution:
```python

```

# 8. []()

## Java Solution:
```java

```

## Python Solution:
```python

```

# 9. []()

## Java Solution:
```java

```

## Python Solution:
```python

```
