# [Count Digits](https://www.codingninjas.com/studio/problems/count-digits_8416387?leftPanelTab=0)

## Solution
```
def countDigits(n: int) -> int:
    temp = n
    count = 0
    while temp !=0:
        rem = temp%10
        temp = temp//10
        if (rem == 0):
            continue
        if (n%rem==0):
            count = count + 1
    return count
```
