/*---------------------------------------------------------------------------
              All problem solved by "Prashanta Chowdhury"
                    **problem_solved_in_C ** 
             100 Programin problem solved using C
------------------------------------------------------------------------*/
#include <stdio.h>
#include <stdlib.h>
#include <math.h>
#include <string.h>

// 1. Hello World
int main() {
    printf("Hello, World!\n");
    return 0;
}

// 2. Sum of two numbers
int add(int a, int b) {
    return a + b;
}

// 3. Subtract two numbers
int subtract(int a, int b) {
    return a - b;
}

// 4. Multiply two numbers
int multiply(int a, int b) {
    return a * b;
}

// 5. Divide two numbers
float divide(int a, int b) {
    if (b == 0) {
        printf("Error: Division by zero!\n");
        return 0;
    }
    return (float)a / (float)b;
}

// 6. Find the maximum of two numbers
int findMax(int a, int b) {
    return (a > b) ? a : b;
}

// 7. Find the minimum of two numbers
int findMin(int a, int b) {
    return (a < b) ? a : b;
}

// 8. Calculate the square of a number
int square(int a) {
    return a * a;
}

// 9. Calculate the cube of a number
int cube(int a) {
    return a * a * a;
}

// 10. Check if a number is even
int isEven(int num) {
    return (num % 2 == 0);
}

// 11. Check if a number is odd
int isOdd(int num) {
    return (num % 2 != 0);
}

// 12. Calculate the factorial of a number
int factorial(int n) {
    if (n == 0) return 1;
    return n * factorial(n - 1);
}

// 13. Check if a number is prime
int isPrime(int n) {
    if (n <= 1) return 0;
    if (n <= 3) return 1;
    if (n % 2 == 0 || n % 3 == 0) return 0;
    for (int i = 5; i * i <= n; i += 6) {
        if (n % i == 0 || n % (i + 2) == 0) return 0;
    }
    return 1;
}

// 14. Find the GCD of two numbers
int findGCD(int a, int b) {
    if (b == 0) return a;
    return findGCD(b, a % b);
}

// 15. Calculate the power of a number
double power(double base, int exponent) {
    return pow(base, exponent);
}

// 16. Find the square root of a number
double squareRoot(double num) {
    if (num < 0) {
        printf("Error: Cannot calculate square root of a negative number!\n");
        return 0;
    }
    return sqrt(num);
}

// 17. Calculate the average of an array of numbers
double calculateAverage(int arr[], int n) {
    if (n == 0) return 0;
    int sum = 0;
    for (int i = 0; i < n; i++) {
        sum += arr[i];
    }
    return (double)sum / n;
}

// 18. Find the maximum element in an array
int findMaxInArray(int arr[], int n) {
    if (n == 0) return 0;
    int max = arr[0];
    for (int i = 1; i < n; i++) {
        if (arr[i] > max) {
            max = arr[i];
        }
    }
    return max;
}

// 19. Find the minimum element in an array
int findMinInArray(int arr[], int n) {
    if (n == 0) return 0;
    int min = arr[0];
    for (int i = 1; i < n; i++) {
        if (arr[i] < min) {
            min = arr[i];
        }
    }
    return min;
}

// 20. Reverse an array
void reverseArray(int arr[], int n) {
    if (n <= 1) return;
    int left = 0;
    int right = n - 1;
    while (left < right) {
        int temp = arr[left];
        arr[left] = arr[right];
        arr[right] = temp;
        left++;
        right--;
    }
}

// 21. Check if a string is a palindrome
int isPalindrome(char str[]) {
    int length = strlen(str);
    for (int i = 0; i < length / 2; i++) {
        if (str[i] != str[length - i - 1]) {
            return 0;
        }
    }
    return 1;
}

// 22. Calculate the length of a string
int stringLength(char str[]) {
    int length = 0;
    while (str[length] != '\0') {
        length++;
    }
    return length;
}

// 23. Copy one string into another
void stringCopy(char dest[], char src[]) {
    int i = 0;
    while (src[i] != '\0') {
        dest[i] = src[i];
        i++;
    }
    dest[i] = '\0';
}

// 24. Concatenate two strings
void stringConcatenate(char dest[], char src[]) {
    int destLength = stringLength(dest);
    int i = 0;
    while (src[i] != '\0') {
        dest[destLength + i] = src[i];
        i++;
    }
    dest[destLength + i] = '\0';
}

// 25. Compare two strings
int stringCompare(char str1[], char str2[]) {
    int i = 0;
    while (str1[i] != '\0' || str2[i] != '\0') {
        if (str1[i] != str2[i]) {
            return str1[i] - str2[i];
        }
        i++;
    }
    return 0;
}

