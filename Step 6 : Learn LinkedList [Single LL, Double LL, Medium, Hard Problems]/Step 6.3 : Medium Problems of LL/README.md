# 1. [Middle Of Linked List](https://www.codingninjas.com/studio/problems/middle-of-linked-list_973250?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Java Solution: Time Complexity: O() Space Complexity: O()
```Java
public class Solution{
    public static Node findMiddle(Node head){
        int size = 0;
        Node temp = head;
        while(temp!=null){
            temp = temp.next;
            size+=1;
        }
        temp = head;
        for(int i=0; i<(size/2); i++ ){
            temp = temp.next;
        }
        return temp;

    }
}
```

### Python Solution: Time Complexity: O() Space Complexity: O()
```Python
class Solution:
    def middleNode(self, head: Optional[ListNode]) -> Optional[ListNode]:
        curr=head; length=0
        while(curr is not None):
            curr=curr.next
            length+=1
        
        temp=head
        for i in range(0,(length//2)):
            temp=temp.next
        
        return temp
```

### Alternate Solution
```Python
class Solution:
    def middleNode(self, head: Optional[ListNode]) -> Optional[ListNode]:
        slow=head; fast=head
        while fast and fast.next:
            slow=slow.next
            fast=fast.next.next
        
        return slow
```

# 2. [Reverse a LinkedList [Iterative]]()

### Solution: Time Complexity: O() Space Complexity: O()
```Python
class Solution:
    def reverseList(self, head: Optional[ListNode]) -> Optional[ListNode]:
        curr=head; prev=None
        while(curr is not None):
            next=curr.next
            curr.next=prev
            prev=curr
            curr=next
        return prev
```

# 3. [Reverse a LL [Recursive]]()

### Solution: Time Complexity: O() Space Complexity: O()
```Java
```

# 4. [Detect a loop in LL]()

### Solution: Time Complexity: O() Space Complexity: O()
```Java
```

# 5. [Find the starting point in LL]()

### Solution: Time Complexity: O() Space Complexity: O()
```Java
```

# 6. [Length of Loop in LL]()

### Solution: Time Complexity: O() Space Complexity: O()
```Java
```

# 7. [Check if LL is palindrome or not]()

### Solution: Time Complexity: O() Space Complexity: O()
```Java
```

# 8. [Segrregate odd and even nodes in LL]()

### Solution: Time Complexity: O() Space Complexity: O()
```Java
```

# 9. [Remove Nth node from the back of the LL]()

### Solution: Time Complexity: O() Space Complexity: O()
```Java
```

# 10. [Delete the middle node of LL]()

### Solution: Time Complexity: O() Space Complexity: O()
```Java
```

# 11. [Sort LL]()

### Solution: Time Complexity: O() Space Complexity: O()
```Java
```

# 12. [Sort a LL of 0's 1's and 2's by changing links]()

### Solution: Time Complexity: O() Space Complexity: O()
```Java
```

# 13. [Find the intersection point of Y LL]()

### Solution: Time Complexity: O() Space Complexity: O()
```Java
```

# 14. [Add 1 to a number represented by LL]()

### Solution: Time Complexity: O() Space Complexity: O()
```Java
```

# 15. [Add 2 numbers in LL](https://leetcode.com/problems/add-two-numbers/description/)

### Solution: Time Complexity: O() Space Complexity: O()
```Java
class Solution {
    public ListNode addTwoNumbers(ListNode l1, ListNode l2) {
        ListNode head1 = l1;
        ListNode head2 = l2;
        ListNode result = new ListNode();
        ListNode head=result;
        int carry = 0;
        while(head1!=null || head2!=null || carry!=0){
            int sum=0;
            sum = head1!=null?head1.val:0;
            sum += head2!=null?head2.val:0;
            sum = sum+carry;
            carry = sum/10;
            result.next= new ListNode(sum%10);
            result=result.next;    
            if (head1!=null){
                head1=head1.next;
            }
            if (head2!=null){
                head2=head2.next;
            }
        }
        return head.next;
    }
}
```



