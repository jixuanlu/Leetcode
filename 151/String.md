# String 
```
String key = new String(array);    // String can be constructed by a char array
```


| return value | method | description |
| ------------ | ------ | ----------- |
| char | charAt(int index) | Returns the char value at the specified index. |
| String | concat(String str) | Concatenates the specified string to the end of this string. |
| int | length() | Returns the length of this string. |
| String | replace(char oldChar (String also works), char newChar (String also works)) | Returns a new string resulting from replacing all occurrences of oldChar in this string with newChar. |
| String[] | 	split(String regex) | Splits this string around matches of the given regular expression. |
| String | trim() | Returns a copy of the string, with leading and trailing whitespace omitted. |
| String | toUpperCase() | Converts all of the characters in this String to upper case using the rules of the default locale. |
| char[] | toCharArray() | Convert the string to a char array. |
| int | indexOf(String str) | Find the start index of the substring |  
| String | substring(int startIndex, int endIndex) | starting index is inclusive, ending index is exclusive | 
| String | valueOf(Object o) | converts different types of values into a string, the input argument includes: boolean, char, char[], int, long, float, double, object. 用法: String.valueOf(), 特定字符串不能使用此方法 |
| String | join(CharSequence delimiter, CharSequence... elements) | String.join(" < ", "Four", "Five", "Six", "Seven") Output: "Four < Five < Six < Seven"; This can also use String[] as input argument String.join("", strings) |
