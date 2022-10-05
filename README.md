# **Algorithms**

Algorithms done in JavaScript.

General study

# Big O notation

> **Is a mathematical notation that describes the limiting behavior of a function when the argument tends towards a particular value or infinity.**

> f(n) could be linear $$f(n) = n$$

> f(n) could be quadratic $$f(n) = n^2$$

> f(n) could be constant $$f(n) = 1$$

> f(n) could be soething entierly diffrent

> Simplifying to measure efficiency
>
> $$O(2n) -> O(n)$$
>
> $$O(500) -> O(1)$$
>
> $$O(12n^2) -> O(n^2)$$

# Time Complexity

> we analyze the runtime of an algorithm as the size of inputs increases

# Space Complexity

> we analyze how much additional memory do we need to allocate in order to run the code in our algorithm

# **Metrics**

## **Basic metrics - speed/time**

> not reliable

> not precise enough when measuring fast algorithms or too time consuming with slow algorithms

```js
const t1 = performance.now();
//function here
const t2 = performance.now();

console.log(`Time elapsed: ${(t2 - t1) / 1000} seconds.`);
```

## **Basic metrics - counting operations**

```js
function addUpTo(n) {
  return (n * (n + 1)) / 2;
}
// three operations

// 1 multipliaction, 1 addition, 1 division
```

```js
function addUpTo(n) {
  let total = 0;

  for (let i = 1; i <= n; i++) {
    total += i;
  }

  return total;
}
// 5n + 2 operations

// 1 assigment on total
// 1 initial assigment on i variable
// n additions, n assigments on total variable
// n additions, n assigments on i variable
// n comparisons
```
