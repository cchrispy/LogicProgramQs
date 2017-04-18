# Logic or Programming questions
List of logic puzzles or programming questions that may show up in interviews

## Logic puzzles
#### The horses problem
There are 25 horses and your goal is to find the fastest 3 horses. You can race horses 5 at a time and compare their speeds relative to each other. How many races are needed to figure out the fastest 3 horses?

#### The 12 ball problem
There are 12 balls. All the balls appear identical to each other, but one of them has a different weight. How many weighings with a balance scale is needed to figure out which ball is the counterfeit AND determine if it's heavier or lighter than the other 11 balls?

#### The bucket problem
You have a 13 gallon bucket, an 18 gallon bucket, and an endless supply of water. You need to measure out exactly 1 gallon of water, using only these tools. How?

#### The locker problem
There are 100 lockers and 100 students. When a student visits a locker he will open it if it's closed, or he will close it if it's open. All lockers are initially closed. Student 1 visits every locker (so he will open them all). Student 2 visits every other locker (so he will close the 2nd, 4th, 6th...). Student 3 visits every third locker (so he will change the state of the 3rd, 6th, 9th...). This continues until all 100 students have had a turn with the lockers. Which lockers are still open? Can you write an algorithm to figure it out? In constant space?

#### The hat problem
100 prisoners stand in a line. A black or white hat is placed on each person. They don't know the color of their own hat or anybody's behind them, but they can see the hats of everyone standing in front of them. Starting from the back, a guard asks them for the color of their hat one by one. If they get it right they're free to go, otherwise they go to jail. What's a plan the prisoners can come up with (before they line up) to maximize their chances of guessing their hat color correctly?

#### 2 Player and N Coins
There are n coins in a line. (Assume n is even). Two players take turns to take a coin from one of the ends of the line until there are no more coins left. The player with the larger amount of money wins. Would you rather go first or second? Assume that you go first, describe an algorithm to compute the maximum amount of money you can win.
```javascript
/*
(Example) Coins: [18, 20, 15, 30, 10, 14]
First Player picks 18, now row of coins is: [20, 15, 30, 10, 14]
Second player picks 20, now row of coins is: [15, 30, 10, 14]
First Player picks 15, now row of coins is: [30, 10, 14]
Second player picks 30, now row of coins is: [10, 14]
First Player picks 14, now row of coins is: [10]
Second player picks 10, game over.

The total value collected by second player is more (20 + 30 + 10) compared to first player (18 + 15 + 14). So the second player wins.
Note that the strategy to pick the maximum of the two corners may not work.
*/
```

#### The lying neighbor
My next door neighbor lies a lot. In fact, he only tells the truth on one day of the week. One day he told me, "I lie on Mondays and on Tuesdays."
The next day he said, "Today is either Thursday, Saturday or Sunday."
The next day he said, "I lie on Wednesdays and Fridays."
On which day of the week does my neighbour tell the truth?

## Algorithms
#### Nested array sum
Find the sum of all integers a list that contains numbers or (nested) arrays of numbers
```javascript
var arr = [1, [2, 3], [4, [5, [6, 7], 8]], [[9], [10, 11]], [[[12]]]];
myFunction(arr); // 78
```

#### Product Combination
Given an array of unique numbers, return an array of products from all possible combinations of three numbers.
```javascript
var numbers = [1, 3, 5, 9];

// 1 * 3 * 5 = 15
// 1 * 3 * 9 = 27
// 1 * 5 * 9 = 45
// 3 * 5 * 9 = 135

myFunction(numbers); // [15, 27, 45, 135]
```

#### Rectangle intersection
Given two rectangles on a grid, return the area of overlap (or 0 if there is no overlap).
```javascript
var Rectangle = function(x, y, width, height) {
  // (x,y) represents the lower left corner
  // format coordinates as tuples
  this.LL = [x, y];
  this.LR = [x + width, y];
  this.UL = [x, y + height];
  this.UR = [x + width, y + width];
}

var rect1 = new Rectangle(0, 0, 3, 3);
var rect2 = new Rectangle(1, 1, 4, 1);

myFunction(rect1, rect2); // 2
```

