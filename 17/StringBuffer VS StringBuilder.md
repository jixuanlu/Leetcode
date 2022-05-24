# 小猪猫快看
# StringBuffer
## Constructor
* ```
  StringBuffer s = new StringBuffer();
  // Construct an empty StringBuffer s, and initiallize the capacity to default "16" (s.capacity() == 16)
  ```
* ```
  StringBuffer s = new StringBuffer(20);
  // Construct an empty StringBuffer s, and initiallize the capacity to the input argument 20
  ```
* ```
  StringBuffer s = new StringBuffer("ThisIsAString");
  // Construct a StringBuffer s, and initiallize it to the input argument "ThisIsAString"
  ```
## Method
* | return value | signature |
  |--------------|-----------|
  | int | length() |
  | int | capacity() |
  | StringBuffer | append(String str) |
  | void | setCharAt(int i, char c) |
  | StringBuffer | delete(int startIndex, int endIndex) |
  | StringBuffer | deleteCharAt(int index) |
  | StringBuffer | insert(int offset, String str) |
  | StringBuffer | replace(int startIndex, int endIndex, String str) |
  | StringBuffer | reverse() |  
  | String | toString() |
</br>

# StringBuilder
## Constructor
* ```
  StringBuilder builder = new StringBuilder();
  // Construct an empty StringBuilder builder, and initiallize the capacity to default "16" (s.capacity() == 16)
  ```
* ```
  StringBuilder builder = new StringBuilder(20);
  // Construct an empty StringBuilder s, and initiallize the capacity to the input argument 20
  ```
* ```
  StringBuilder builder = new StringBuilder("ThisIsAString");
  // Construct a StringBuilder s, and initiallize it to the input argument "ThisIsAString"
  ```
## Method
* | return value | signature |
  |--------------|-----------|
  | int | length() |
  | int | capacity() |
  | StringBuilder | append(String str) |
  | void | setCharAt(int i, char c) |
  | StringBuilder | delete(int startIndex, int endIndex) |
  | StringBuilder | deleteCharAt(int index) |
  | StringBuilder | insert(int offset, String str) |
  | StringBuilder | replace(int startIndex, int endIndex, String str) |
  | StringBuilder | reverse() |  
  | String | toString() |
</br>

# Difference
* StringBuffer is synchronized i.e. thread safe. It means two threads can't call the methods of StringBuffer simultaneously. StringBuilder is non-synchronized i.e. not thread safe. It means two threads can call the methods of StringBuilder simultaneously.
