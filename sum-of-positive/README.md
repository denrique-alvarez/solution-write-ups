# [Sum of positive](https://www.codewars.com/kata/5715eaedb436cf5606000381/train/javascript)

This function takes an array of numbers as parameter, checks the positive
numbers and returns the total sum of those numbers.

This function might be helpful in accounting programs and also for controlling cash-flow.

<!--
  describe the function's behavior in your own words.
  explain why someone might want to use this function
-->

## Syntax

> positiveSum(`array`) -> `number`

### Parameters

**arr**: `array`

This is an array of numbers.

<!--
  describe the parameter
-->

### Return Value: `number`

The return value is the sum of all positive numbers in the array.

<!--
  describe the return value
-->

## Test Cases

Sample tests from CodeWars

```js
describe("Basic tests", () => {
  it("Testing for fixed tests", () => {
    assert.strictEqual(positiveSum([1,2,3,4,5]),15);
    assert.strictEqual(positiveSum([1,-2,3,4,5]),13);
    assert.strictEqual(positiveSum([]),0);
    assert.strictEqual(positiveSum([-1,-2,-3,-4,-5]),0);
    assert.strictEqual(positiveSum([-1,2,3,4,-5]),9);
    });
  });
```

<!--
  copy in the test cases from the original challenge

  if you write your own test cases in a sandbox file, include those too
-->

## Use Cases

> This function is fairly simple so it doesn't take a lot of edge cases.
> Many of the possible cases could be very similar as well.

Savings

```js
const incomeAndExpenses = [1, 6, 34, -56, 24, 667, -76, 21];
const income = positiveSum(incomeAndExpenses);
console.log(income); // 753
```

Cash-flow

```js
const cashRegister = [1, 6, 34, -56, 24, 347, -76, 21];
const totalSold = positiveSum(cashRegister);
console.log(totalSold); //  433
```

<!--
  write a minimum of 2 use cases to show this functions behavior.

  try to find interesting _edge cases_, it's good for you ;)
  an edge case is when a function behaves different than you'd expect.
  This will help you and others better understand the function.

  https://www.geeksforgeeks.org/dont-forget-edge-cases/
-->

---

## Retrospective

This is a very simple function that, however, make me realize the importance of
understanding and looking carefully at each line of code. That can help you
develop good habits and efficient approaches to a problem.

Many language features can be used to solve a problem, so implementation is
just the materialization of a chosen approach to the problem.

I also think this particular function could be expanded and developed into something
much more complex that would consider, for instance, negative values or other
types of elements, which would increase its usability.

<!--
  write any notes to help you review this exercise later, and to help others' study it.

  this might include:

  - good ideas to use later in your own code
  - less good ideas to avoid in your own code
  - new vocabulary you learned
  - the most important thing(s) you learned
  - something that you still don't understand but want to keep studying
  - something that surprised you
  - tricks you will want to remember and use later
-->

### Continue Doing

- Looking for some interesting refactors and tweaks that will allow me practice
  and study other different language features.

### Start Doing

- Writing my own test cases.

- Checking several solutions from other people and analyze the one that could be
  more interesting study-wise.

### Stop Doing

- Rushing through the code. It's better to understand a line code in depth
  before moving on to the next one.
