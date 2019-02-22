Add your answers to the Algorithms exercises here.

```
a)  a = 0
    while (a < n * n * n):
      a = a + n * n
```
ANSWER for A:
For n = 0; runtime is O(1); the while loop will never execute
For n > 1; runtime is O(n); the while loop will execute n times since n x (n * n) = n ** 3


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

