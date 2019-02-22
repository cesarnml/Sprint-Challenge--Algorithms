# Answers

## Exercise 1

```
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```
ANSWER for A:
The runtime is O(n); the while loop will execute n times since n x (n * n) = n ** 3


```
b)  sum = 0

    for i in range(n):
      i += 1
      for j in range(i + 1, n):
        j += 1
        for k in range(j + 1, n):
          k += 1
          for l in range(k + 1, 10 + k):
            l += 1
            sum += 1
```
ANSWER for B:
Loops wil run (polynomial expression), (end - start):
(n-1 - 0)(n-1 - j+1)(n-1 - k+1)(k+10-1 - k+1)
simplies to:
(n - 1)(n - j)(n - k)(10)
ignoring all terms except for the largest order of n:
simplies to n^3, so O(n^3) is runtime

```
c)  def bunnieEars(bunnies):
      if bunnies == 0:
        return 0

      return 2 + bunnyEars(bunnies-1)
```

ANSWER for c:
runtime is O(n) since the callstack will be called n times in order to reach exit condition

## Exercise 2
Suppose that you have an _n_-story building and plenty of eggs. Suppose also
that an egg gets broken if it is thrown off floor _f_ or higher, and doesn't get
broken if dropped off a floor less than floor _f_. Devise a strategy to
determine the value of _f_ such that the number of dropped eggs is minimized.

Write out your proposed algorithm in plain English or pseudocode and give the
runtime complexity of your solution.

ANSWER:
Employ a binary search to find floor _f_, which will have runtime O(log(n)).
Step 1: Calculate middle_floor = n // 2
Step 2: Drop egg from middle_floor... see if it breaks
Step 3a: If egg breaks ... repeat algorithm on lower floors (1:middle_floor - 1)
Step 3b: If egg doesn't break ... repeat algorithm on upper floors (middle_floor:n)