// 26. Find the index of a substring in a string
int findSubstring(char str[], char substr[]) {
    int strLen = stringLength(str);
    int substrLen = stringLength(substr);
    for (int i = 0; i <= strLen - substrLen; i++) {
        int j;
        for (j = 0; j < substrLen; j++) {
            if (str[i + j] != substr[j]) {
                break;
            }
        }
        if (j == substrLen) {
            return i;
        }
    }
    return -1; // Substring not found
}

// 27. Find the factorial of a number using a loop
int factorialLoop(int n) {
    int result = 1;
    for (int i = 2; i <= n; i++) {
        result *= i;
    }
    return result;
}

// 28. Calculate the sum of natural numbers up to n
int sumOfNaturalNumbers(int n) {
    return (n * (n + 1)) / 2;
}

// 29. Check if a year is a leap year
int isLeapYear(int year) {
    return ((year % 4 == 0 && year % 100 != 0) || (year % 400 == 0));
}

// 30. Convert temperature from Celsius to Fahrenheit
double celsiusToFahrenheit(double celsius) {
    return (celsius * 9.0 / 5.0) + 32.0;
}

// 31. Convert temperature from Fahrenheit to Celsius
double fahrenheitToCelsius(double fahrenheit) {
    return (fahrenheit - 32.0) * 5.0 / 9.0;
}

// 32. Find the area of a rectangle
double rectangleArea(double length, double width) {
    return length * width;
}

// 33. Find the area of a triangle
double triangleArea(double base, double height) {
    return 0.5 * base * height;
}

// 34. Find the area of a circle
double circleArea(double radius) {
    return 3.14159265358979323846 * radius * radius;
}

// 35. Find the perimeter of a rectangle
double rectanglePerimeter(double length, double width) {
    return 2.0 * (length + width);
}

// 36. Find the perimeter of a triangle
double trianglePerimeter(double side1, double side2, double side3) {
    return side1 + side2 + side3;
}

// 37. Find the circumference of a circle
double circleCircumference(double radius) {
    return 2.0 * 3.14159265358979323846 * radius;
}

// 38. Check if a number is a palindrome
int isNumberPalindrome(int num) {
    int originalNum = num;
    int reversedNum = 0;
    while (num > 0) {
        int digit = num % 10;
        reversedNum = reversedNum * 10 + digit;
        num /= 10;
    }
    return (originalNum == reversedNum);
}

// 39. Find the sum of digits of a number
int sumOfDigits(int num) {
    int sum = 0;
    while (num > 0) {
        int digit = num % 10;
        sum += digit;
        num /= 10;
    }
    return sum;
}

// 40. Find the product of digits of a number
int productOfDigits(int num) {
    int product = 1;
    while (num > 0) {
        int digit = num % 10;
        product *= digit;
        num /= 10;
    }
    return product;
}

// 41. Find the reverse of a number
int reverseNumber(int num) {
    int reversedNum = 0;
    while (num > 0) {
        int digit = num % 10;
        reversedNum = reversedNum * 10 + digit;
        num /= 10;
    }
    return reversedNum;
}

// 42. Find the number of digits in a number
int numberOfDigits(int num) {
    int count = 0;
    while (num > 0) {
        num /= 10;
        count++;
    }
    return count;
}

// 43. Find the sum of an arithmetic series
int sumOfArithmeticSeries(int firstTerm, int lastTerm, int commonDifference) {
    int n = (lastTerm - firstTerm) / commonDifference + 1;
    return n * (firstTerm + lastTerm) / 2;
}

// 44. Find the sum of a geometric series
double sumOfGeometricSeries(double firstTerm, double commonRatio, int n) {
    if (commonRatio == 1) {
        return firstTerm * n;
    } else {
        return firstTerm * (1 - pow(commonRatio, n)) / (1 - commonRatio);
    }
}

// 45. Check if a number is Armstrong
int isArmstrong(int num) {
    int originalNum = num;
    int n = numberOfDigits(num);
    int sum = 0;
    while (num > 0) {
        int digit = num % 10;
        sum += pow(digit, n);
        num /= 10;
    }
    return (originalNum == sum);
}

// 46. Find the LCM of two numbers
int findLCM(int a, int b) {
    return (a * b) / findGCD(a, b);
}

// 47. Find the sum of digits of a factorial
int sumOfFactorialDigits(int n) {
    int fact = factorial(n);
    return sumOfDigits(fact);
}

// 48. Find the product of digits of a factorial
int productOfFactorialDigits(int n) {
    int fact = factorial(n);
    return productOfDigits(fact);
}

// 49. Generate Fibonacci series up to n terms
void generateFibonacci(int n) {
    int a = 0, b = 1, c;
    printf("Fibonacci series up to %d terms: ", n);
    for (int i = 0; i < n; i++) {
        printf("%d ", a);
        c = a + b;
        a = b;
        b = c;
    }
    printf("\n");
}

