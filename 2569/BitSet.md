~~~
BitSet bset = new BitSet(size);

Constructor:

BitSet()
// Creates a new bit set.

BitSet(int nbits)
// Creates a bit set whose initial size is large enough to explicitly
// represent bits with indices in the range 0 through nbits-1.
~~~

| return type | method | Description |
| ----------- | ------ | ----------- |
| int | cardinality() | Returns the number of bits set to true in this BitSet. |
| void | clear() | Sets all of the bits in this BitSet to false. |
| void | clear(int bitIndex) | Sets the bit specified by the index to false. |
| void | clear(int fromIndex, int toIndex) | Sets the bits from the specified fromIndex (inclusive) to the specified toIndex (exclusive) to false. |
| boolean | equals(Object obj) | Compares this object against the specified object. |
| void | flip(int bitIndex) | Sets the bit at the specified index to the complement of its current value. |
| void | flip(int fromIndex, int toIndex) | Sets each bit from the specified fromIndex (inclusive) to the specified toIndex (exclusive) to the complement of its current value. |
| boolean | get(int bitIndex) | Returns the value of the bit with the specified index. |
| BitSet | get(int fromIndex, int toIndex) | Returns a new BitSet composed of bits from this BitSet from fromIndex (inclusive) to toIndex (exclusive). |
| boolean | isEmpty() | Returns true if this BitSet contains no bits that are set to true. |
| int | length() | Returns the "logical size" of this BitSet: the index of the highest set bit in the BitSet plus one. |
| void | set(int bitIndex) | Sets the bit at the specified index to true. |
| void | set(int bitIndex, boolean value) | Sets the bit at the specified index to the specified value. |
| int	| size() | Returns the number of bits of space actually in use by this BitSet to represent bit values. |
| byte[] | toByteArray() | Returns a new byte array containing all the bits in this bit set. |
| long[] | toLongArray() | Returns a new long array containing all the bits in this bit set. |
| String | toString() | Returns a string representation of this bit set. |
