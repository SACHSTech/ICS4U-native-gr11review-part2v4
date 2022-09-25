# Grade 11 Java Review Part 2

## Instructions
Program the solutions for each problem in a single `Utility.java` file in  `src/gr11review/part2 directory`.  You are required to:

### a) Code Solutions
* within a group of two or three, each of your coding to your own branch, code your solutions in VS Code.
* Each member must pick a problem from each section (Methods, FileIO, Array - One Dimensional 1 Loop, Array - One Dimensional 2 Loops, Two Dimensional Arrays)
* commit and push changes to appropriate development branches in github.
* merge tested and completed solutions to the main branch.
* use proper style conventions for variable names and comments.

### b) Test Solutions
* Create a test class `UtilityTest.java` in the `src/gr11review/part2` directory.
* With the concepts of the [Types of Tests](https://docs.google.com/document/d/1vkqcF0oocKygmTJXlBd0Izqau0to38rfG7u7gnBGw10/edit?usp=sharing), define test methods to thoroughly test the functionality of your solution methods. 
* Name your test methods using the name of the solution method + "Test" + test case #.  For example, if your solution method in `Utility.java` is called `abc()`, there should be corresponding test methods in `UtilityTest.java` called `abcTest1(), abcTest2(), abcTest3() ...` etc.
* tests methods should also be created by each member in their development branch and merged into the main branch.

## Problem Sets

### Methods


#### Methods 1

We'll say that a String is xy-balanced if for all the 'x' chars in the string, there exists a 'y' char somewhere later in the string. So "xxy" is balanced, but "xyx" is not. One 'y' can balance multiple 'x's. Return true if the given string is xy-balanced.

##### Examples
```
xyBalance("aaxbby") → true
xyBalance("aaxbb") → false
xyBalance("yaaxbb") → false
```

#### Methods 2
Given a string, return the sum of the numbers appearing in the string, ignoring all other characters. A number is a series of 1 or more digit chars in a row. (Note: Character.isDigit(char) tests if a char is one of the chars '0', '1', .. '9'. Integer.parseInt(string) converts a string to an int.)
**Signature** `public static int sumNumbers(String str)`

#### Examples
```
sumNumbers("abc123xyz") → 123
sumNumbers("aa11b33") → 44
sumNumbers("7 11") → 18
```

### File IO

#### File IO - Read 1
Write a method `longestWord(String filenametxt)` such that given the name of a file `filenametxt` that contains a single word on each line,  returns the longest word in the file.  
**Signature** `public static String longestWord(String filenametxt)`

#### Example
words.txt contains:  
```
Lorem
ipsum
dolor
sit
amet
consectetur
adipiscing 
elit
```
`longestWord("words.txt")` --> `"consectetur"`

#### File IO - Read 2
Write a method `alphaWord(String filenametxt)` such that given the name of a file `filenametxt` that contains a single word on each line,  returns the word that is alphabetically first.  
**Signature** `public static String alphaWord(String filenametxt)`

##### Example
words.txt contains:  
```
Lorem
ipsum
dolor
sit
amet
consectetur
adipiscing 
elit
```
`alphaWord("words.txt")` --> `"amet"`

### Arrays - One Dimensional, 1 Loop

#### Array 1 - One Dimensional
For each multiple of 10 in the given array, change all the values following it to be that multiple of 10, until encountering another multiple of 10. So {2, 10, 3, 4, 20, 5} yields {2, 10, 10, 10, 20, 20}.  
**Signature** `public static int[] tenRun(int[] nums)`

##### Examples
```
tenRun([2, 10, 3, 4, 20, 5]) → [2, 10, 10, 10, 20, 20]
tenRun([10, 1, 20, 2]) → [10, 10, 20, 20]
tenRun([10, 1, 9, 20]) → [10, 10, 10, 20]
```

#### Array 2 - One Dimensional
We'll say that an element in an array is "alone" if there are values before and after it, and those values are different from it. Return a version of the given array where every instance of the given value which is alone is replaced by whichever value to its left or right is larger.
public int[] notAlone(int[] nums, int val)  
**Signature** `public static int[] notAlone(int[] nums, int value)`

##### Examples
```
notAlone([1, 2, 3], 2) → [1, 3, 3]
notAlone([1, 2, 3, 2, 5, 2], 2) → [1, 3, 3, 5, 5, 2]
notAlone([3, 4], 3) → [3, 4]
```

### Arrays - One Dimensional, 2 Loops


#### Array 3 - One Dimensional - Two Loops
Given two arrays of ints sorted in increasing order, `outer` and `inner`, return true if all of the numbers in `inner` appear in `outer`. The best solution makes only a single "linear" pass of both arrays, taking advantage of the fact that both arrays are already in sorted order.  
**Signature** `public static boolean linearIn(int[] outer, int[] inner)`

##### Examples
```
linearIn([1, 2, 4, 6], [2, 4]) → true
linearIn([1, 2, 4, 6], [2, 3, 4]) → false
linearIn([1, 2, 4, 4, 6], [2, 4]) → true
```


#### Array 4 - One Dimensional - Two Loops
Given a non-empty array, return true if there is a place to split the array so that the sum of the numbers on one side is equal to the sum of the numbers on the other side.  
**Signature**  `public static boolean canBalance(int[] nums)`

##### Examples
```
canBalance([1, 1, 1, 2, 1]) → true
canBalance([2, 1, 1, 2, 1]) → false
canBalance([10, 10]) → true
```

### Arrays - Two Dimensional

#### Array 5 - Two Dimensional
Write a method that takes a 2D array and reverses all of the content in the 2D array. The last value should be the first, and the first value should be the last.  

**Signature** `public static int[][] reverse(int[][] arr)`

##### Example
`reverse({{1,2,3},{4,5,6},{7,8,9}})` returns
```
[9,8,7]
[6,5,4]
[3,2,1]
```

#### Array 6 - Two Dimensional 
Write a method that returns a portion of a 2D array based on a specified row and col.  
**Signature** `public static int[][] split(int[][] arr, int row, int col)`  

##### Example
For example, the call `split({{1,2,3},{4,5,6},{7,8,9}}, 1, 1)` would return all elements up to that point in the 2D array: 
```
[1,2]
[4,5]
```
