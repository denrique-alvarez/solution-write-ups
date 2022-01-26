# [Multiples of 5 or 3](https://www.codewars.com/kata/514b92a657cdc65150000006/train/javascript)

This function goes from 0 to a given number looking for multiples of 3 or 5 and
then returns a value with the total sum of such numbers.

I can't think of a practical situation where this function will be helpful except
for practicing coding, which is good enough.

## Syntax

> solution(`number`) -> `number`

### Parameters

**number**; `number`

This number is the highest number until which mulples will be looked for and
added up.

### Return value; `number`

The return value is the total sum of all multiples found between 0 and the given
number.

### Test cases

Sample tests from CodeWars

```js
const { assert } = require("chai")

function test(n, expected) {
  let actual = solution(n)
  it(`Expected ${expected}, got ${actual}`, () => {
  assert.strictEqual(actual, expected)
    })
}

describe("basic tests", function(){
  test(10,23)
})
```

## Use Cases

> This function is not very complicated so there are not many edge cases.
> We could just keep adding different multiples or changing them without altering the basic behavior of the function.

Looking for other multiples

```js
function solution(number){
  let sum = 0;
  for (let i = 0; i < number; i++) {
    if (i % 4 === 0 || i % 6 === 0) {
      sum = sum + i;
    }
  }
  return sum;
}
```

More than two multiples

```js
function solution(number){
  let sum = 0;
  for (let i = 0; i < number; i++) {
    if (i % 4 === 0 || i % 6 === 0 || i % 9 === 0) {
      sum = sum + i;
    }
  }
  return sum;
}
```

## Retrospective

Finding a practical use for this function seems pretty tricky. However, it's very
interesting how a given value can be deconstructed and then translated into a different
value, totally different but related. With the help of a loop and a couple operators,
it's possible to translate something like a number into something else. I am sure
it could be possible to build something else on top of this type of function but
it's hard to see exactly what. Maybe creating an array where those numbers can be
used as values or indexes.

Or maybe a small feature that, given a number, like a password, can generate a
new one.

### Continue Doing

- It's good to think about possible uses for a piece of code. That gives the exercise
  an extra layer of complexity but also makes things a bit more 'real'.

- Writing and understanding code in terms of variables, parameters and arguments.
  This help you think in terms of the bahavior and less in terms of the specific
  result. Save that for the test cases.

### Start Doing

- Still need to write my own test cases.

- Check more solutions that implement different language features that I have not
  used and tweak them.

### Stop Doing

- Better this time, but still rushing, specially when going through other people
  code.
