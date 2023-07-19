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
# [Reverse Bits](https://www.codingninjas.com/studio/problems/reverse-bits_2181102?leftPanelTab=0)

## Solution:
```
def reverseBits(n):
    return int('{:032b}'.format(n)[::-1], 2) # converting number into binary then reversing the binary number and specifying the base of binary number(2).
```
## Alternate Solution
```
def reverseBits(n):
    return int(bin(n).replace('0b','').zfill(32)[::-1],2)
```
