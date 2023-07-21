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
# [Palindrome number](https://www.codingninjas.com/studio/problems/palindrome-number_624662?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)

## Solution:
```
n=int(input()) 
temp = n 
rev = 0
while temp !=0:
    rem = temp % 10
    rev = rev*10 + rem
    temp= temp//10
if (rev==n):
    print("true")
else:
    print("false")
```
# [GCD or HCF](https://www.codingninjas.com/studio/problems/hcf-and-lcm_840448?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

## Solution:
```
```

# [Check Armstrong ](https://www.codingninjas.com/studio/problems/check-armstrong_589?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)

## Solution:
```
n = int(input())
temp1 = n
temp2 = n
pwr = 0
armstrong_num = 0

while temp1 != 0:
    rem = temp1 % 10
    pwr = pwr + 1
    temp1 = temp1 // 10

while temp2 != 0:
    rem = temp2 % 10
    armstrong_num = armstrong_num + rem**pwr
    temp2 = temp2 // 10

if (armstrong_num == n):
    print("true")
else:
    print("false")
```
# [Print all Divisors]()

## Solution:
```
```
# [Check Prime](https://www.codingninjas.com/studio/problems/check-prime_624934?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf&leftPanelTab=0)

## Solution:
```
n = int(input())
count = 0
for i in range(1,int(sqrt(n)+1)):
    if (n==1):
        break
    if (n%i==0):
        count = count + 1
if (count == 1):
    print("YES")
else:
    print("NO")
```
