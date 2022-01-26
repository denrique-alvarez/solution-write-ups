# [Remix 1](https://www.codewars.com/users/denrique-alvarez/completed_solutions)

This solution was very intuitive, the first language features that came to
my mind. After seeing other solutions like
[ooflorent](https://www.codewars.com/users/ooflorent) 's, I realize the
solution could be formulated in a shorter, more efficient way.

<!--
  which solutions inspired your solution?
  what did you take from each one?
-->

```js
function positiveSum(arr) {
  let sum = 0;
  for (num of arr) {
    if (num > 0) {
      sum = sum + num;
    } else {
      sum = sum;
    }
  }
  return sum;
}
```

## Strategy

I took a very obvious approach and kind of wrote 'literally' what the constrains
instructions I was given, first going through all elements and then checking if
the value was positive.

## Implementation

**for... of**: My strategy was checking every element in the array regardless the
number thus I decided this type of loop was the best option for me.

**if... else**: I used this type of conditionals since there were only two possibilities.
Later I realized this was not totally necessary exactly because of the same reason.
The second part of the condition doesn't actually do anything.

## Possible Refactors

- Using a ternary operator instead of a conditional statement.

- Using other array methods like reduce() or filter() to go over the elements and
  obtaining the final value.

- I could also use a for loop with an index but it seems unnecessary in this case
  since the should as many iterations as elements in the array.

## References

I wrote this solution without thinking too much about it so it uses some of the
language features I am the most familiar with so far. Still need to practice ternary
operators and other array methods applicable.
