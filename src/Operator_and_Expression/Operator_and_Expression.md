# Operator & Expression

## Problems

* ***Click on the title of the problem to submit your solution before looking at our solution.***
* ***We discourage looking at our solution before attempting to solve it by yourself first.***

1. **[Simple Calculator ↗️](https://vjudge.net/problem/Gym-287306C)**

   Given two numbers X and Y. Print the summation and multiplication and subtraction of these 2 numbers.

   ***Input***

   Only one line containing two separated numbers \\(X, Y (1  ≤  X, Y  ≤  10 ^ 5)\\)

   ***Output***

   Print 3 lines that contain the following in the same order:

   1. "\\(X + Y =\\) **summation result**" without quotes.
   2. "\\(X \* Y =\\) **multiplication result**" without quotes.
   3. "\\(X - Y =\\) **subtraction result**" without quotes.

   ***Examples***

   Input

   ```
   5 10
   ```

   Output

   ```
   5 + 10 = 15
   5 * 10 = 50
   5 - 10 = -5
   ```

   ***Notes***

   **Be careful with spaces.**

   Hint:

   ```hint
   Press the eye icon to reveal hint.
   ~ Use long long int instead of int
   ~ Don't forget to use the designated format specifier for long long int (%lld)
   ```

   **Solution**

   ```c
   // Press the eye icon to reveal solution.
   ~#include <stdio.h>

   ~int main()
   ~{
   ~    long long x, y;
   ~
   ~    scanf("%lld %lld", &x, &y);
   ~
   ~    printf("%lld + %lld = %lld\n", x, y, x + y);
   ~    printf("%lld * %lld = %lld\n", x, y, x * y);
   ~    printf("%lld - %lld = %lld\n", x, y, x - y);
   ~
   ~    return 0;
   ~}
   ```

2. **[Difference ↗️](https://vjudge.net/problem/Gym-287306D)**

   Hint:

   ```hint
   Press the eye icon to reveal hint.
   ~ Use long long int instead of int
   ~ Don't forget to use the designated format specifier for long long int (%lld)
   ```

   **Solution**

   ```c
   // Press the eye icon to reveal solution.
   ~#include <stdio.h>

   ~int main()
   ~{
   ~    long long a, b, c, d, x;
   ~
   ~    scanf("%lld %lld %lld %lld", &a, &b, &c, &d);
   ~
   ~    x = (a * b) - (c * d);
   ~
   ~    printf("Difference = %lld\n", x);
   ~
   ~    return 0;
   ~}
   ```