#### Find a dupe
You are given an array of length N that contains random integers from 1 to N-1 (inclusive). Write a function that will return a number that appears more than once in the array. There will always be at least one duplicate number in the array. Constraints: O(n log n) time complexity and O(1) space complexity, without mutating the original array.
```javascript
var list = [4, 1, 5, 2, 1, 2];

myFunction(list); // return either 1 or 2
```

#### Island Count
Given a 2D matrix filled with 1's and 0's, count the number of islands in the matrix. An island is a group of 1's that are connected adjacently to each other (not including diagonally).
```javascript
var matrix = [
  [0, 1, 0, 1, 0],
  [0, 0, 1, 1, 1],
  [1, 0, 0, 1, 0],
  [0, 1, 1, 0, 0],
  [1, 0, 1, 0, 1]
];

myFunction(matrix); // 6
```

#### Find Pivot
Given a sorted array that has been rotated, find the pivot point index. Constraint: O(log n) time complexity.
```javascript
var pivotArray = [5, 6, 7, 1, 2, 3, 4];

myFunction(pivotArray); // return 3, the index of the pivot point
```

#### Line of Best Fit
As an input, you have points on a 2D graph. You aim to find a straight line that can fit as my points as possible. Return the maximum number of points you can fit.

#### Triplet Sums
Given an array of integers and a number N, find all the triplets that will add up to a sum greater than or equal to N. The triplets should be arranged in increasing order.
```javascript
var myArray = [50, 20, 30, 40, 10];

myFunction(myArray, 90); // [[10, 40, 50], [20, 30, 40], [20, 40, 50], [30, 40, 50]]
```

#### Pascal's triangle
Write a function that returns n lines of Pascal's triangle
```javascript
// Pascal's triangle:
//         1
//       1   1
//     1   2   1
//   1   3   3   1
// 1   4   6   4   1
//        ...
```

#### 2nd largest node in a binary tree
Write a function that finds the second largest value in a binary tree  

#### Steady String
A string of length N (where N is evenly divisible by 4) contains only the letters A, B, C, D. This string is considered steady if each of the letters occur exactly N/4 times. Find the length of the smallest possible substring that needs to be replaced in order to for the string to be steady. If the string is already steady, return 0.
```javascript
myFunction('AAABAAAC'); // 5
                        // 'AAABA' can be replaced with 'BBCDD' to make it steady

myFunction('AAADDBBB'); // 4
                        // 'ADDB' can be replaced with 'CCDD' to make it steady

myFunction('AAABAAAA'); // 6
                        // 'AAABAA' can be replaced with 'BBCCDD' to make it steady
```

#### Sum pair
Given an unsorted array of integers and a sum value, write a function that finds the pairs of integers whose sum equals the sum value. There may be duplicate integers. Constraints: linear time complexity.
```javascript
myFunction([13, 13, 1, 1, 3, 4, 5, 8, 9, 10], 14); // [[1, 13], [1, 13], [4, 10], [5, 9]];
```
##### Sum pair, extended
Given an array of integers and a value, determine if there are any two integers in the array which sum equal to the given value. Constraints: O(n log n) time complexity, O(1) space complexity.

#### Dutch national flag sort
Given an array that consists of 0's, 1's, and 2's, return the same array sorted. Constraints: O(n) time complexity, O(1) space complexity.
```javascript
var arr = [2,0,0,1,2,1];
myFunction(arr); // [0,0,1,1,2,2]
```

#### Path between tree nodes
Find the path between two nodes on a binary search tree (sorted) and on a binary tree.

#### Rectangle combinations
Given an N x M matrix, print all squares/rectangles of all possible sizes(all 1*1, then all 1*2…. 2*1… )

