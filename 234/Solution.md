# Method 1 List
* Put the LinkedList into an arrayList then use double pointer.
## Code
```
class Solution {
    public boolean isPalindrome(ListNode head) {
        ListNode temp = head;
        List<Integer> arr = new ArrayList<Integer>();
        while(temp != null) {
            arr.add(temp.val);
            temp = temp.next;
        }
        int n = arr.size();
        int i = 0, j = n-1;
        while(i<j) {
            if(arr.get(i) != arr.get(j))
                return false;
            i++;
            j--;
        }
        return true;
    }
}
```
</br>

# Method 2 Recursion

## Code 
```

```
