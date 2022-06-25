~~~
class Solution {
    public int strStr(String haystack, String needle) {
        int[] next = buildNext(needle);
        int i = 0; //主串
        int j = 0; //字串
        while(i < haystack.length()) {
            if(haystack.charAt(i) == needle.charAt(j)) {
                i++;
                j++;
            }
            else if(j > 0) 
                j = next[j - 1];
            else
                i++;

            if(j == needle.length()) 
                return i - j;
        }
        return -1;
    }

    public int[] buildNext(String sub) {
        int n = sub.length();
        int[] next = new int[n];
        int prefixLen = 0;
        int i = 1;

        next[0] = 0;
        while(i < n){
            if(sub.charAt(prefixLen) == sub.charAt(i)) {
                prefixLen += 1;
                next[i] = prefixLen;
                i++;
            }
            else {
                if(prefixLen == 0) {
                    next[i] = 0;
                    i++;
                }
                else
                    prefixLen = next[prefixLen - 1];
            }
        }
        return next;
    }
}
~~~
