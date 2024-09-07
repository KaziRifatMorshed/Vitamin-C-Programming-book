# Operator & Expression

## Theory

Execute this line and think, what is happening...

```c
#include <stdio.h>
int main(void) {
  int a, b, c, d, e;
  e = 7;
  printf("e = %d\n", e);
  c = d = e;
  printf("c = %d, d = %d, e =  %d\n", c, d, e);
  a = b = c = d = e = -3; // last "value" or "value of variable" (-3) is going to be assigned to all variables before the last one
  printf("%d %d %d %d %d ", a, b, c, d, e);
}
```

similarly,

```c
#include <stdio.h>
int main(void) {
  int a = 1, b = 2, c = -3, d = 0, e = b, f = e;
  printf("%d %d %d %d %d %d", a, b, c, d, e, f);
}
```

You can assign multiple statements in one line with comma. Luckily, you wont have to write multiple lines with semicolon.

```c
#include <stdio.h>
int main(void) {
  printf("Hello "), printf("World"), putchar('\n'), printf("input any int value:");
  int a = 0;
  scanf("%d", &a), printf("\na is %d...", a);
}
```

this trick is helpful for situation like:

```c
// Note that, this is a cuda code, do not get confused it with a C Programming language code
// the purpose of presenting it is to let you know that you can use this trick in scenarios like this...

~#include <cstdio>
~#include <cstdlib>
~#include <cuda.h>
~
~#define SIZE 1024
~
~__global__ void VectorAdd(int *a, int *b, int *c, int n) {
~  int i = threadIdx.x;
~  if (i < n) {
~    c[i] = a[i] + b[i];
~  }
~}
~
~/*
~".cu": "cd $dir && nvcc $fileName -o $fileNameWithoutExt -arch=sm_86 &&
~$dir$fileNameWithoutExt",
~*/
int main(void) {
  int *a, *b, *c;
   
  cudaMallocManaged(&a, SIZE * sizeof(int)), cudaMallocManaged(&b, SIZE * sizeof(int)), cudaMallocManaged(&c, SIZE * sizeof(int));

  for (int i = 0; i < SIZE; i++) {
    a[i] = b[i] = i;
    c[i] = 0;
  }

~
~  int threadsPerBlock = 256;
~  int blocksPerGrid = (SIZE + threadsPerBlock - 1) / threadsPerBlock;
~
~  // VectorAdd<<<1, SIZE>>>(a, b, c, SIZE); // <<<1, SIZE>>> WAS AN ERROR
~  VectorAdd<<<blocksPerGrid, threadsPerBlock>>>(a, b, c, SIZE);
~
~  // Kernel execution happens here
~
~  cudaDeviceSynchronize(); // Wait for kernel to finish
~
~  for (int i = 0; i < 10; i++) {
~    printf("c[%d] = %d\n", i, c[i]);
~  }
~
  cudaFree(a), cudaFree(b), cudaFree(c);

} // WORKING

```

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
