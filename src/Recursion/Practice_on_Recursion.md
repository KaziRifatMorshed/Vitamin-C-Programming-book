# PRACTICE Recursion

Some of the sollowing problems are directly copied from [Zobayer Hasan vai's blog post on recursion](https://zobayer.blogspot.com/2009/12/cse-102-practice-recursions.html). We are grateful to his open contributions towards learning CS.\
You can use the [Competitive Programming Helper (cph)](https://marketplace.visualstudio.com/items?itemName=DivyanshuAgrawal.competitive-programming-helper) extension in VS code to make your practice easier though it wont make a big difference.

<i>ALL THE BEST FOR YOUR HARD WORK.</i>

### Problems on Recursion

1. Print 1 to 50 with a recursive function.\\

   Output:

   ```
   1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 17 18 19 20 21 22 23 24 25 26 27 28 29 30 31 32 33 34 35 36 37 38 39 40 41 42 43 44 45 46 47 48 49 50 
   ```

   Hint:

   ```c
            // recursive call
            printer(number + 1); // value of number increments here
   ```

   Solution:

   ```c
    ~#include <stdio.h> 
    ~void printer(int number) {
    ~    // printf("in this recursive call, number is %d \n", number);
    ~    // Base Case
    ~    if (number > 50) { // in a new recursive call, if the value of number is greater than 50, recursive call should terminate
    ~        return;
    ~    } else {
    ~        printf("%d ", number);
    ~        // recursive call
    ~        printer(number + 1); // value of number increments here
    ~    }
    ~}
    ~int main(void) {
    ~    printer(1);
    ~}
   ```

2. Print 1 to 50 reversely with a recursive function.\\

   Output:

   ```
   50 49 48 47 46 45 44 43 42 41 40 39 38 37 36 35 34 33 32 31 30 29 28 27 26 25 24 23 22 21 20 19 18 17 16 15 14 13 12 11 10 9 8 7 6 5 4 3 2 1 
   ```

   Hint:

   ```
        uno reverse...
        write down only 5 recursive call (with code and variable value) in your notebook
   ```

   Solution:

   ```c
    ~#include <stdio.h> 
    ~void printer(int number) {
    ~    if (number > 50) { 
    ~        return;
    ~    } else {
    ~        printer(number + 1); // notice the change here
    ~        printf("%d ", number); // and think, how ?
    ~    }
    ~}
    ~int main(void) {
    ~    printer(1);
    ~}
   ```

3. Print out the series $$ 1 + 2 + 3 + ... + n $$ and determine the sum.\
   Input:
   ```
   5
   ```
   Output:
   ```
   1 + 2 + 3 + 4 + 5 = 15
   ```
   Hint:
   ```c
   ~#include <stdio.h>
    int sum_it(int num, int limit) {
   ~ if (num > limit) {
   ~     printf("= ");
   ~     return 0;
   ~ } else {
   ~     printf("%d ", num);
   ~     if (num != limit) {
   ~     printf("+ ");
   ~     }
   ~     return num + sum_it(num + 1, limit);
   ~ }
   ~ }
   ~ int main(void) {
   ~ int limit = 0;
   ~ scanf("%d", &limit);
   ~ int sum = sum_it(1, limit);
   ~ printf("%d", sum);
   ~ } // done
   ```

4. You will be given an array of integers. Write a recursive solution to print it in (inputted) order.\
   Input:
   ```
   5
   69 87 45 21 47
   ```
   Output:
   ```
   69 87 45 21 47
   ```
   Hint:

5. Same as before. Add index number (starting from 1) to each int output in (inputted) order.\
   Input:
   ```
   5
   69 87 45 21 47
   ```
   Output:
   ```
   1.69 2.87 3.45 4.21 5.47
   ```

6. Same as before. Add index number (starting from n) to each int and get output in reverse order.\
   Input:
   ```
   7
   69 87 45 21 47 76 2
   ```
   Output:
   ```
   7.69 6.87 5.45 4.21 3.47 2.76 1.2 
   ```

7. You will be given an array of integers. Write a recursive solution to print it in reverse order.
   Input:
   ```
   5
   62 87 45 24 47
   ```
   Output:
   ```
   47 24 45 87 62
   ```

8. Same as before. The program will print inputted numbers except even integers.
   Input:
   ```
   5
   62 87 45 24 47
   ```
   Output:
   ```
   47 45 87
   ```

9. Use recursion to find max among 2 integers.

10. Use recursion to find the max among 3 integers.

11. Use recursion to find min among 2 integers.

12. Use recursion to find min among 3 integers.

13. Write a recursive function to print an array in the following order.
    ```
    [0] [n-1] 
    [1] [n-2]  
    ... 
    [(n-1)/2] [n/2]
    ```
    Input:
    ```
    5
    1 5 7 8 9
    ```
    Output:
    ```
    1 9
    5 8
    7 7
    ```

14. Write a recursive program to remove all odd integers from an array. You must not use any extra array or print anything in the function. Just read the input, call the recursive function, and then print the array in main().\
    Input:
    ```
    6
    1 54 88 6 55 7
    ```
    Output:
    ```
    54 88 6
    ```

15. Write a recursive solution to print the polynomial series for any input n: $$ 1 + x + x^2 + ... + x^{n-1} $$ \
    Input:
    ```
    5
    ```
    Output:
    ```
    1 + x + x^2 + x^3 + x^4
    ```

16. Write a recursive solution to evaluate the previous polynomial for any given x and n. Like, when x=2 and n=5, we have $$ 1 + x + x^2 + ... + x^{n-1} = 31 $$ \
    Input:
    2 5
    Output:
    31

17. Write a recursive program to compute n!\
    Input:
    5
    Output:
    120

18. Write a recursive program to compute the ~n-th~ Fibonacci number. 1st and 2nd Fibonacci numbers are 1, 1.\
    Input:
    6
    Output:
    8

19. Write a recursive program to determine whether a given integer is prime or not.\
    Input:
    49
    999983
    1
    Output:
    not prime
    prime
    not prime

20. Write a recursive function that finds the gcd of two non-negative integers.\
    Input:
    25 8895
    Output:
    5

21. Write a recursive solution to compute the LCM of two integers. You must not use the formula lcm(a,b) = (a x b) / gcd(a,b); find lcm from scratch...\
    Input:
    23 488
    Output:
    11224

22. Suppose you are given an array of integers in an arbitrary order. Write a recursive solution to find the maximum element from the array.\
    Input:
    5
    7 4 9 6 2
    Output:
    9

23. Write a recursive solution to find the second maximum number from a given set of integers.\
    Input:
    5
    5 8 7 9 3
    Output:
    8

24. Implement linear search recursively, i.e. given an array of integers, find a specific value from it. Input format: first n, the number of elements. Then n integers. Then, q, the number of queries, then q integers. Output format: for each of the q integers, print its index (within 0 to n-1) in the array or print 'not found', whichever is appropriate.\
    Input:
    5
    2 9 4 7 6
    2
    5 9
    Output:
    not found
    1

25. Implement binary search recursively, i.e. given an array of sorted integers, find a query integer from it. Input format: first n, the number of elements. Then n integers. Then, q, the number of queries, then q integers. Output format: for each of the q integers, print its index (within 0 to n-1) in the array or print 'not found', whichever is appropriate.\
    Input:
    5
    1 2 3 4 5
    2
    3 -5
    Output:
    2
    not found

26. Write a recursive solution to get the reverse of a given integer. The function must return an int.\
    Input:
    123405
    Output:
    504321

27. Read a string from keyboard and print it in reversed order. You must not use any array to store the characters. Write a recursive solutions to solve this problem.\
    Input:
    helloo
    Output:
    oolleh

28. Write a recursive program that determines whether a given sentence is palindromic or not just considering the alpha-numeric characters ('a'-'z'), ('A'-'Z'), ('0'-'9').\
    \
    Input:
    ```
    madam
    ```
    Output:
    ```
    palindromic
    ```
    Input:
    ```
    hulala
    ```
    Output:
    ```
    not palindromic
    ```

29. Implement prime number determining algorithm recursively.

    Hint:

    ```c
    isPrime(num, j + 2);
    ```

    Solution:

    ```c
        ~int isPrime(int num, int j) { // RECURSIVE
        ~  if (num <= 1) {
        ~    return false;
        ~  }
        ~  if (num % 2 == 0) {
        ~    return false;
        ~  }
        ~  if (num % j == 0) {
        ~    return false;
        ~  }
        ~  if (j * j <= num) {
        ~    isPrime(num, j + 2);
        ~  }
        ~  return true;
        ~}
    ```

30. Implement strcat(), stracpy(), strcmp() and strlen() recursively.\
    \
    Input:
    test on your own\
    Output:
    test on your own

31. If you already solved the problem for finding the nth fibonacci number, then you must have a clear vision on how the program flow works. So now, in this problem, print the values of your fibonacci function in pre-order, in-order and post-order traversal. For example, when n = 5, your program calls 3 and 4 from it, from the call of 3, your program calls 1 and 2 again....... here is the picture:
    Input:

    ```
    5
    ```

    Output:

    ```
    Inorder: 1 3 2 5 2 4 1 3 2
    Preorder: 5 3 1 2 4 2 3 1 2
    Postorder: 1 2 3 2 1 2 3 4 5
    ```

32. Convert a Decimal number to Binary.\
    Hint:

    ```
    return Decimal_to_Binary_RECURSIVE(i / 2) ... ;
    ```

    Solution:

    ```c
    ~#include <stdio.h>
    ~int Decimal_to_Binary_RECURSIVE(int i) {
    ~    if (i == 0){
    ~        return 0;
    ~    }
    ~    return Decimal_to_Binary_RECURSIVE(i / 2) * 10 + i % 2;
    ~}
    ~int main(void) {
    ~    int i = 0;
    ~    scanf("%d", &i);
    ~    printf("the binary of the decimal num %d is %d", i, Decimal_to_Binary_RECURSIVE(i));
    ~}
    ```

33. All of you have seen the tower of Hanoi. You have 3 pillars 'a', 'b' and 'c', and you need transfer all disks from one pillar to another. Conditions are, only one disk at a time is movable, and you can never place a larger disk over a smaller one. Write a recursive solution to print the moves that simulates the task, a -> b means move the topmost of tower a to tower b.\
    \
    Input:

    ```
    3
    ```

    Output:

    ```
    a -> c
    a -> b
    c -> b
    a -> c
    b -> a
    b -> c
    a -> c
    x
    ```
