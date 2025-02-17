# 1. [Introduction To Doubly Linked List](https://www.codingninjas.com/studio/problems/introduction-to-doubly-linked-list_8160413?utm_source=youtube&utm_medium=affiliate&utm_campaign=Codestudio_Linkedlistseries&leftPanelTabValue=PROBLEM)

### Java Solution
```Java
public class Solution{
    public static Node constructDLL(int []arr) {
        Node head = null;
        for(int i=arr.length-1; i>=0; i--){
            Node node = new Node(arr[i]); // Create a node
            node.next = head; // asign node.next to head and node.prev is null
            if (head!=null){ // update the current head prev to new node
                head.prev = node;
            }
            head = node; // update head to point new node
         }
         return head;     
     }
}
// Time complexity: O(), Space complexity: O()
```
### Python Solution
```Python
class Solution:
    def constructDLL(self, arr):
        head = Node(arr[0])
        curr=head
        curr.prev=None
        for i in range(1, len(arr)):
            temp = Node(arr[i])
            curr.next=temp
            temp.prev=curr
            curr=curr.next
        return head
```

# 2. [Insert at end of Doubly Linked List](https://www.geeksforgeeks.org/problems/insert-a-node-in-doubly-linked-list/1)

### Solution
```Java
/*
class Node
{
	int data;
	Node next;
	Node prev;
	Node(int data)
	{
	    this.data = data;
	    next = prev = null;
	}
}*/

class GfG
{
    //Function to insert a new node at given position in doubly linked list.
    void addNode(Node head_ref, int pos, int data)
	{
	    Node newNode = new Node(data);
	    Node temp=head_ref;
	    for(int i=0; i<pos; i++){
    	      temp=temp.next;
	    }
	    newNode.prev=temp;
	    newNode.next=temp.next;
	    temp.next=newNode;
	}
}
// Time complexity: O(), Space complexity: O()
```

### Python Solution
```Python
class Solution:
    def addNode(self, head, p, x):
        node=Node(x)
        curr=head
        for i in range(1,p+1):
                curr=curr.next
        
        nxt=curr.next
        curr.next=node
        node.prev=curr
        node.next=nxt
        return head
```

# 3. [Delete Last Node of a Doubly Linked List](https://www.geeksforgeeks.org/problems/delete-node-in-doubly-linked-list/1)

### Solution
```Java
/*
Definition for doubly Link List Node
class Node
{
    int data;
    Node next;
    Node prev;
    Node(int x){
        data = x;
        next = null;
        prev = null;
    }
}
*/

class Solution {
    public Node deleteNode(Node head, int x) {
        // for first element to delete
        if (x==1){
            head=head.next;
            return head;
        }
        
        Node temp=head;
        for(int i=1; i<x; i++){
            temp=temp.next;
        }
        // for last element to delete
        if (temp.next==null){
            temp.prev.next=null;
            return head;
        }
        // delete element except first and last position
        temp.prev.next=temp.next;
        if (temp.next!=null)
            temp.next.prev=temp.prev;
        temp.prev=null;
        temp.next=null;
        return head;
    }
}

// Time complexity: O(n), Space complexity: O(1)
```

### Python Solution
```Python
class Solution:
    def delete_node(self, head, x):
        if (x==1):
            head=head.next
            head.prev=None
            return head
        temp=head
        for i in range(2, x):
            temp=temp.next
        if (temp.next.next is None):
            temp.next=None
        else:
            temp.next=temp.next.next
            temp.next.prev=temp
        return head
```

# 4. [Reverse A Doubly Linked List](https://www.codingninjas.com/studio/problems/reverse-a-doubly-linked-list_1116098?utm_source=striver&utm_medium=website&utm_campaign=a_zcoursetuf)

### Java Solution
```Java
public class Solution{
    public static Node reverseDLL(Node head){
        Node temp = null;
        Node current = head;
        /* swap next and prev for all nodes of
         doubly linked list */
        while (current != null) {
            temp = current.prev;
            current.prev = current.next;
            current.next = temp;
            current = current.prev;
        }
        // update head
        if (temp != null) {
            head = temp.prev;
        }
        return head;
    }
}
```

## Alternate Java Solution:
```Java
/*
class Node
{
    int data;
    Node next, prev;
    Node(int data)
    {
        this.data = data;
        this.next = null;
        this.prev = null;
    }
}

*/
public static Node reverseDLL(Node  head)
{
    Node front=head;
    Node rear=head;
    int size=0;
    while(rear.next!=null){
        size++;
        rear=rear.next;
    }
    /* swap data front and rear for all nodes of
         doubly linked list */
    for(int i=0; i<=(size/2); i++){
        int temp=front.data;
        front.data=rear.data;
        rear.data=temp;

        // Updating front and rear
        front=front.next;
        rear=rear.prev;
    }
    return head;
}
```

### Python Solution
```Python
class Solution:
    def reverseDLL(self, head):
        front=head
        rear=head
        length=0
        while(rear.next is not None):
            rear=rear.next
            length+=1
        
        for index in range((length//2)+1):
            front.data, rear.data=rear.data, front.data
            front=front.next
            rear=rear.prev
            index+=1
        
        return head
```

## Alternate Python Solution
```
class Solution:
    def reverseDLL(self, head):
        curr=head
        while(curr):
            curr.prev, curr.next=curr.next, curr.prev
            if not curr.prev:
                return curr
            curr=curr.prev
        return head
```
