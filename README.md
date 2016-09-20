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

## Algorithms
#### Product Combination
Given an array of unique numbers, return an array of products from all possible combinations of three numbers.
```javascript
var numbers = [1, 3, 5, 9];

// 1 * 3 * 5 = 15
// 1 * 3 * 9 = 27
// 1 * 5 * 9 = 45
// 3 * 5 * 9 = 135

myFunction(numbers) = [15,27,45,135];
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

myFunction(rect1, rect2) = 2;
```