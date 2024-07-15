# 1. []()

## Solution:
```Java
```

# 2. [50. pow(x, n)](https://leetcode.com/problems/powx-n/description/)

## Solution:
```Java
```

# 3. []()

## Solution:
```Java
```

# 4. []()

## Solution:
```Java
```

# 5. [Reverse a Stack](https://www.geeksforgeeks.org/problems/reverse-a-stack/1)

## Solution:
```Java
class Solution{
    static void reverse(Stack<Integer> s){
        if (s.isEmpty()){
            return;
        }
        int top=s.pop();
        reverse(s);
        insertAtBottom(s, top);
        
    }
    static void insertAtBottom(Stack<Integer> s, int top){
        if (s.empty()){
            s.push(top);
        }
        else{
            int value=s.pop();
            insertAtBottom(s, top);
            s.push(value);
        }
    }
}
```
