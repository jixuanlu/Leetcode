# Method 1 Calculate Length

Loop through all the node to get the length of the linkedlist, then use the length minus the n value to get the node we need to remove. Use a variable temp move the previous node of the target node and remove it. 
## Code
```
class Solution {
    public ListNode removeNthFromEnd(ListNode head, int n) {
        int length = 0;
        ListNode temp = head;
        while(temp != null) {
            temp = temp.next;
            length++;
        }
        temp = head;
        int index = length - n;
        for(int i = 1; i < index; i++) 
            temp = temp.next;
        
        if(index == 0) return temp.next;
        
        if(temp.next == null) return null;
        else temp.next = temp.next.next;
        
        return head;
    }
}
```

# Method 2 Stack
loop through all the node and put each node into a stack. The nth node in the stack is the node we need to remove.
## Code
```
```