// 50. Calculate the average of two numbers
double averageOfTwoNumbers(double a, double b) {
    return (a + b) / 2.0;
}

// 51. Swap two numbers using a temporary variable
void swapWithTemp(int *a, int *b) {
    int temp = *a;
    *a = *b;
    *b = temp;
}

// 52. Swap two numbers without using a temporary variable
void swapWithoutTemp(int *a, int *b) {
    *a = *a + *b;
    *b = *a - *b;
    *a = *a - *b;
}

// 53. Find the maximum of three numbers
int findMaxOfThree(int a, int b, int c) {
    if (a >= b && a >= c) return a;
    if (b >= a && b >= c) return b;
    return c;
}

// 54. Find the minimum of three numbers
int findMinOfThree(int a, int b, int c) {
    if (a <= b && a <= c) return a;
    if (b <= a && b <= c) return b;
    return c;
}

// 55. Check if a character is a vowel
int isVowel(char ch) {
    ch = tolower(ch);
    return (ch == 'a' || ch == 'e' || ch == 'i' || ch == 'o' || ch == 'u');
}

// 56. Check if a character is a consonant
int isConsonant(char ch) {
    return !isVowel(ch);
}

// 57. Find the ASCII value of a character
int findASCIIValue(char ch) {
    return (int)ch;
}

// 58. Convert a character to uppercase
char toUpperCase(char ch) {
    if (islower(ch)) {
        return ch - 32;
    }
    return ch;
}

// 59. Convert a character to lowercase
char toLowerCase(char ch) {
    if (isupper(ch)) {
        return ch + 32;
    }
    return ch;
}

// 60. Check if a character is a digit
int isDigit(char ch) {
    return (ch >= '0' && ch <= '9');
}

// 61. Check if a character is an alphabet
int isAlphabet(char ch) {
    return (ch >= 'a' && ch <= 'z') || (ch >= 'A' && ch <= 'Z');
}

// 62. Calculate the sum of n natural numbers using a loop
int sumOfNaturalNumbersLoop(int n) {
    int sum = 0;
    for (int i = 1; i <= n; i++) {
        sum += i;
    }
    return sum;
}

// 63. Calculate the sum of the first n odd natural numbers
int sumOfOddNaturalNumbers(int n) {
    int sum = 0;
    for (int i = 1; i <= 2 * n; i += 2) {
        sum += i;
    }
    return sum;
}

// 64. Calculate the sum of the first n even natural numbers
int sumOfEvenNaturalNumbers(int n) {
    int sum = 0;
    for (int i = 2; i <= 2 * n; i += 2) {
        sum += i;
    }
    return sum;
}

// 65. Calculate the sum of the squares of n natural numbers
int sumOfSquares(int n) {
    int sum = 0;
    for (int i = 1; i <= n; i++) {
        sum += i * i;
    }
    return sum;
}

// 66. Calculate the sum of the cubes of n natural numbers
int sumOfCubes(int n) {
    int sum = 0;
    for (int i = 1; i <= n; i++) {
        sum += i * i * i;
    }
    return sum;
}

// 67. Check if a number is a perfect number
int isPerfectNumber(int num) {
    int sum = 1;
    for (int i = 2; i * i <= num; i++) {
        if (num % i == 0) {
            if (i * i != num) {
                sum = sum + i + num / i;
            } else {
                sum = sum + i;
            }
        }
    }
    return (num == sum);
}

// 68. Check if a number is a strong number
int isStrongNumber(int num) {
    int originalNum = num;
    int sum = 0;
    while (num > 0) {
        int digit = num % 10;
        sum += factorial(digit);
        num /= 10;
    }
    return (originalNum == sum);
}

// 69. Check if a number is a palindrome
int isPalindromeNumber(int num) {
    int originalNum = num;
    int reversedNum = 0;
    while (num > 0) {
        int digit = num % 10;
        reversedNum = reversedNum * 10 + digit;
        num /= 10;
    }
    return (originalNum == reversedNum);
}

// 70. Calculate the sum of natural numbers divisible by 3 or 5 below n
int sumOfMultiples(int n) {
    int sum = 0;
    for (int i = 1; i < n; i++) {
        if (i % 3 == 0 || i % 5 == 0) {
            sum += i;
        }
    }
    return sum;
}

// 71. Find the number of digits in an integer
int numberOfDigitsInInteger(int num) {
    int count = 0;
    while (num != 0) {
        num /= 10;
        count++;
    }
    return count;
}

// 72. Check if a number is positive, negative, or zero
void checkNumber(int num) {
    if (num > 0) {
        printf("Positive\n");
    } else if (num < 0) {
        printf("Negative\n");
    } else {
        printf("Zero\n");
    }
}

