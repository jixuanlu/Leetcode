# Method 1 Recursion
Base case, if list1 == null return list2; if list2 == null return list1. In the recursive part, we compare the list1.val and list2.val, if list1 is small we make list1 as the head and call the functio itself, make list1.next as list1; list2 as list2 and merge, and vice versa. After finish merge, return the smaller node. 
## Code
```
class Solution {
    public ListNode mergeTwoLists(ListNode list1, ListNode list2) {
        if(list1 == null) 
            return list2;
        if(list2 == null)
            return list1;
        if(list1.val < list2.val) {
            list1.next = mergeTwoLists(list1.next, list2);
            return list1;
        }
        else {
            list2.next = mergeTwoLists(list2.next, list1);
            return list2;
        }
    }
}
```
