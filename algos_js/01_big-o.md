# Big O notation

Big O notation allows us to categorize the performance of a given solution to a problem (algorithm), so we can compare solutions and choose the most efficient one.

Performance doesn't necessarily matter in personal projects. But at a large company, your algorithm might be handling a very large dataset, and one solution could run hours faster than another. So this is where Big O is useful.

## What does "better" mean?

When comparing two solutions, "better" can depend on the context. You might prefer a more readable solution, a solution that runs more quickly, a solution that uses less memory, etc.

Performance often comes at the expense of readability, so balancing those two is important.

## Timing code: Not an ideal approach

You can use `performance.now()` to get an accurate timestamp, running it before and after your code executes:

```javascript
const t1 = performance.now();
// do something here
const t2 = performance.now();
console.log(`Time Elapsed: ${(t2 - t1) / 1000} seconds.`);
```

Timing is not ideal because it can vary, even on the same machine. Timing is not the most reliable or the easiest to talk about, and which solution "wins" could vary based on large inputs, small inputs, etc. And for fast algorithms, speed measurements may not be precise enough. It's also painful to compare an algo that takes one hour with an algo that takes four hours.

## A better approach: Counting operations

Instead of timing the code, we can count the number of simple operations the computer has to perform in order to execute the solution.

We aren't looking for the exact number -- counting every single individual operation in code can be tricky. We're looking for a higher level sense of how many operations are required. Does that number of operations grow proportionally based on input? How steep is that growth? Big O notation is more focused on the overall trend in the operation count.