// 73. Find the sum of all even numbers in an array
int sumOfEvenNumbers(int arr[], int n) {
    int sum = 0;
    for (int i = 0; i < n; i++) {
        if (arr[i] % 2 == 0) {
            sum += arr[i];
        }
    }
    return sum;
}

// 74. Find the sum of all odd numbers in an array
int sumOfOddNumbers(int arr[], int n) {
    int sum = 0;
    for (int i = 0; i < n; i++) {
        if (arr[i] % 2 != 0) {
            sum += arr[i];
        }
    }
    return sum;
}

// 75. Count the number of even and odd elements in an array
void countEvenOdd(int arr[], int n) {
    int evenCount = 0, oddCount = 0;
    for (int i = 0; i < n; i++) {
        if (arr[i] % 2 == 0) {
            evenCount++;
        } else {
            oddCount++;
        }
    }
    printf("Even numbers: %d\n", evenCount);
    printf("Odd numbers: %d\n", oddCount);
}

// 76. Find the second largest element in an array
int secondLargest(int arr[], int n) {
    if (n < 2) {
        printf("Array size should be at least 2\n");
        return -1;
    }
    int largest = arr[0];
    int secondLargest = arr[1];
    for (int i = 2; i < n; i++) {
        if (arr[i] > largest) {
            secondLargest = largest;
            largest = arr[i];
        } else if (arr[i] > secondLargest && arr[i] != largest) {
            secondLargest = arr[i];
        }
    }
    return secondLargest;
}

// 77. Find the second smallest element in an array
int secondSmallest(int arr[], int n) {
    if (n < 2) {
        printf("Array size should be at least 2\n");
        return -1;
    }
    int smallest = arr[0];
    int secondSmallest = arr[1];
    for (int i = 2; i < n; i++) {
        if (arr[i] < smallest) {
            secondSmallest = smallest;
            smallest = arr[i];
        } else if (arr[i] < secondSmallest && arr[i] != smallest) {
            secondSmallest = arr[i];
        }
    }
    return secondSmallest;
}

// 78. Find the sum of diagonal elements of a matrix
int sumOfDiagonalElements(int mat[][3], int n) {
    int sum = 0;
    for (int i = 0; i < n; i++) {
        sum += mat[i][i];
    }
    return sum;
}

// 79. Find the product of diagonal elements of a matrix
int productOfDiagonalElements(int mat[][3], int n) {
    int product = 1;
    for (int i = 0; i < n; i++) {
        product *= mat[i][i];
    }
    return product;
}

// 80. Transpose a matrix
void transposeMatrix(int mat[][3], int n) {
    int temp;
    for (int i = 0; i < n; i++) {
        for (int j = i + 1; j < n; j++) {
            temp = mat[i][j];
            mat[i][j] = mat[j][i];
            mat[j][i] = temp;
        }
    }
}

// 81. Check if a matrix is symmetric
int isSymmetricMatrix(int mat[][3], int n) {
    for (int i = 0; i < n; i++) {
        for (int j = i + 1; j < n; j++) {
            if (mat[i][j] != mat[j][i]) {
                return 0;
            }
        }
    }
    return 1;
}

// 82. Find the sum of all elements in a matrix
int sumOfMatrixElements(int mat[][3], int n, int m) {
    int sum = 0;
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < m; j++) {
            sum += mat[i][j];
        }
    }
    return sum;
}

// 83. Multiply two matrices
void multiplyMatrices(int mat1[][3], int mat2[][3], int result[][3], int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            result[i][j] = 0;
            for (int k = 0; k < n; k++) {
                result[i][j] += mat1[i][k] * mat2[k][j];
            }
        }
    }
}

// 84. Find the largest element in a matrix
int findLargestInMatrix(int mat[][3], int n, int m) {
    int largest = mat[0][0];
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < m; j++) {
            if (mat[i][j] > largest) {
                largest = mat[i][j];
            }
        }
    }
    return largest;
}

// 85. Find the smallest element in a matrix
int findSmallestInMatrix(int mat[][3], int n, int m) {
    int smallest = mat[0][0];
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < m; j++) {
            if (mat[i][j] < smallest) {
                smallest = mat[i][j];
            }
        }
    }
    return smallest;
}

// 86. Find the number of rows and columns in a matrix
void findRowsColumns(int mat[][3], int *rows, int *columns) {
    *rows = sizeof(mat) / sizeof(mat[0]);
    *columns = sizeof(mat[0]) / sizeof(mat[0][0]);
}

// 87. Find the average of all elements in a matrix
double averageOfMatrixElements(int mat[][3], int n, int m) {
    int sum = 0;
    int count = 0;
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < m; j++) {
            sum += mat[i][j];
            count++;
        }
    }
    return (double)sum / count;
}