#### Rotate array
Given an N x M matrix, rotate the matrix 90 degrees clockwise.
```javascript
var array = [
  ['a', 'b', 'c', 'd'],
  ['e', 'f', 'g', 'h'],
  ['i', 'j', 'k', 'l']
];

var rotatedArray = [
  ['i', 'e', 'a'],
  ['j', 'f', 'b'],
  ['k', 'g', 'c'],
  ['l', 'h', 'd']
];

myFunction(array); // should deep equal rotatedArray
```

#### Rotate array (Challenge mode)
Given an N x N matrix, rotate the matrix 45 degrees clockwise.
```javascript
var array = [
  [1, 2, 3],
  [4, 5, 6],
  [7, 8, 9]
];

var rotatedArray = [
  [      1      ],
  [    4 , 2    ],
  [  7 , 5 , 3  ],
  [    8 , 6    ],
  [      9      ]
];

myFunction(array); // should deep equal rotatedArray
```

#### Midpoint singly linked list
Find the middle element of a *singly* list. Constraints: O(n) time complexity, O(1) space complexity.

#### Reversed singly linked list
Given the pointer to the head of a singly linked list, reverse it and return the pointer to the head of the reversed linked list. Constraints: O(n) time complexity, O(1) space complexity.
```javascript
/*
Given the following linked list
head --> 4 --> 12 --> 7 --> 22 --> NULL

return the reversed linked list
head --> 22 --> 7 --> 12 --> 4 --> NULL
*/
```

#### Maximal subarray
Given an array, return the subarray with the maximum sum.
```javascript
var array = [1, -3, 5, -2, 9, -8, -6, 4];

myFunction(array); // [5, -2, 9];
```

#### Next biggest number
Given an integer, return the next biggest number that can be formed using the same digits. If no bigger number can be made, return -1.
```javascript
myFunction(341) === 413; // true
myFunction(413) === 431; // true
myFunction(431) ===  -1; // true
myFunction(5)   ===  -1; // true
myFunction(501) ===  -1; // true
```

#### Array permutation
Given an array of unique elements, return an array of all permutations of the elements. Extra: modify the function so that it can handle an array that may have duplicate elements. The returned permutations should all be unique.
```javascript
var arr = [1, 2, 3];
var permutations = [
  [ 1, 2, 3 ],
  [ 1, 3, 2 ],
  [ 2, 1, 3 ],
  [ 2, 3, 1 ],
  [ 3, 1, 2 ],
  [ 3, 2, 1 ]
];
myFunction(arr); // should deep equal permutations
```

