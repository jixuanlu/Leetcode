# Method 1 HashTable

## Code 
~~~
class Solution {
    public boolean canConstruct(String ransomNote, String magazine) {
        int[] record = new int[26];
        for(char c : ransomNote.toCharArray()) {
            record[c - 'a'] += 1;
        }
        for(char c : magazine.toCharArray()) {
            record[c - 'a'] -= 1;
        }
        for(int i : record) {
            if(i > 0)
                return false;
        }
        return true;
    }
}
~~~

Similar question: 383
