EX-21-POINTERS
# AIM:
Write a C program to convert a 23.65 into 25 using pointer

## ALGORITHM:
1.	Declare a double variable to hold the floating-point number (23.65).
2.	Declare a pointer to double to point to the address of the variable.
3.	Use the pointer to modify the value to 25.0.
4.	Print the modified value.

## PROGRAM:

```
#include <stdio.h>

void round_up(float *num) {
    *num = 25.0f;  
}

int main() {
    float value = 23.65f;
    printf("Original value: %.2f\n", value);

    round_up(&value);

    printf("Modified value: %.2f\n", value);
    return 0;
}
```

## OUTPUT:
 	
![Screenshot 2025-04-28 151350](https://github.com/user-attachments/assets/31f4ddcf-b74a-4af3-ab72-bc2fc37de761)



## RESULT:
Thus the program to convert a 23.65 into 25 using pointer has been executed successfully.
 
 


# EX-22-FUNCTIONS AND STORAGE CLASS

## AIM:

Write a C program to calculate the Product of first 12 natural numbers using Recursion

## ALGORITHM:

1.	Define a recursive function calculateProduct that takes an integer parameter n.
2.	Return n multiplied by the result of the calculateProduct function called with n - 1.
3.	Declare an integer variable n and an unsigned long long variable product.
4.	Initialize n with the value 12 (for the first 12 natural numbers).
5.	Call the calculateProduct function with n and store the result in the product variable.
6.	Print the result, indicating it is the product of the first 12 natural numbers.

## PROGRAM:

```
#include <stdio.h>


unsigned long long product(int n) {
    if (n == 1) {
        return 1; 
    } else {
        return n * product(n - 1); 
    }
}

int main() {
    int n = 12;
    unsigned long long result = product(n);
    
    printf("The product of the first 12 natural numbers is: %llu\n", result);
    
    return 0;
}
```

## OUTPUT:

![Screenshot 2025-04-28 151748](https://github.com/user-attachments/assets/7476ab7c-2393-4920-b10d-89128ffa5233)

         		
## RESULT:

Thus the program has been executed successfully.
 
 


# EX-23-ARRAYS AND ITS OPERATIONS

## AIM:

Write C Program to find Sum of each row of a Matrix

## ALGORITHM:

1.	Declare and initialize the matrix with the desired values.
2.	Create a loop to iterate through each row of the matrix.
3.	Inside the loop, calculate the sum of the elements in each row.
4.	Print the sum for each row.

## PROGRAM:

```
#include <stdio.h>

int main() {
    int rows, cols;

    printf("Enter the number of rows and columns of the matrix: ");
    scanf("%d %d", &rows, &cols);

    int matrix[rows][cols];

    
    printf("Enter the elements of the matrix:\n");
    for (int i = 0; i < rows; i++) {
        for (int j = 0; j < cols; j++) {
            printf("Element [%d][%d]: ", i, j);
            scanf("%d", &matrix[i][j]);
        }
    }

    
    printf("\nSum of each row:\n");
    for (int i = 0; i < rows; i++) {
        int rowSum = 0;
        for (int j = 0; j < cols; j++) {
            rowSum += matrix[i][j];
        }
        printf("Sum of row %d = %d\n", i, rowSum);
    }

    return 0;
}
```

## OUTPUT

![Screenshot 2025-04-28 152458](https://github.com/user-attachments/assets/52d556d6-26e4-4327-b98c-978d6a5358ec)


 ## RESULT
 


# EX-24-STRINGS

## AIM:

Write C program for the below pyramid string pattern. Enter a string: PROGRAM Enter number of rows: 5 P R O G R A M P R O G R A M P R O G R A M

## ALGORITHM:

1.	Input the number of rows for the pyramid (e.g., num_rows).
2.	Initialize variables:i for the row count (starting from 1),j for the character count (starting from 1)
3.	Start a loop for i from 1 to num_rows (for each row of the pyramid).
4.	Calculate the midpoint position as midpoint = (2 * num_rows - 1) / 2.
5.	End the program.

## PROGRAM:

```
#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int rows;

    printf("Enter a string: ");
    scanf("%s", str);

    printf("Enter number of rows: ");
    scanf("%d", &rows);

    int len = strlen(str);

    for (int i = 1; i <= rows; i++) {
      
        for (int j = 0; j < i; j++) {
            for (int k = 0; k < len; k++) {
                printf("%c ", str[k]);
            }
        }
        printf("\n"); 
    }

    return 0;
}
```

 ## OUTPUT

![Screenshot 2025-04-28 152710](https://github.com/user-attachments/assets/ce37e915-6100-46ee-b838-bcae60d11387)
 

## RESULT

Thus the C program to String process executed successfully
 

 
.



# EX -25 –DISPLAYING ARRAYS USING POINTERS
## AIM

Write a c program to read and display an array of any 6 integer elements using pointer

## ALGORITHM
Step 1: Start the program.
Step 2: Declare the following:
•	Integer variable i for iteration.
•	Integer variable n to store the number of elements.
•	Integer array arr[10] to hold up to 10 elements.
•	Integer pointer parr and initialize it to point to the array arr.
Step 3: Read the value of n (number of elements) from the user.
Step 4: Loop from i = 0 to i < n:
•	Read an integer value and store it in the address parr + i using pointer arithmetic.
Step 5: Loop from i = 0 to i < n:
•	Print the element at *(parr + i) using pointer dereferencing.
Step 6: End the program.

## PROGRAM

```
#include <stdio.h>

int main() {
    int arr[6];
    int *ptr;

    ptr = arr; 

    printf("Enter 6 integer elements:\n");
    for (int i = 0; i < 6; i++) {
        scanf("%d", ptr + i);
    }

    
    printf("\nThe array elements are:\n");
    for (int i = 0; i < 6; i++) {
        printf("%d ", *(ptr + i));
    }

    printf("\n");

    return 0;
}
```

## OUTPUT

![Screenshot 2025-04-28 153048](https://github.com/user-attachments/assets/e908b98a-5b18-493b-8f43-4465ec888f08)
 

## RESULT

Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


