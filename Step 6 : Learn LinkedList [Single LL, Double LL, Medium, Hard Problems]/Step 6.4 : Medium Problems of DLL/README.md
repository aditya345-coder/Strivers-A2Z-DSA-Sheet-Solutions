# 1. [Delete all occurrences of a key in DLL](https://www.geeksforgeeks.org/problems/delete-all-occurrences-of-a-given-key-in-a-doubly-linked-list/1)

## Solution:
```Java
class Solution {
    static Node deleteAllOccurOfX(Node head, int x) {
        if (head.data==x){
            head=head.next;
            head.prev=null;
        }
        Node temp=head;
        while(temp.next!=null){
            if (temp.data==x){
                if (temp.next!=null)
                    temp.next.prev=temp.prev;
                if (temp.prev!=null)
                    temp.prev.next=temp.next;
                if (temp.prev==null){
                    head=head.next;
                }
            }
            temp=temp.next;
        }
        if (temp.data==x){
            temp.prev.next=null;
        }
        return head;
    }
}
```
## Alternate Solution:
```Java
/* Structure of Doubly Linxed List
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
class Solution {
    static Node deleteAllOccurOfX(Node head, int x) {
        // If there is only one node
        if (head.next==null){
            if (head.data==x){
                head = null;
            }
            return head;
        }
        // if first node has value x
        while (head!=null && head.data==x){
            head = head.next;
        }
    
        Node temp = head;
        while(temp!=null){
            if (temp.data == x){

                // Checxing if temp.next element is not null (if last node)
                if (temp.next!=null){
                    temp.next.prev = temp.prev;
                }
                // Checxing if temp.prev element is not null
                if (temp.prev!=null){
                    temp.prev.next = temp.next;
                }
            }
            temp=temp.next;
        }
        return head;
    }
}
```

# [Find pairs with given sum in DLL](https://www.geeksforgeeks.org/problems/find-pairs-with-given-sum-in-doubly-linked-list/1)

## Solution:
```Java
class Solution {
    public static ArrayList<ArrayList<Integer>> findPairsWithGivenSum(int target, Node head) {
        ArrayList<ArrayList<Integer>> arr = new ArrayList<ArrayList<Integer>>();
        Node front = head;
        Node rear = head;
        while(rear.next!=null){
            rear=rear.next;
        }
        while(front.data<rear.data){
            if ((front.data+rear.data)==target){
                ArrayList<Integer> temp = new ArrayList<Integer>();
                temp.add(front.data);
                temp.add(rear.data);
                arr.add(temp);
                rear=rear.prev;
            }
            else if ((front.data+rear.data)>target){
                rear=rear.prev;
            }else{
                front=front.next;
            }
        }
        return arr;
    }
}
```

# [Remove duplicates from sorted DLL] (https://www.geeksforgeeks.org/problems/remove-duplicates-from-a-sorted-doubly-linked-list/1)

## Solution:
```Java
class Solution{
    Node removeDuplicates(Node head){
        Node current=head;
        Node temp=null;
        while(current.next!=null){
            if (current.data==current.next.data){
                temp = current.next.next; // to store the deleted element address
                current.next= temp;
                if (current.next!=null)
                    temp.prev=current;
            }
            else{
                current=current.next;
            }
        }
        return head;
    }
}
```