// 88. Check if a matrix is identity
int isIdentityMatrix(int mat[][3], int n) {
    for (int i = 0; i < n; i++) {
        for (int j = 0; j < n; j++) {
            if ((i == j && mat[i][j] != 1) || (i != j && mat[i][j] != 0)) {
                return 0;
            }
        }
    }
    return 1;
}

// 89. Find the number of vowels and consonants in a string
void countVowelsConsonants(char str[], int *vowels, int *consonants) {
    *vowels = 0;
    *consonants = 0;
    for (int i = 0; str[i] != '\0'; i++) {
        if (isAlphabet(str[i])) {
            if (isVowel(str[i])) {
                (*vowels)++;
            } else {
                (*consonants)++;
            }
        }
    }
}

// 90. Count the number of words in a string
int countWords(char str[]) {
    int words = 0;
    int isWord = 0; // Indicates whether we are inside a word
    for (int i = 0; str[i] != '\0'; i++) {
        if (isAlphabet(str[i])) {
            if (!isWord) {
                isWord = 1;
                words++;
            }
        } else {
            isWord = 0;
        }
    }
    return words;
}

// 91. Reverse a string
void reverseString(char str[]) {
    int length = strlen(str);
    for (int i = 0; i < length / 2; i++) {
        char temp = str[i];
        str[i] = str[length - i - 1];
        str[length - i - 1] = temp;
    }
}

// 92. Check if a string is a palindrome
int isPalindromeString(char str[]) {
    int length = strlen(str);
    for (int i = 0; i < length / 2; i++) {
        if (str[i] != str[length - i - 1]) {
            return 0;
        }
    }
    return 1;
}

// 93. Find the length of a string
int stringLength(char str[]) {
    int length = 0;
    while (str[length] != '\0') {
        length++;
    }
    return length;
}

// 94. Copy one string into another
void stringCopy(char dest[], char src[]) {
    int i = 0;
    while (src[i] != '\0') {
        dest[i] = src[i];
        i++;
    }
    dest[i] = '\0';
}

// 95. Concatenate two strings
void stringConcatenate(char dest[], char src[]) {
    int destLength = stringLength(dest);
    int i = 0;
    while (src[i] != '\0') {
        dest[destLength + i] = src[i];
        i++;
    }
    dest[destLength + i] = '\0';
}

// 96. Compare two strings
int stringCompare(char str1[], char str2[]) {
    int i = 0;
    while (str1[i] != '\0' || str2[i] != '\0') {
        if (str1[i] != str2[i]) {
            return str1[i] - str2[i];
        }
        i++;
    }
    return 0;
}

// 97. Find the index of a substring in a string
int findSubstringIndex(char str[], char substr[]) {
    int strLen = stringLength(str);
    int substrLen = stringLength(substr);
    for (int i = 0; i <= strLen - substrLen; i++) {
        int j;
        for (j = 0; j < substrLen; j++) {
            if (str[i + j] != substr[j]) {
                break;
            }
        }
        if (j == substrLen) {
            return i;
        }
    }
    return -1; // Substring not found
}

// 98. Convert a string to an integer
int stringToInteger(char str[]) {
    int num = 0;
    int sign = 1;
    int i = 0;
    if (str[0] == '-') {
        sign = -1;
        i = 1;
    }
    while (str[i] != '\0') {
        num = num * 10 + (str[i] - '0');
        i++;
    }
    return num * sign;
}

// 99. Convert an integer to a string
void integerToString(int num, char str[]) {
    int i = 0;
    int isNegative = 0;
    if (num < 0) {
        isNegative = 1;
        num = -num;
    }
    while (num > 0) {
        str[i] = num % 10 + '0';
        num /= 10;
        i++;
    }
    if (isNegative) {
        str[i] = '-';
        i++;
    }
    str[i] = '\0';
    reverseString(str);
}

// 100. Calculate the power of a number using a loop
double powerWithLoop(double base, int exponent) {
    double result = 1.0;
    for (int i = 0; i < exponent; i++) {
        result *= base;
    }
    return result;
}

