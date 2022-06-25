# KMP
This question use the property of the next array in KMP algorithm, we calculate the next array for this String and use an if statement 
to justify whether this String is repeated by a sub String. 
## Code
~~~
class Solution {
    public boolean repeatedSubstringPattern(String s) {
        int[] next = buildNext(s); 
        int n = s.length();

        if(n == 0)
            return false;

        if(n > 0 && next[n - 1] > 0 && n % (n - next[n - 1]) == 0)
            return true;
        return false;
    }

    public int[] buildNext(String s) {
        int n = s.length();
        int[] next = new int[n];
        int prefixLen = 0;
        int i = 1;

        next[0] = 0;
        while(i < n) {
            if(s.charAt(prefixLen) == s.charAt(i)) {
                prefixLen += 1;
                next[i] = prefixLen;
                i++;
            }
            else {
                if(prefixLen == 0) {
                    next[i] = 0;
                    i++;
                }
                else {
                    prefixLen = next[prefixLen - 1];
                }
            }
        }
        return next;
    }
}
~~~
