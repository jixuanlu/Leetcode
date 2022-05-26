# Method 1 Stack
If meet "(" or "[" or "{" put the character into a stack. If meet ")" or "]" or "}", check whether the top node in the stack is the correspond character. If yes pop the first node, else return false. After loop through all the character, if the stack is empty, that means all the character are paired, return true else return false.
## Code
```
class Solution {
    public boolean isValid(String s) {
        int n = s.length();
        Deque stack = new LinkedList();
        for(int i = 0; i < n; i++) {
            if(s.charAt(i) == '(') stack.addFirst("(");
            else if(s.charAt(i) == '[') stack.addFirst("[");
            else if(s.charAt(i) == '{') stack.addFirst("{");
            else if(s.charAt(i) == ')') {
                if(!stack.isEmpty() && stack.getFirst() == "(") stack.pollFirst();
                else return false;
            }
            else if(s.charAt(i) == ']') {
                if(!stack.isEmpty() && stack.getFirst() == "[") stack.pollFirst();
                else return false;
            }
            else {
                if(!stack.isEmpty() && stack.getFirst() == "{") stack.pollFirst();
                else return false;
            }
        }
        if(stack.isEmpty() == true) return true;
        else return false;
    }
}
```

# Method 2 Eliminate Pairs
Replace all the pairs "()", "[]", "{}" to empty string "". If the last string is empty return ture else return false.
## Code
```
# Python
class Solution(object):
    def isValid(self, s):
        while "()" in s or "[]" in s or "{}" in s:
            s = s.replace("()", "")
            s = s.replace("[]", "")
            s = s.replace("{}", "")
        return s == ""
```