int main() {
    // Example usage of the above functions
    printf("1. Hello World\n");
    printf("2. Sum of 5 and 7: %d\n", add(5, 7));
    printf("3. 7 minus 3: %d\n", subtract(7, 3));
    printf("4. 6 times 8: %d\n", multiply(6, 8));
    printf("5. 20 divided by 4: %.2f\n", divide(20, 4));
    printf("6. Maximum of 9 and 12: %d\n", findMax(9, 12));
    printf("7. Minimum of 15 and 10: %d\n", findMin(15, 10));
    printf("8. Square of 5: %d\n", square(5));
    printf("9. Cube of 3: %d\n", cube(3));
    printf("10. Is 4 even? %s\n", isEven(4) ? "Yes" : "No");
    printf("11. Is 9 odd? %s\n", isOdd(9) ? "Yes" : "No");
    printf("12. Factorial of 5: %d\n", factorial(5));
    printf("13. Is 11 prime? %s\n", isPrime(11) ? "Yes" : "No");
    printf("14. GCD of 18 and 24: %d\n", findGCD(18, 24));
    printf("15. 2 to the power of 3: %.2lf\n", power(2.0, 3));
    printf("16. Square root of 25: %.2lf\n", squareRoot(25));
    int arr[] = {2, 4, 6, 8, 10};
    int n = sizeof(arr) / sizeof(arr[0]);
    printf("17. Average of array: %.2lf\n", calculateAverage(arr, n));
    printf("18. Maximum element in array: %d\n", findMaxInArray(arr, n));
    printf("19. Minimum element in array: %d\n", findMinInArray(arr, n));
    int arr2[] = {1, 2, 3, 4, 5};
    printf("20. Original array: ");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr2[i]);
    }
    reverseArray(arr2, n);
    printf("\n   Reversed array: ");
    for (int i = 0; i < n; i++) {
        printf("%d ", arr2[i]);
    }
    printf("\n");
    char palindromeStr[] = "racecar";
    char nonPalindromeStr[] = "hello";
    printf("21. Is \"%s\" a palindrome? %s\n", palindromeStr, isPalindrome(palindromeStr) ? "Yes" : "No");
    printf("    Is \"%s\" a palindrome? %s\n", nonPalindromeStr, isPalindrome(nonPalindromeStr) ? "Yes" : "No");
    printf("22. Length of \"%s\": %d\n", palindromeStr, stringLength(palindromeStr));
    printf("23. Copying \"%s\" into another string: ", palindromeStr);
    char copiedStr[20];
    stringCopy(copiedStr, palindromeStr);
    printf("%s\n", copiedStr);
    printf("24. Concatenating \"%s\" and \"%s\": ", palindromeStr, nonPalindromeStr);
    char concatenatedStr[20];
    stringConcatenate(concatenatedStr, palindromeStr);
    stringConcatenate(concatenatedStr, nonPalindromeStr);
    printf("%s\n", concatenatedStr);
    printf("25. Comparing \"%s\" and \"%s\": %d\n", palindromeStr, nonPalindromeStr, stringCompare(palindromeStr, nonPalindromeStr));
    printf("26. Index of \"%s\" in \"%s\": %d\n", nonPalindromeStr, concatenatedStr, findSubstring(concatenatedStr, nonPalindromeStr));
    printf("27. Factorial of 6 using loop: %d\n", factorialLoop(6));
    printf("28. Sum of natural numbers up to 10: %d\n", sumOfNaturalNumbersLoop(10));
    printf("29. Is 2020 a leap year? %s\n", isLeapYear(2020) ? "Yes" : "No");
    printf("30. 25 Celsius in Fahrenheit: %.2lf\n", celsiusToFahrenheit(25));
    printf("31. 68 Fahrenheit in Celsius: %.2lf\n", fahrenheitToCelsius(68));
    printf("32. Area of a rectangle with length 6 and width 4: %.2lf\n", rectangleArea(6, 4));
    printf("33. Area of a triangle with base 5 and height 8: %.2lf\n", triangleArea(5, 8));
    printf("34. Area of a circle with radius 3: %.2lf\n", circleArea(3));
    printf("35. Perimeter of a rectangle with length 7 and width 3: %.2lf\n", rectanglePerimeter(7, 3));
    printf("36. Perimeter of a triangle with sides 5, 7, and 9: %.2lf\n", trianglePerimeter(5, 7, 9));
    printf("37. Circumference of a circle with radius 4: %.2lf\n", circleCircumference(4));
    printf("38. Is 121 a palindrome number? %s\n", isNumberPalindrome(121) ? "Yes" : "No");
    printf("39. Sum of digits of 12345: %d\n", sumOfDigits(12345));
    printf("40. Product of digits of 456: %d\n", productOfDigits(456));
    printf("41. Reverse of 98765: %d\n", reverseNumber(98765));
    printf("42. Number of digits in 123456789: %d\n", numberOfDigits(123456789));
    printf("43. Sum of the arithmetic series 2, 4, 6, ..., 100: %d\n", sumOfArithmeticSeries(2, 100, 2));
    printf("44. Sum of the geometric series 3, 9, 27, ..., 729: %.2lf\n", sumOfGeometricSeries(3.0, 3.0, 5));
    printf("45. Is 153 a Armstrong number? %s\n", isArmstrong(153) ? "Yes" : "No");
    printf("46. LCM of 12 and 18: %d\n", findLCM(12, 18));
    printf("47. Sum of digits of 5!: %d\n", sumOfFactorialDigits(5));
    printf("48. Product of digits of 7!: %d\n", productOfFactorialDigits(7));
    printf("49. Fibonacci series up to 10 terms: ");
    generateFibonacci(10);
    printf("50. Average of 9 and 12: %.2lf\n", averageOfTwoNumbers(9.0, 12.0));
    int x = 5, y = 10;
    printf("51. Before swapping: x=%d, y=%d\n", x, y);
    swapWithTemp(&x, &y);
    printf("    After swapping with temp: x=%d, y=%d\n", x, y);
    swapWithoutTemp(&x, &y);
    printf("    After swapping without temp: x=%d, y=%d\n", x, y);
    printf("52. Maximum of 8, 12, and 7: %d\n", findMaxOfThree(8, 12, 7));
    printf("53. Minimum of 15, 9, and 13: %d\n", findMinOfThree(15, 9, 13));
    printf("54. Is 'A' a vowel? %s\n", isVowel('A') ? "Yes" : "No");
    printf("    Is 'b' a vowel? %s\n", isVowel('b') ? "Yes" : "No");
    printf("55. Is 'C' a consonant? %s\n", isConsonant('C') ? "Yes" : "No");
    printf("    Is 'e' a consonant? %s\n", isConsonant('e') ? "Yes" : "No");
    printf("56. ASCII value of 'A': %d\n", findASCIIValue('A'));
    printf("57. ASCII value of 'b': %d\n", findASCIIValue('b'));
    printf("58. Convert 'a' to uppercase: %c\n", toUpperCase('a'));
    printf("    Convert 'B' to lowercase: %c\n", toLowerCase('B'));
    printf("59. Is '5' a digit? %s\n", isDigit('5') ? "Yes" : "No");
    printf("    Is 'x' a digit? %s\n", isDigit('x') ? "Yes" : "No");
    printf("60. Is 'A' an alphabet? %s\n", isAlphabet('A') ? "Yes" : "No");
    printf("    Is '4' an alphabet? %s\n", isAlphabet('4') ? "Yes" : "No");
    printf("61. Sum of first 10 natural numbers using loop: %d\n", sumOfNaturalNumbersLoop(10));
    printf("62. Sum of first 10 odd natural numbers: %d\n", sumOfOddNaturalNumbers(10));
    printf("63. Sum of first 10 even natural numbers: %d\n", sumOfEvenNaturalNumbers(10));
    printf("64. Sum of squares of first 5 natural numbers: %d\n", sumOfSquares(5));
    printf("65. Sum of cubes of first 4 natural numbers: %d\n", sumOfCubes(4));
    printf("66. Is 28 a perfect number? %s\n", isPerfectNumber(28) ? "Yes" : "No");
    printf("67. Is 145 a strong number? %s\n", isStrongNumber(145) ? "Yes" : "No");
    printf("68. Is 121 a palindrome number? %s\n", isPalindromeNumber(121) ? "Yes" : "No");
    printf("69. Sum of natural numbers below 20 divisible by 3 or 5: %d\n", sumOfMultiples(20));
    printf("70. Number of digits in 12345: %d\n", numberOfDigitsInInteger(12345));
    printf("71. Check if -7 is positive, negative, or zero: ");
    checkNumber(-7);
    printf("72. Sum of even numbers in {2, 4, 6, 8, 10}: %d\n", sumOfEvenNumbers(arr, n));
    printf("73. Sum of odd numbers in {2, 4, 6, 8, 10}: %d\n", sumOfOddNumbers(arr, n));
    printf("74. Count of even and odd numbers in {2, 4, 6, 8, 10}: ");
    countEvenOdd(arr, n);
    int arr3[] = {5, 9, 1, 11, 7};
    int m = sizeof(arr3) / sizeof(arr3[0]);
    printf("75. Second largest element in {5, 9, 1, 11, 7}: %d\n", secondLargest(arr3, m));
    printf("76. Second smallest element in {5, 9, 1, 11, 7}: %d\n", secondSmallest(arr3, m));
    int mat1[3][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
    printf("77. Sum of diagonal elements in the matrix:\n");
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            printf("%d ", mat1[i][j]);
        }
        printf("\n");
    }
    printf("    Sum: %d\n", sumOfDiagonalElements(mat1, 3));
    int mat2[3][3] = {{1, 0, 0}, {0, 2, 0}, {0, 0, 3}};
    printf("78. Product of diagonal elements in the matrix:\n");
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            printf("%d ", mat2[i][j]);
        }
        printf("\n");
    }
    printf("    Product: %d\n", productOfDiagonalElements(mat2, 3));
    printf("79. Transpose of the matrix:\n");
    int mat3[3][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
    transposeMatrix(mat3, 3);
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            printf("%d ", mat3[i][j]);
        }
        printf("\n");
    }
    printf("80. Is the matrix symmetric:\n");
    int mat4[3][3] = {{1, 2, 3}, {2, 4, 5}, {3, 5, 6}};
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            printf("%d ", mat4[i][j]);
        }
        printf("\n");
    }
    printf("    %s\n", isSymmetricMatrix(mat4, 3) ? "Yes" : "No");
    printf("81. Sum of all elements in the matrix:\n");
    int mat5[2][3] = {{1, 2, 3}, {4, 5, 6}};
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 3; j++) {
            printf("%d ", mat5[i][j]);
        }
        printf("\n");
    }
    printf("    Sum: %d\n", sumOfMatrixElements(mat5, 2, 3));
    int mat6[2][3] = {{1, 2, 3}, {4, 5, 6}};
    int result[2][3];
    printf("82. Multiplication of two matrices:\n");
    printf("    Matrix A:\n");
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 3; j++) {
            printf("%d ", mat6[i][j]);
        }
        printf("\n");
    }
    int mat7[3][2] = {{1, 2}, {3, 4}, {5, 6}};
    printf("    Matrix B:\n");
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 2; j++) {
            printf("%d ", mat7[i][j]);
        }
        printf("\n");
    }
    multiplyMatrices(mat6, mat7, result, 2);
    printf("    Result:\n");
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 2; j++) {
            printf("%d ", result[i][j]);
        }
        printf("\n");
    }
    int mat8[2][2] = {{3, 7}, {2, 8}};
    printf("83. Largest element in the matrix:\n");
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 2; j++) {
            printf("%d ", mat8[i][j]);
        }
        printf("\n");
    }
    printf("    Largest element: %d\n", findLargestInMatrix(mat8, 2, 2));
    printf("84. Smallest element in the matrix:\n");
    int mat9[2][2] = {{9, 4}, {6, 1}};
    for (int i = 0; i < 2; i++) {
        for (int j = 0; j < 2; j++) {
            printf("%d ", mat9[i][j]);
        }
        printf("\n");
    }
    printf("    Smallest element: %d\n", findSmallestInMatrix(mat9, 2, 2));
    printf("85. Number of rows and columns in the matrix:\n");
    int rows, columns;
    findRowsColumns(mat6, &rows, &columns);
    printf("    Rows: %d, Columns: %d\n", rows, columns);
    int mat10[3][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}};
    printf("86. Average of all elements in the matrix:\n");
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            printf("%d ", mat10[i][j]);
        }
        printf("\n");
    }
    printf("    Average: %.2lf\n", averageOfMatrixElements(mat10, 3, 3));
    printf("87. Is the matrix identity:\n");
    int mat11[3][3] = {{1, 0, 0}, {0, 1, 0}, {0, 0, 1}};
    for (int i = 0; i < 3; i++) {
        for (int j = 0; j < 3; j++) {
            printf("%d ", mat11[i][j]);
        }
        printf("\n");
    }
    printf("    %s\n", isIdentityMatrix(mat11, 3) ? "Yes" : "No");
    char str1[] = "Hello, World!";
    int vowels, consonants;
    printf("88. Count of vowels and consonants in \"%s\":\n", str1);
    countVowelsConsonants(str1, &vowels, &consonants);
    printf("    Vowels: %d, Consonants: %d\n", vowels, consonants);
    char str2[] = "This is a sample sentence.";
    printf("89. Number of words in \"%s\": %d\n", str2, countWords(str2));
    char str3[] = "abcdefg";
    printf("90. Reverse of \"%s\": ", str3);
    reverseString(str3);
    printf("%s\n", str3);
    char str4[] = "racecar";
    printf("91. Is \"%s\" a palindrome? %s\n", str4, isPalindromeString(str4) ? "Yes" : "No");
    printf("92. Length of \"%s\": %d\n", str4, stringLength(str4));
    char str5[] = "Copy me!";
    char str6[20];
    printf("93. Copying \"%s\" into another string: ", str5);
    stringCopy(str6, str5);
    printf("%s\n", str6);
    char str7[] = "Concatenate ";
    char str8[] = "me!";
    printf("94. Concatenating \"%s\" and \"%s\": ", str7, str8);
    stringConcatenate(str7, str8);
    printf("%s\n", str7);
    char str9[] = "hello";
    char str10[] = "world";
    printf("95. Comparing \"%s\" and \"%s\": %d\n", str9, str10, stringCompare(str9, str10));
    char str11[] = "This is a sample string.";
    char substr1[] = "sample";
    printf("96. Index of \"%s\" in \"%s\": %d\n", substr1, str11, findSubstringIndex(str11, substr1));
    char str12[] = "12345";
    printf("97. Converting \"%s\" to integer: %d\n", str12, stringToInteger(str12));
    int num1 = -567;
    char str13[20];
    printf("98. Converting %d to string: ", num1);
    integerToString(num1, str13);
    printf("%s\n", str13);
    printf("99. 2 to the power of 5 using loop: %.2lf\n", powerWithLoop(2.0, 5));
    return 0;
}


