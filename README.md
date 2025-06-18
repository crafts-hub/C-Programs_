<h2 align="center">Table of Content (C)</h2>


### [Variables](#variables-1)
- [Question 1](#question-1) 👉 swap two numbers without a third variable
- [Question 2](#question-2) 👉 swap two numbers using a third variable
- [Question 3](#question-3) 👉 find absolute value of an input number
- [Question 4](#question-4) 👉 check if one number is divisible by another
- [Question 5](#question-5) 👉 check if the input character is a digit or not
- [Question 6](#question-6) 👉 second largest number among three numbers

### [Loops](#loops-1)
- [Question 7](#question-7) 👉 calculates sum of numbers from start to end
- [Question 8](#question-8) 👉 calculates sum of all even numbers from 1 to 100
- [Question 9](#question-9) 👉 calculates sum of all odd numbers from 1 to 100
- [Question 10](#question-10) 👉 multiplication table of a given number
- [Question 11](#question-11) 👉 calculates factorial of a given number
- [Question 12](#question-12) 👉 reverses the given number
- [Question 13](#question-13) 👉 calculates sum of the digits of a given number
- [Question 14](#question-14) 👉 check if a given number is a perfect number
- [Question 15](#question-15) 👉 find all prime numbers up to a given limit
- [Question 16](#question-16) 👉 check if a given number is an Armstrong number
- [Question 17-](#question-17-) 👉 print Fibonacci series upto given number of terms

### [Nested Loops](#nested-loops-1)
- [Question 17](#question-17) 👉 print a right-angled triangle with left alignment
- [Question 18](#question-18) 👉 print a right-angled triangle with right alignment
- [Question 19](#question-19) 👉 print an inverted right-angled triangle with left alignment
- [Question 20](#question-20) 👉 print an inverted right-angled triangle with right alignment

### [Array](#array-1)
- [Question 21](#question-21) 👉 calculate the sum of all elements in an array
- [Question 22](#question-22) 👉 find the largest number in an array
- [Question 23](#question-23) 👉 find the smallest number in an array
- [Question 24](#question-24) 👉 count even and odd numbers in an array

### [Sequences](#sequences-1)
- [Formulas](#quick-revision-ap-gp-and-hp-formulas)
- [Question 25](#question-25) 👉 Print AP upto n like: 1, 4, 7, ....
- [Question 26](#question-26) 👉 Print GP upto n like: 5, 15, 45, ...
- [Question 27](#question-27) 👉 Print HP upto n like: 1/1, 1/4, 1/7, ...
- [Question 28](#question-28) 👉 print sum of AP
- [Question 29](#question-29) 👉 print sum of GP


### [Exercise](#exercise-1)
- [Question 30](#question-30) 👉 Write output of the program
- [Question 31](#question-31) 👉 Write output of the program
- [Question 32](#question-32) 👉 Write output of the program
- [Question 33](#question-33) 👉 Write output of the program
- [Question 34](#question-34) 👉 Write output of the program
- [Question 35](#question-35) 👉 Write output of the program (Tricky one)






<br>
<p align="right">
  <img src="https://github.com/crafts-hub/C-plus-Programs/blob/main/Source%20Code/z-Assets/LOGO%20PNG_02.png" alt="logo" width="18" style="vertical-align: middle; margin-right: 4px;" />
  <span style="font-size: 10px; color: gray;">jameel499</span>
</p>





---






<h2 align="center">Variables</h2>

### [Question 1](#variables)
#### Write a program to swap two numbers **without** using a third variable.

### Program
```cpp
#include <stdio.h>

int main() {
    int a = 7, b = 9;

    //---- Swapping without a third variable
    a = a + b;  // a = 7 + 9 = 16
    b = a - b;  // b = 16 - 9 = 7
    a = a - b;  // a = 16 - 7 = 9

    printf("After swapping: \n");
    printf("a = %d, b = %d\n", a, b);

    return 0;
}
```

### Output
```
After swapping: 
a = 9, b = 7
```

---

### [Question 2](#variables)
#### Write a program to swap two numbers **using a third variable**.

### Program
```cpp
#include <stdio.h>

int main() {
    int a = 7, b = 9, temp;  
    // swapping ka matbal hai "a = 9" ki value "b = 7" ho jay 

    temp = a; // yahan per "a" ki value "temp" mein store ho gai hai ta ke is ko agay use kar sakein
    a = b;    // finally ab "a" mein "b" store kar sakty hain
    b = temp; // ab hum ne "b" mein "a" ki value store kar rehe hain. 
              //"a" ki value is liye hum ne temp mein store ki thi

    printf("After swapping: \n");
    printf("a = %d, b = %d\n", a, b);

    return 0;
}
```

### Output
```
After swapping: 
a = 9, b = 7
```

---

### [Question 3](#variables)
#### Write a program to find the absolute value of an input number.

### Program
```cpp
#include <stdio.h>

int absolute(int num) {
    if (num < 0)
        return -num; // Make it positive
    else
        return num;  // Already positive
}

int main() {
    int number;
    printf("Enter a number: ");
    scanf("%d", &number);

    printf("Absolute value is: %d\n", absolute(number));

    return 0;
}
```

### Output
```
Enter a number: 
-5
Absolute value is: 5
```


---

### [Question 4](#variables)
#### Write a program to check if one number is divisible by another.

### Program
```cpp
#include <stdio.h>

void checkDivisibility(int a, int b) {
    int rem = a % b;  // Get remainder

    if (rem == 0) {
        printf("%d is divisible by %d\n", a, b);  // No remainder, divisible
    } else {
        printf("%d is NOT divisible by %d, remainder is %d\n", a, b, rem);  // Remainder present
    }
}

int main() {
    int num1, num2;
    printf("Enter two numbers: ");
    scanf("%d %d", &num1, &num2);

    checkDivisibility(num1, num2);

    return 0;
}
```

### Output
```
Enter two numbers: 
10 2
10 is divisible by 2
```

---

### [Question 5](#variables)
#### Write a program to check if the input character is a digit or not.

### Program
```cpp
#include <stdio.h>

void checkIfDigit(char ch) {
    if (ch >= '0' && ch <= '9')
    {
        printf("%c is a digit.\n", ch);
    } else 
    {
        printf("%c is not a digit.\n", ch);
    }
}

int main() {
    char character;
    printf("Enter a character: ");
    scanf(" %c", &character);  // space before %c to consume any leftover newline

    checkIfDigit(character);

    return 0;
}
```

### Output
```
Enter a character: 
5
5 is a digit.
```


---

### [Question 6](#variables)
#### Write a program to find the second largest number among three numbers.

### Program
```cpp
#include <stdio.h>

// As I have made the function below main() function, so I have to Declare it like:
int findSecondLargest(int a, int b, int c);

int main() {
    int num1, num2, num3, secondLargestNum;
    printf("Enter three numbers: ");
    scanf("%d %d %d", &num1, &num2, &num3);

    secondLargestNum = findSecondLargest(num1, num2, num3);

    printf("The second largest number is: %d\n", secondLargestNum);

    return 0;
}

int findSecondLargest(int a, int b, int c) {

    if (a > b && a > c || a > c && a < b) 
    {
        return a;
    } 
    else if (b > a && b > c || b > c && b < a) 
    {
        return b;
    } 
    else 
    {
        return c;
    }
}
```

### Output
```
Enter three numbers: 
3 6 9
The second largest number is: 6
```


---



<h2 align="center">Loops</h2>


### [Question 7](#loops)
#### Write a program that calculates the sum of numbers from `start` to `end`.

### Program
```cpp
#include <stdio.h>

int Calculate_Sum(int start, int end) {
    int sum = 0;
    for (int i = start; i <= end; ++i) {
        sum += i;
    }
    return sum;
}

int main() {
    int start = 1, end = 100;

    int result = Calculate_Sum(start, end);
    printf("Sum of numbers from 1 to 100 is: 👉 %d\n", result);

    return 0;
}

```

### Output
```
Sum of numbers from 1 to 100 is: 👉 5050
```


---

### [Question 8](#loops)
#### Write a program that calculates the sum of all even numbers from 1 to 100.

### Program
```cpp
#include <stdio.h>

int main() {
    int sum = 0;

    for (int i = 1; i <= 100; i++) {
        int remainder = i % 2;
        if (remainder == 0) 
            sum += i;
    }

    printf("The sum of even numbers is: %d", sum);
    return 0;
}

```

### Output
```
The sum of even numbers is: 2550
```


---

### [Question 9](#loops)
#### Write a program that calculates the sum of all odd numbers from 1 to 100.

### Program
```cpp
#include <stdio.h>

int main() {
    int sum = 0;

    for (int i = 1; i <= 100; i++) {
        int remainder = i % 2;
        if (remainder == 0) 
            continue; // if num is even, skip it
        sum += i;
    }

    printf("The sum of odd numbers is: %d", sum);
    return 0;
}

```

### Output
```
The sum of odd numbers is: 2500
```


---

### [Question 10](#loops)
#### Write a program that generates the multiplication table of a given number.

### Program
```cpp
#include <stdio.h>

void CalculateTable(int my_num) {
    for (int i = 1; i <= 10; i++)
    {
        printf("%d X %d = %d\n", my_num, i, (my_num * i));
    }
}

int main() {
    int num;
    printf("Give any number\n");
    scanf("%d", &num);
    
    CalculateTable(num);
    return 0;
}

```

### Output
```
Give any number
5
5 X 1 = 5
5 X 2 = 10
5 X 3 = 15
5 X 4 = 20
5 X 5 = 25
5 X 6 = 30
5 X 7 = 35
5 X 8 = 40
5 X 9 = 45
5 X 10 = 50
```


---

### [Question 11](#loops)
#### Write a program that calculates the factorial of a given number.

### Program
```cpp
#include <stdio.h>

int Calculate_Factorial(int my_num, int fac) // custom method
{
    if (my_num < 0) {
        printf("Factorial is not defined for negative numbers\n");
        return 0;
    } else {
        for (int i = 1; i <= my_num; ++i) {
            fac = fac * i;
        }
        return fac;
    }
}

int main() {
    int num, factorial = 1;
    printf("Enter a positive integer: \n");
    scanf("%d", &num);

    int myFactorial = Calculate_Factorial(num, factorial);
    printf("Factorial is: 👉 %d\n", myFactorial);
    return 0;
}

```

### Output
```
Enter a positive integer: 
5
Factorial is: 👉 120
```


---

### [Question 12](#loops)
#### Write a program that reverses a given number.

### Program
```cpp
#include <stdio.h>

int main() {
    int my_num, rev = 0;
    printf("Please enter a number! \n");
    scanf("%d", &my_num);
    printf("Your number is: --- %d\n Thank you! :) \n", my_num);

    while (my_num > 0) {
        int lastDigit = my_num % 10;
        rev = rev * 10 + lastDigit;
        my_num /= 10;
    }

    printf("The reversed num is: --- %d\n", rev);
    return 0;
}

```

### Output
```
Please enter a number! 
12345
Your number is: --- 12345
Thank you! :) 
The reversed num is: --- 54321
```

---

### [Question 13](#loops)
#### Write a program that calculates the sum of the digits of a given number.

### Program
```cpp
#include <stdio.h>

int Sum_Of_Digits(int num) {
    int sum = 0;
    
    if (num < 0) {
        printf("Please enter a non-negative number\n");
        return 0;
    } else {
        while (num > 0) {
            int digit = num % 10; // get last digit
            sum += digit;         // add to sum
            num = num / 10;       // remove last digit
        }
        return sum;
    }
}

int main() {
    int number;
    printf("Enter a positive integer: \n");
    scanf("%d", &number);

    int result = Sum_Of_Digits(number);
    printf("Sum of digits is: 👉 %d\n", result);

    return 0;
}

```

### Output
```
Enter a positive integer: 
12345
Sum of digits is: 👉 15
```


---

### [Question 14](#loops)
#### Write a program to check if a given number is a perfect number.

### Program
```cpp
#include <stdio.h>

int main() {
    int num, sum = 0;
    printf("Enter a number.\n");
    scanf("%d", &num);

    for (int i = 1; i <= num / 2; i++) {
        if (num % i == 0) {
            sum += i;
        }
    }

    if (sum == num)
        printf("Perfect: %d", sum);
    else
        printf("Not Perfect: ");

    return 0;
}

```

### Output
```
Enter a number.
6
Perfect: 6
```

---

### [Question 15](#loops)
#### Write a program to find all prime numbers up to a given limit.

### Program
```cpp
#include <stdio.h>

int main() {
    int limitNum;
    printf("Give a limit (0 and 1 excluded): \n");
    scanf("%d", &limitNum);

    for (int i = 2; i <= limitNum; i++) { // I m checking if 'i' is prime or not
        int isPrime = 1;

        for (int j = 2; j <= i / 2; j++) {
            if (i % j == 0) {
                isPrime = 0;
                break;
            }
        }

        if (isPrime)
            printf("%d, ", i);
    }

    printf("\n");
    return 0;
}

```

### Output
```
Give a limit (0 and 1 excluded): 
20
2, 3, 5, 7, 11, 13, 17, 19, 
```


---

### [Question 16](#loops)
#### Write a program to check if a given number is an Armstrong number.

### Program
```cpp
#include <stdio.h>
#include <math.h> // to access pow(_______, _______) func

int main() {
    int num, temp, power = 0, sum = 0;
    scanf("%d", &num);
    temp = num; // just save num's value temporarily

    // Calculate the power count (number of digits)
    while (num != 0) {
        power++;
        num /= 10;
    }
    num = temp; // Restore original number

    // Calculate the sum of each digit raised to the power
    while (num != 0) {
        int lastDigit = num % 10;
        sum += pow(lastDigit, power); // the func gives lastDigit raised to power
        num /= 10;
    }
    num = temp;

    // Check if the number is an Armstrong number
    if (sum == temp) // Compare sum to the original number
        printf("%d is an Armstrong number.\n", temp);
    else
        printf("%d is not an Armstrong number.\n", temp);

    return 0;
}

```

### Output
```
153
153 is an Armstrong number.
```

---


### [Question 17-](#loops)
#### Print Fibonacci series upto a given number of terms.

```
0, 1, 1, 2, 3, 5, 8, 13, 21, 34, ...
```

### Program
```cpp

#include <stdio.h>

int main() {
    int numOfTerms, a = 0, b = 1;

    printf("Give number of terms you want to print:\n");
    scanf("%d", &numOfTerms);

    printf("%d, %d", a, b); // prints first two terms, i.e: 0, 1

    // (i = 3) means it starts from 3rd term because we already printed first two terms
    for (int i = 3; i <= numOfTerms; i++) {
        // below is simple logic of swapping two numbers:
        int c = a + b;
        a = b;
        b = c;
        printf(", %d", b);
    }

    return 0;
}


```

### Output
```

Give number of terms you want to print: 
8
0, 1, 1, 2, 3, 5, 8, 13


```


---







<h2 align="center">Nested Loops</h2>


### [Question 17](#nested-loops)
#### Write a program to print a left aligned right-angled triangle of stars.

### Program
```cpp
#include <stdio.h>

int main() {
    int n = 5; // Height of the triangle
    for (int i = 1; i <= n; i++) 
    {
        for (int j = 1; j <= i; j++) 
        {
            printf("*");
        }
        printf("\n");
    } 
    return 0;
}

```

### Output
```
*
**
***
****
*****
```


---

### [Question 18](#nested-loops)
#### Write a program to print a right-angled triangle of stars with right alignment.

### Program
```cpp
#include <stdio.h>

int main() {
    int n = 5; // Height of the triangle
    for (int i = 1; i <= n; i++) 
    {
        for (int j = n; j > i; j--) // for simple left aligned programs, I did "<=" or ">=". But in this one (as it is right aligned), I did ">" for printing spaces first, the reason is: if (n = 5) then I want to put 4 spaces and then one star
        {
            printf(" ");  // Printing spaces for right alignment
        }
        for (int j = 1; j <= i; j++) 
        {
            printf("*");
        }
        printf("\n");
    } 
    return 0;
}

```

### Output
```
    *
   **
  ***
 ****
*****
```


---

### [Question 19](#nested-loops)
#### Write a program to print an inverted left aligned right-angled triangle of stars.

### Program
```cpp
#include <stdio.h>

int main() {
    int n = 5;
    for (int i = 1; i <= n; i++)
    {
        for (int j = n; j >= i; j--) 
        {
            printf("*");
        }
        printf("\n");
    }
    return 0;
}

```

### Output
```
*****
****
***
**
*
```

---

### [Question 20](#nested-loops)
#### Write a program to print an inverted right-angled triangle of stars with right alignment.

### Program
```cpp
#include <stdio.h>

int main() {
    int n = 5;
    for (int i = 1; i <= n; i++) 
    { 
        for (int j = 1; j < i; j++) // As it is right aligned, I did "<" for printing spaces first, as we dont need to print any space for first iteration, so with the condition, it will skip space for 1st iteration
        {
            printf(" "); // Print Spaces first then stars
        }

        for (int j = n; j >= i ; j--) 
        {
            printf("*");
        }

        printf("\n");
    }
    return 0;
}

```

### Output
```
*****
 ****
  ***
   **
    *
```


---









<h2 align="center">Array</h2>








### [Question 21](#array)
#### Write a program to calculate the sum of all elements in an array.

### Program
```cpp
#include <stdio.h>

int main() {

    int arr[6];  // Array size is 6 as per the input request
    int sum = 0;

    // Taking input elements in array
    printf("Enter 6 elements: ");
    for (int i = 0; i < 6; i++) 
    {
        scanf("%d", &arr[i]);
    }

    for (int i = 0; i < 6; i++) 
    {
        sum += arr[i];  // Add each element to sum
    }

    printf("The sum of all elements in the array is: %d\n", sum);

    return 0;
}

```

### Output
```
Enter 6 elements: 
2 4 6 8 10 12
The sum of all elements in the array is: 42
```


---

### [Question 22](#array)
#### Write a program to find the largest number in an array.

### Program
```cpp
#include <stdio.h>

int main() {

    int arr[5];
    int largest = 0;

    // Taking input elements in array
    printf("Enter 6 elements: ");
    for (int i = 0; i < 6; i++) {
        scanf("%d", &arr[i]);
    }

    largest = arr[0]; // Assume the first element is the largest and then we will check each element

    // Traverse the array to find the largest element
    for (int i = 1; i < 6; i++) {
        if (arr[i] > largest) {
            largest = arr[i];
        }
    }

    printf("The largest number in the array is: %d\n", largest);

    return 0;
}

```

### Output
```
Enter 6 elements: 
2 14 6 87 10 12
The largest number in the array is: 87
```

---

### [Question 23](#array)
#### Write a program to find the smallest number in an array.

### Program
```cpp
#include <stdio.h>

int main() {

    int arr[5];
    int smallest = 0;

    // Taking input elements in array
    printf("Enter 6 elements: ");
    for (int i = 0; i < 6; i++) {
        scanf("%d", &arr[i]);
    }

    smallest = arr[0]; // Assume the first element is the smallest and then we will check each element

    // Traverse the array to find the smallest element
    for (int i = 1; i < 6; i++) {
        if (arr[i] < smallest) {
            smallest = arr[i];
        }
    }

    printf("The smallest number in the array is: %d\n", smallest);

    return 0;
}

```

### Output
```
Enter 6 elements: 
52 4 16 8 10 12
The smallest number in the array is: 4
```


---

### [Question 24](#array)
#### Write a program to count even and odd numbers in an array.

### Program
```cpp
#include <stdio.h>

int main() {

    int arr[6];  // Array size is 6 as per the input request
    int evenCount = 0, oddCount = 0;

    // Taking input elements in array
    printf("Enter 6 elements: ");
    for (int i = 0; i < 6; i++) 
    {
        scanf("%d", &arr[i]);
    }

    for (int i = 0; i < 6; i++) 
    {
        if (arr[i] % 2 == 0)
        {  // Check if the number is even
            evenCount++;
        } else 
        {  // Otherwise, it's odd
            oddCount++;
        }
    }

    // Output the counts of even and odd numbers
    printf("Even numbers count: %d\n", evenCount);
    printf("Odd numbers count: %d\n", oddCount);

    return 0;
}

```

### Output
```
Enter 6 elements: 
2 3 4 5 6 7 8
Even numbers count: 4
Odd numbers count: 3
```


---





<h2 align="center">Sequences</h2>





### **Quick Revision: A.P., G.P., and H.P. Formulas**

| **Concept**                 | **Arithmetic Progression (A.P.)**                                                                       | **Geometric Progression (G.P.)**                                                                          | **Harmonic Progression (H.P.)**                                                                       |
| --------------------------- | ------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| **Definition**              | Difference between terms is constant.                                                                   | Each term is multiplied by a constant ratio.                                                              | Reciprocals of terms form an A.P.                                                                     |
| **n-th Term**               | $T_n = a + (n - 1) \cdot d$                                                                             | $T_n = a \cdot r^{n - 1}$                                                                                 | $T_n = \frac{1}{a + (n - 1) \cdot d}$                                                                 |
| **Sum of First n Terms**    | $S_n = \frac{n}{2} \cdot \left[2a + (n - 1) \cdot d\right]$<br>or<br> $S_n = \frac{n}{2} \cdot (a + l)$ | $S_n = \frac{a(1 - r^n)}{1 - r} \quad \text{for } r \neq 1$<br> $S_n = a \cdot n \quad \text{for } r = 1$ | No direct formula. Use:<br> $S_n = \sum_{k=0}^{n-1} \frac{1}{a + kd}$                                 |
| **First Term (a)**          | Given                                                                                                   | Given                                                                                                     | Reciprocal of the first term of corresponding A.P.                                                    |
| **Common Difference/Ratio** | $d = T_2 - T_1$                                                                                         | $r = \frac{T_2}{T_1}$                                                                                     | Same common difference **d** from related A.P.                                                        |
| **Nature**                  | Linear growth                                                                                           | Exponential growth                                                                                        | Hyperbolic decay                                                                                      |
| **Relation to Others**      | —                                                                                                       | —                                                                                                         | If A.P. is: $a, a+d, a+2d, \ldots$ then H.P. is: $\frac{1}{a}, \frac{1}{a+d}, \frac{1}{a+2d}, \ldots$ |

---

### **Examples Summary**

| **Progression** | **Example**               | **a** | **d / r** | **T₅**               | **Sum of 5 Terms (S₅)**                                                                      |
| --------------- | ------------------------- | ----- | --------- | -------------------- | -------------------------------------------------------------------------------------------- |
| A.P.            | 1, 4, 7, 10, 13           | 1     | 3         | $1 + 4 \cdot 3 = 13$ | $S_5 = \frac{5}{2} \cdot [2 + 4 \cdot 3] = 35$                                               |
| G.P.            | 5, 15, 45, 135, 405       | 5     | 3         | $5 \cdot 3^4 = 405$  | $S_5 = \frac{5(1 - 3^5)}{1 - 3} = 605$                                                       |
| H.P.            | 1/1, 1/4, 1/7, 1/10, 1/13 | 1     | 3         | $\frac{1}{13}$       | $S_5 = \frac{1}{1} + \frac{1}{4} + \frac{1}{7} + \frac{1}{10} + \frac{1}{13} \approx 1.6769$ |



---





### [Question 25](#sequences)

#### Write a program to print the Sequence: 1 4 7 10 ...



### **Identifying the Pattern**

```
1, 4, 7, 10, ...
```

This is an **Arithmetic Progression (A.P.)**, where:

* **First term (a) = 1**
* **Common difference (d) = 3**

Each term is formed by **adding 3 to the previous term**:

* 1 + 3 = 4
* 4 + 3 = 7
* 7 + 3 = 10
* and so on...



### **C Program to Print First `n` Terms of A.P.**

```cpp
#include <stdio.h>

int main() {

    int firstTerm = 1;
    int numberOfTerms;
    int commonDiff = 3; // as 4-1 = 3

    printf("Give number of terms you want to print:\n");
    scanf("%d", &numberOfTerms);

    int currentTerm = firstTerm; // We will print series from first term onwards. 

    for(int i = 1; i <= numberOfTerms; i++) // "i" defines how many times this loop will execute.... in our case it will execute up to "numberOfTerms"
    {
        printf("%d ", currentTerm);
        currentTerm = currentTerm + commonDiff; // after each iteration, we will get next term by adding common difference to current term like, "1 + 3 = 4", "4 + 3 = 7", "7 + 3 = 10", and so on...
    }

    return 0;
}

```



### **Example:**

**Input:**

```
Give number of terms you want to print:
5
```

**Output:**

```
1 4 7 10 13
```









---

### [Question 26](#sequences)

#### Write a program to print the series: 5 15 45 ...

### **Identifying the Pattern**

```
5, 15, 45, ...
```

This is a **Geometric Progression (G.P.)**, not an arithmetic progression.

Each term is multiplied by **3**:

* 5 × 3 = 15
* 15 × 3 = 45
* and so on...

So this is a **geometric sequence** with:

* **First term (a) = 5**
* **Common ratio (r) = 3**


### **C Program to Print First `n` Terms**

```cpp
#include <stdio.h>

int main() {
    // this pattern is same as shown in Question 25

    int a = 5;           // First term
    int r = 3;           // Common ratio... as ratio of two consecutive terms is: "15 / 5 = 3" also "45 / 15 = 3" and so on...
    int n;               // Number of terms

    printf("Enter number of terms: ");
    scanf("%d", &n);

    int currentTerm = a;

    for (int i = 0; i < n; i++) {
        printf("%d ", currentTerm);
        currentTerm = currentTerm * r;  // after each iteration, we will get next term by multiplying common ratio to current term like, "5 * 3 = 15", "15 * 3 = 45", "45 * 3 = 135" and so on...
    }

    return 0;
}

```


### **Example:**

**Input:**

```
Enter number of terms: 5
```

**Output:**

```
5 15 45 135 405
```

---






### [Question 27](#sequences)

#### Write a program to print the Sequence: 1/1, 1/4, 1/7, 1/10, ...


### **What is Harmonic Progression (HP)?**

A **Harmonic Progression (H.P.)** is a sequence where the **reciprocals** of the terms form an **Arithmetic Progression (A.P.)**.



### **Understanding with an Example:**

If the A.P. is:

```
1, 1.5, 2, 2.5, ...
```

Then the corresponding **H.P.** becomes:

```
1/1, 1/1.5, 1/2, 1/2.5 → 1, 0.666..., 0.5, 0.4...
```

So:

* If A.P. is: `a, a + d, a + 2d, ...`
* Then H.P. is: `1/a, 1/(a + d), 1/(a + 2d), ...`


### **C Program to Print First `n` Terms of an H.P.**

```cpp
#include <stdio.h>

int main() {
    int a = 1;         // first term of the underlying A.P.
    int b = 4;         // second term of the A.P.
    int d = b - a;     // common difference
    int n;

    printf("Enter number of terms: ");
    scanf("%d", &n);

    int currentTerm = a;

    printf("Harmonic Progression: ");
    for (int i = 1; i <= n; i++) {
        printf("1/%d", currentTerm);

        if (i < n) {
            printf(", ");
        }

        currentTerm += d;
    }

    return 0;
}

```


### **Example Input:**

```
Enter number of terms: 5
```

**Output:**

```
1/1, 1/4, 1/7, 1/10, 1/13
```

---








### [Question 28](#sequences)

#### Write a program to print the sum of sequence: 1, 4, 7, 10, ...


### **Formula to Find the Sum of A.P.**

If you know:

* **First term (a)**
* **Common difference (d)**
* **Number of terms (n)**

Then the **sum of the first `n` terms** is:

$$
\text{Sum} = \frac{n}{2} \times \left[2a + (n - 1) \times d\right]
$$

Or:

$$
\text{Sum} = \frac{n}{2} \times (\text{first term} + \text{last term})
$$


### **C Program to Calculate and Print the Sum of an A.P.**

```cpp
#include <stdio.h>

int main() {
    int a, d, n;

    printf("Enter first term (a): ");
    scanf("%d", &a);

    printf("Enter common difference (d): ");
    scanf("%d", &d);

    printf("Enter number of terms (n): ");
    scanf("%d", &n);

    int sum = (n * (2 * a + (n - 1) * d)) / 2;

    printf("The sum of the A.P. is: %d\n", sum);

    return 0;
}

```


### **Example Input:**

```
a = 1
d = 3
n = 5
```

The A.P. is: `1, 4, 7, 10, 13`


### **Output:**

```
The sum of the A.P. is: 35
```

---







### [Question 29](#sequences)

#### Write a program to print the sum of sequence: 5, 15, 45, 135, ...


### **Sum of the first `n` terms of a G.P.:**

If you know:

* **First term (a)**
* **Common ratio (r)**
* **Number of terms (n)**

Then the sum of the first `n` terms is:

$$
S_n = \frac{a(1 - r^n)}{1 - r} \quad \text{(for } r \neq 1\text{)}
$$

For **r = 1**, the sum becomes:

$$
S_n = a \times n
$$


### **C Program to Calculate and Print the Sum of a G.P.**

```cpp
#include <stdio.h>
#include <math.h>  // for power function (pow)

int main() {
    int a = 5;           // First term
    int r = 3;           // Common ratio
    int n;               // Number of terms

    printf("Enter number of terms: ");
    scanf("%d", &n);

    // Calculate the sum of the first 'n' terms of the G.P.
    double sum = 0;

    if (r == 1) {
        // If r = 1, the sum is just a * n
        sum = a * n;
    } else {
        // Use the sum formula for G.P.
        sum = a * (1 - pow(r, n)) / (1 - r);
    }

    // Print the sum
    printf("The sum of the G.P. is: %.2lf\n", sum);

    return 0;
}

```


### **Example Input:**

```
Enter number of terms: 5
```

The G.P. is: `5, 15, 45, 135, 405`

### **Output:**

```
The sum of the G.P. is: 605
```

---




<h2 align="center">Exercise</h2>


### [Question 30](#exercise)
#### Write output of the program.

### Program

```cpp

#include <stdio.h>

int func(int n) {
    static int x = 0;
    if (n > 0) {
        x++;
        return func(n - 1) + x;
    }
    return 0;
}

int main() {
    printf("value is: %d\n", func(5));
    return 0;
}


```

### **Working:**

* `x` is a **static variable**, so it retains its value across recursive calls.
* For each recursive call: `x` is incremented, and added on the way back.



### **Recursive Calls Breakdown:**

| Call    | `n` | `x` (after `x++`) | Return value |
| ------- | --- | ----------------- | ------------ |
| func(5) | 5   | 1                 | ?            |
| func(4) | 4   | 2                 | ?            |
| func(3) | 3   | 3                 | ?            |
| func(2) | 2   | 4                 | ?            |
| func(1) | 1   | 5                 | ?            |
| func(0) | 0   | -                 | 0            |

Then it returns (read from bottom to top):

```text

func(5): 14 + 1 = 15
func(4): 12 + 2 = 14
func(3): 9 + 3 = 12
func(2): 5 + 4 = 9
func(1): 0 + 5 = 5
func(0): 0
```

### **Final Output:**

```
value is: 15
```

---



### [Question 31](#exercise)
#### Write output of the program.

### Program

```cpp

#include <stdio.h>

int fun(int n) {
    if (n == 0) return 0;
    return fun(n - 1) + n;
}

int main() {
    int result = fun(5);
    printf("Result: %d\n", result);
    return 0;
}



```

The `int fun(int n)` is a **recursive sum** function.
It adds all numbers from `1` to `n`.



So calling `fun(5)` gives:

```
fun(5) = fun(4) + 5
fun(4) = fun(3) + 4
fun(3) = fun(2) + 3
fun(2) = fun(1) + 2
fun(1) = fun(0) + 1
fun(0) = 0
```

Now unwind:

```
fun(5) = 10 + 5 = 15  
fun(4) = 6 + 4 = 10  
fun(3) = 3 + 3 = 6  
fun(2) = 1 + 2 = 3  
fun(1) = 0 + 1 = 1  
fun(0) = 0

```



### Final Output:

```
Result: 15
```


---




### [Question 32](#exercise)
#### Write output of the program.

### Program

```cpp

#include <stdio.h>

void update(int x) {
    x = x + 5;
    printf("Inside function: %d\n", x);
}

int main() {
    int a = 10;
    update(a++);
    printf("In main: %d\n", a);
    return 0;
}



```

### **Explanation:**

```cpp
int a = 10;
update(a++);
```

* `a++` passes **10** to `update`, because **post-increment** returns the original value before incrementing.
* So `x = 10` inside the function.
* `x + 5 = 15`, so:

  ```cpp
  cout << "Inside function: " << x << endl;  // prints 15
  ```


Here's the exact flow:

1. `a = 10`
2. `update(a++)`

   * `a++` passes `10` (post-increment).
   * After this line, `a` becomes **11**.
3. Inside `update`, `x = 10`, and:

   ```cpp
   x = x + 5 → 10 + 5 = 15
   cout << x → 15
   ```
4. Back in `main`, `cout << a → 11`


### Final Output:

```
Inside function: 15  
In main: 11
```


---








### [Question 33](#exercise)
#### Write output of the program.

### Program

```cpp

#include <stdio.h>

int main() {
    int b = 6;
    b = ++b + b++;
    b = b++ + ++b;
    b = ++b + ++b;
    b = b++ + b++;

    printf("%d", b++);
    printf("b = %d\n", b);
    return 0;
}


```

### **Explanation:**

**Initial value:**

```cpp
int b = 6;
```



### Step 1:

```cpp
b = ++b + b++;
```

Evaluate:

* `++b` → pre-increment: `b = 7`, value used = 7
* `b++` → post-increment: value used = 7, then `b = 8`

So:

```
b = 7 + 7 = 14   // Now b is 14 (but internally, b was incremented after the post-increment)
```



### Step 2:

```cpp
b = b++ + ++b;
```

Now `b = 14`

Evaluate:

* `b++` → value used = 14, then `b = 15`
* `++b` → pre-increment: `b = 16`, value used = 16

So:

```
b = 14 + 16 = 30
```



### Step 3:

```cpp
b = ++b + ++b;
```

Now `b = 30`

Evaluate:

* First `++b` → `b = 31`, value used = 31
* Second `++b` → `b = 32`, value used = 32

So:

```
b = 31 + 32 = 63
```



### Step 4:

```cpp
b = b++ + b++;
```

Now `b = 63`

Evaluate:

* First `b++` → value used = 63, then `b = 64`
* Second `b++` → value used = 64, then `b = 65`

So:

```
b = 63 + 64 = 127
```

Now `b = 127`, but behind the scenes it's been incremented twice, so final value is:

```
b = 127
```



### Final Output:

```cpp
cout << b++;           // 127
cout << "b = " << b; // b = 128
```

---





### [Question 34](#exercise)
#### Write output of the program.

### Program

```cpp

#include <stdio.h>

int main() {
    int a = 5;
    int b = a++ + ++a + a++ + ++a;

    printf("a: %d\n", a);
    printf("b: %d\n", b);

    return 0;
}


```


### **Explanation:**

```cpp
int a = 5;
int b = a++ + ++a + a++ + ++a;
```

Initial value:

* `a = 5`

Now let's evaluate `b = a++ + ++a + a++ + ++a` in **left-to-right order**:



### Step-by-step:

| Expression | Action         | Value Used        | New Value of `a` |
| ---------- | -------------- | ----------------- | ---------------- |
| `a++`      | Post-increment | `5`               | `a = 6`          |
| `++a`      | Pre-increment  | `7` (a becomes 7) | `a = 7`          |
| `a++`      | Post-increment | `7`               | `a = 8`          |
| `++a`      | Pre-increment  | `9` (a becomes 9) | `a = 9`          |

Now sum those values:

```cpp
b = 5 + 7 + 7 + 9 = 28
```



### Final Result:

```cpp
a: 9
b: 28
```

---



### [Question 35](#exercise)
#### Write output of the program.

### Program

```cpp

#include <stdio.h>

int* getReference() {
    static int x = 10;
    x += 5;
    return &x;
}

int main() {
    int a = *getReference();
    *getReference() = 50;

    printf("a: %d\n", a);
    printf("getReference(): %d\n", *getReference());

    return 0;
}


```

This one tests your understanding of:

* `static` variables
* Returning by **reference**
* Assignment to a function call


### **Explanation:**


```cpp
int& getReference() {
    static int x = 10;
    x += 5;              // x = x + 5
    return x;            // returns reference to x
}
```


### **Step-by-Step Execution:**

1. **`int a = getReference();`**

   * `x = 10 → x += 5 → x = 15`
   * `a = 15` (copies value)

2. **`getReference() = 50;`**

   * Function called again:

     * `x = 15 → x += 5 → x = 20`
   * But then `= 50` sets `x = 50` (because it returns a reference)

3. **`getReference()`**

   * Function called again:

     * `x = 50 → x += 5 → x = 55`
   * So, prints `55`



### Final Output:

```
a: 15
getReference(): 55
```

---