#### Array spiral  
Given a positive integer N, return a N x N matrix with a spiral pattern. The pattern will spiral inwards starting from a corner, where no leg of the spiral can be immediately adjacent to another leg (parts of the spiral can't touch side-to-side).
```javascript
myFunction(5); // [[1, 1, 1, 1, 1],
               //  [1, 0, 0, 0, 0],
               //  [1, 0, 1, 1, 1],
               //  [1, 0, 0, 0, 1],
               //  [1, 1, 1, 1, 1]]

myFunction(6); // [[1, 1, 1, 1, 1, 1],
               //  [1, 0, 0, 0, 0, 0],
               //  [1, 0, 1, 1, 1, 1],
               //  [1, 0, 1, 0, 0, 1],
               //  [1, 0, 0, 0, 0, 1],
               //  [1, 1, 1, 1, 1, 1]]

```

#### Balance parens
Print all possible combinations of balanced parenthesis up to n.
```javascript
myFunction(2); // (()), ()()
myFunction(3); // ((())), (()()), (())(), ()(()), ()()()
```

#### Coin Change  
Given a list of coin values, how many ways can you make change for a given amount N? You may assume you have an infinite amount of coins of each value. For example given a target amount, N = 4, and list of coin values, coins = [1, 2, 3], there are four ways to make change for the amount 4: {1, 1, 1, 1}, {1, 1, 2}, {2, 2}, {1, 3}. Try to optimize the solution. Hint: memoization.  
```javascript
myFunction(4, [1, 2, 3]); // 4

myFunction(10, [2, 3, 5, 6]); // 5
// { 2, 2, 2, 2, 2}, { 2, 2, 3, 3 }, { 2, 2, 6 }, { 2, 3, 5 }, { 5, 5 }
```  

#### Min Sum Path  
Given a M x N grid with non-negative numbers, find a path from the top left to the bottom right which minimizes the sum of all numbers along the path. The output should be the sum.  
```javascript
var input = [
  [1, 3, 2],
  [4, 3, 1],
  [5, 6, 1]
];

myFunction(input); // 8 (start -> 1 -> 3 -> 2 -> 1 -> 1 -> end)
```

#### Max Balanced Binary Subarray
Given an array consisting of 0s and 1s, return the length of the longest subarray that contain an equal number of 0s and 1s.  
```javascript
var input = [1, 1, 1, 0, 1, 0, 0, 1];
myFunction(input); // 6

var input = [0, 1, 1, 1, 1, 0, 0, 1];
myFunction(input); // 4

var input = [0, 1, 1, 1, 0];
myFunction(input); // 2

var input = [1, 1];
myFunction(input); // 0
```

#### Pythagorean triplets  
Given an array of integers, find all Pythagorean triplets in the array. Pythagorean triplets are 3 integers [a, b, c] such that a^2 + b^2 = c^2.
```javascript
var input = [1, 13, 3, 4, 10, 12, 2, 5];
myFunction(input); // [[3, 4, 5], [5, 12, 13]]
```

#### Say What You See  
Given an array of strings that are digits, return an array of the spoken descriptions of those string-digits. For example the string "12" is spoken as "one one, one two", so return "1112". The string "211" is spoken as "one two, two ones", so return "1221".
```javascript
myFunction(['12', '21']);     // ['1112', '1211']
myFunction(['1112', '1133']); // ['3112', '2123']
myFunction(['11114', '123']); // ['4114', '111213']
myFunction(['555334']);       // ['352314']
```

#### Longest Palindrome in a String  
Given a string, return the longest palindrome that is found inside of the string. Contraints: linear time and constant space.
```javascript
var str = 'abbcdcdcba';
myFunction(str); // 'bcdcdcb'
```

#### Max Distance Monotonic  
A monotonic pair in an array A of length N is a pair of integers (P, Q) such that 0 <= P <= Q <= N and A[P] <= A[Q].
Given an array of integers, find the monotonic pair whose indeces are furthest apart and return that distance. Constraints: linear time complexity and linear space complexity.
```javascript
var arr = [5, 3, 6, 3, 4, 2];

// There are 11 monotonic pairs: 
// (0,0), (0, 2), (1, 1), (1, 2), (1, 3), (1, 4), (2, 2), (3, 3), (3, 4), (4, 4), (5, 5)
// The biggest distance is 3, in the pair (1, 4)

myFunction(arr); // 3
```

#### Count Moves  
You are given an array of integers of length N. A move consists of incrementing N-1 of the elements by one. What is the minimum number of moves needed for all the integers to be equal?
```javascript
var arr = [5, 6, 8, 8, 5];

// 1st move: [6, 7, 8, 9, 6];
// 2nd move: [7, 8, 9, 9, 7];
// 3rd move: [8, 9, 10, 9, 8];
// 4th move: [9, 10, 10, 10, 9];
// 5th move: [10, 11, 11, 10, 10];
// 6th move: [11, 11, 12, 11, 11];
// 7th move: [12, 12, 12, 12, 12];

myFunction(arr); // 7
```

#### Max Difference in Order  
Given an array of integers, find the maximum difference between two elements such that the smaller element appears earlier in the array than the larger element. Constraints: Linear time complexity, constant space complexity.  
```javascript
var arr = [2, 7, 9, 5, 1, 3, 5];

myFunction(arr); // 7
// The pair is (2, 9) 
```

#### Zig Zag String  
Given a string and integer N, print the string in a zig-zag form in N rows. See below.
```javascript
var string = "HELLOAWESOMEWORLD", N = 3;

// result...
//      H       O       S       W       D
//        E   L   A   E   O   E   O   L
//          L       W       M       R
```