# HashMap
```
class Solution {
    public int[] intersect(int[] nums1, int[] nums2) {
        // Make nums1 be the smaller array
        if (nums1.length > nums2.length) {
            return intersect(nums2, nums1);
        }

        Map<Integer, Integer> set1 = new HashMap<>();

        for(int i : nums1) {
            if(!set1.containsKey(i)) {
                set1.put(i, 1);
            }
            else {
                int value = set1.get(i);
                value ++;
                set1.replace(i, value);
            }
        }
        
        int[] intersection = new int[nums1.length];
        int index = 0;
        for(int i : nums2) {
            if(set1.containsKey(i)) {
                if(set1.get(i) > 0) {
                    int value = set1.get(i);
                    value --;
                    
                    // Once a value become 0 remove directly
                    if(value == 0)
                        set1.remove(i);
                    else
                        set1.replace(i, value);

                    intersection[index++] = i;  
                }
            }
        }
        return Arrays.copyOfRange(intersection, 0, index);
    }
}
```
Only use int[] array rather than List<Integer>, don't need convert List t array, this will decrease the running time. Also after a value become to 0 remove this pair directly will decrease the memory, also, choose the smaller length of two num to initiallize the array will decrease memory too.

# Convert Integer List to int[]
```
int[] array = ans.stream().mapToInt(i->i).toArray();
```
