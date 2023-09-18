## Integer.parseInt()

| Return Value | method | description |
| ------------ | ------ | ----------- |
| Integer | parseInt(String s) | This method parses the String argument as a signed decimal integer object. |
| Integer | parseInt(String s, int radix) | This method parses the String argument as a signed decimal integer object in the specified radix by the second argument. (把输入的字符串作为radix指定的进制形式parse成10进制) 例如 Integer.parseInt("A", 16) = 10; Integer.parseInt("11", 2) = 3 |

## Integer.toBinaryString()
| Return Value | method | description |
| ------------ | ------ | ----------- |
| String | toBinaryString(int num) | This method returns a string representation of the integer argument as an unsigned integer in base 2. (把一个10进制数转为32位的2进制数,对负数,会用补码表示)|
