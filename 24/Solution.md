# Method 1 Recursion
* Base case, if head == null or head.next == null, directly return head, no need to swap. For recursive part, we separate each swap to one recursion, 
make the head.next as the newHead.(Because after swap, this node will move in front of the previous head as a newHead for the current recursion also as the return value) 
Then we call the swapPair() function itself the input argument will be the newHead.next which is head of the rest LinkedList except the current two node that is swapping. 
And make the return value be the next node of head. After that make head be the next node of the newHead, and return newHead. </br></br>
* By doing this we swap only the first two nodes, and make the rest of swap as a subproblem, use its return value as the next node after we swap. Then this questions will be 
solved recursively.
## Code
```
class Solution {
    public ListNode swapPairs(ListNode head) {
        if(head == null || head.next == null)
            return head;
        ListNode newHead = head.next;
        head.next = swapPairs(newHead.next);
        newHead.next = head;
        return newHead;
    }
}
```
