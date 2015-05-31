# Glossary

## combination
A selection of contiguous or non-contiguous elements from a collection. The ordering of the elements is not important. Contrast this with "subsequence," where the ordering of the elements must be from left to right.

For example, the string `"abcd"` has the following combinations:

```java
""
"a"
"b"
"c"
"d"
"ab" or "ba"
"ac" or "ca"
"ad" or "da"
"bc" or "cb"
"bd" or "db"
"cd" or "dc"
"abc" or "acb" or "bac" or "bca" or "cab" or "cba"
"abd" or "adb" or "bad" or "bda" or "dab" or "dba"
"acd" or "adc" or "cad" or "cda" or "dac" or "dca"
"bcd" or "bdc" or "cbd" or "cdb" or "dbc" or "dcb"
"abcd" or "abdc" or "acbd" (...and so on)
```

## composite number
An integer greater than 1, which is divisible by an integer other than 1 and itself.

For example, the first 10 composite numbers are `[4, 6, 8, 9, 10, 12, 14, 15, 16, 18]`.

## Fibonacci number
A sequence of numbers, `f(n)`, defined by the following recurrence:

```java
f(n) = f(n - 1) + f(n - 2)    for n > 2
f(2) = 1
f(1) = 1
```

## lexicographical
The natural order of characters in an alphabet.

For example, `"cat"` comes before `"train"` lexicographically and after `"car"` lexicographically.

## maximum
The largest value in a collection.

For example, the largest value in `[1, 44, 39, 2, 39, 18]` is `44`.

## minimum
The smallest value in a collection.

For example, the smallest value in `[1, 44, 39, 2, 39, 18]` is `1`.

## permutation
An ordering of elements in a collection.

For example, the permutations of `"abcd"` are:

```java
"abcd"
"abdc"
"acbd"
"acdb"
"adbc"
"adcb"
"bacd"
"badc"
"bcad"
"bcda"
"bdac"
"bdca"
"cabd"
"cadb"
"cbad"
"cbda"
"cdab"
"cdba"
"dabc"
"dacb"
"dbac"
"dbca"
"dcab"
"dcba"
```

## prime number
An integer greater than 1, which is divisible only by 1 and itself.

For example, the first 10 prime numbers are `[2, 3, 5, 7, 11, 13, 17, 19, 23, 29]`.

## subarray
A slice of contiguous elements in an array.

For example, the array `[1, 2, 3, 4]` has the following subarrays:

```java
[]
[1]
[2]
[3]
[4]
[1, 2]
[2, 3]
[3, 4]
[1, 2, 3]
[2, 3, 4]
[1, 2, 3, 4]
```

## subsequence
A selection of contiguous or non-contiguous elements from a collection, in order from left to right.

For example, the string `"abcd"` has the following subsequences:

```java
""
"a"
"b"
"c"
"d"
"ab"
"ac"
"ad"
"bc"
"bd"
"cd"
"abc"
"abd"
"acd"
"bcd"
"abcd"
```

## substring
A slice of contiguous characters in a string.

For example, the string `"abcd"` has the following substrings:

```java
""
"a"
"b"
"c"
"d"
"ab"
"bc"
"cd"
"abc"
"bcd"
"abcd"
```
