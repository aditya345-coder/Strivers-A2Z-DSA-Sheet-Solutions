# 1. [Implement Stack using Arrays](https://www.geeksforgeeks.org/problems/implement-stack-using-array/1)

## Solution:
```Java
class MyStack {
    private int[] arr;
    private int top;

    public MyStack() {
        arr = new int[1000];
        top = -1;
    }

    public void push(int x) {
        if (top>=1000){
           return;        
        }
        top++;
        arr[top] = x;
        
    }

    public int pop() {
        if (top==-1){
            return -1;
        }
        int result = arr[top];
        top--;
        return result;
    }
}
```

# 2. [Implement Queue using Arrays](https://www.geeksforgeeks.org/problems/implement-queue-using-array/1)

## Solution:
```Java
class MyQueue {

    int front, rear;
	int arr[] = new int[100005];

    MyQueue()
	{
		front=0;
		rear=0;
	}
	
	//Function to push an element x in a queue.
	void push(int x)
	{
	    if (rear>=100005){
	        return;
	    }
	    if (rear==arr.length && front!=0){
	        rear=0;
	    }
	    arr[rear]=x;
	    rear++;
	} 

    //Function to pop an element from queue and return that element.
	int pop()
	{
	    if (front==rear){
	        return -1;
	    }
	    
	    int deleteElement=arr[front];

		front++;
		return deleteElement;
	} 
}
```

# 3. []()

## Solution:
```Java
```

# 4. []()

## Solution:
```Java
```

# 5. [Implement stack using Linkedlist](https://www.geeksforgeeks.org/problems/implement-stack-using-linked-list/1)

## Solution:
```Java
class MyStack 
{
    // class StackNode {
    //     int data;
    //     StackNode next;
    //     StackNode(int a) {
    //         data = a;
    //         next = null;
    //     }
    // }   
    StackNode top;
    
    //Function to push an integer into the stack.
    void push(int a) 
    {
        StackNode sNode = new StackNode(a);
        if (top==null){
            top=sNode;
            return;
        }
        sNode.next=top;
        top=sNode;
        
    }

    //Function to remove an item from top of the stack.
    int pop() 
    {
        if (top==null){
            return -1;
        }
        int data = top.data;
        top=top.next;
        return data;
    }
}
```

# 6. []()

## Solution:
```Java
```

# 7. [Check for balanced paranthesis](https://leetcode.com/problems/valid-parentheses/description/)

## Solution:
```Java
class Solution {
    public boolean isValid(String s) {
        HashMap<Character, Character> map = new HashMap<>();
        map.put('(', ')');
        map.put('[', ']');
        map.put('{', '}');
        Stack<Character> stack = new Stack<Character>();
        char [] str = s.toCharArray();
        for(int i=0; i<str.length; i++){
            // When you encounter an opening bracket, push it to the top of the stack.
            if (map.containsKey(str[i])){
                stack.push(str[i]);
            }
            else{
                // When you encounter a closing bracket, check if the top of the stack was the opening for it. 
                // If yes, pop it from the stack. Otherwise, return false.
                if (stack.isEmpty()){
                    return false;
                }
                char openingBracket=stack.pop();
                char closingBracket=map.get(openingBracket);
                if (closingBracket!=str[i]){
                    return false;
                }
            }
        }
        return stack.isEmpty();
    }
}
```

## Alternate Solution:
```Java
class Solution {
    public boolean isValid(String s) {
        Stack<Character> stack = new Stack<Character>();
        char [] str = s.toCharArray();
        if (str.length==1){
            return false;
        }
        for(int i=0; i<str.length; i++){
            if (str[i]=='(' || str[i]=='[' || str[i]=='{'){
                stack.push(str[i]);
            }
            else if (!stack.isEmpty() && (str[i]==')' || str[i]==']' || str[i]=='}')){
                if ((stack.peek()=='(' && str[i]==')') || (stack.peek()=='[' && str[i]==']') || (stack.peek()=='{' && str[i]=='}')){
                    stack.pop();
                }
                else{
                    return false;
                }
            }
            else{
                return false;
            }
        }
        if (stack.size()==0){
            return true;
        }
        return false;
    }
}
```

# 8. [Implement Min Stack](https://leetcode.com/problems/min-stack/description/)

## Solution:
```Java
class MinStack {
    ArrayList<Integer> stack;
    public MinStack() {
        stack = new ArrayList<>(); 
    }
    
    public void push(int val) {
        stack.add(val);
    }
    
    public void pop() {
        stack.remove(stack.size()-1);
    }
    
    public int top() {
        return stack.get(stack.size()-1);
    }
    
    public int getMin() {
        return Collections.min(stack);
    }
}
```
