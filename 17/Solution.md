# Method 1 recursion
  Inside the letterCombinations():</br>
  * Consider the specical cases length == 0.</br>
  * Create a List<String> as the result list.</br>
  * Create a HashMap<Character, String> as the hash table to store all the letters represent each button.</br>
  * We go to the recursive function to add all the combinations to the list, After finished return the list.</br>

  Inside the recursive function:</br>

  * We start from index 0, call the recursive function itself until the it loop through all the digit, when the index == digits.length, stop and add the current combination to the combinations list.</br>
  * For each recursive call, loop through all the letters find from hashMap by the current digit. And add the current letter to the current combination.</br>
  * Inside loop of the letter call the recursive function.</br>
  * After return from the recursive function, delete the current letter to get ready for the next loop.</br>
 
 By doing this, we can loop through all the letters for the current dight, and for each letters recursively loop all the letters for the next digit, until the last one, and add each combination to the combinations list.
