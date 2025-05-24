EX-21-POINTERS
# AIM:
Write a C program to convert a 23.65 into 25 using pointer

## ALGORITHM:
1.	Declare a double variable to hold the floating-point number (23.65).
2.	Declare a pointer to double to point to the address of the variable.
3.	Use the pointer to modify the value to 25.0.
4.	Print the modified value.

## PROGRAM:
``` C
#include <stdio.h>

int main() {
    double num = 23.65;

    double *ptr = &num;

    *ptr = 25.0;

    printf("The modified value is: %.2f\n", num);

    return 0;
}

```

## OUTPUT:

![img1](https://github.com/user-attachments/assets/8be674c2-687d-44e7-b487-5d12ded3b87c)

 	











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
``` C
#include <stdio.h>

unsigned long long calculateProduct(int n) {
    if (n == 1) { 
        return 1;
    }
    return n * calculateProduct(n - 1); 
}

int main() {
    int n = 12;
    unsigned long long product;

    product = calculateProduct(n);

    printf("The product of the first %d natural numbers is: %llu\n", n, product);

    return 0;
}

```
## OUTPUT:

![img2](https://github.com/user-attachments/assets/1caad182-6675-4cb2-aba5-6aeaaec824f6)


         		
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
``` C
#include <stdio.h>

int main() {
    int matrix[3][4] = {
        {1, 2, 3, 4},
        {5, 6, 7, 8},
        {9, 10, 11, 12}
    };
    
    int rows = 3, cols = 4;
    
    for (int i = 0; i < rows; i++) {
        int sum = 0; 
        
        for (int j = 0; j < cols; j++) {
            sum += matrix[i][j];
        }
        
        printf("Sum of row %d: %d\n", i + 1, sum);
    }
    
    return 0;
}

```



## OUTPUT

![img3](https://github.com/user-attachments/assets/1eb1e30b-64d9-4a04-b22e-e32cf1756b9d)



 
 

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
``` C
#include <stdio.h>
#include <string.h>

int main() {
    char str[100];
    int num_rows;

    printf("Enter a string: ");
    scanf("%s",str);

    //printf("Enter number of rows: ");
    //scanf("%d",&num_rows);

    int len = strlen(str);
    int sp=10;
    int k=0;
    int y=0;
    for (int i = 1; i <=5; i++)
	 {
        for (int space = 1; space <= sp; space++)
		 {
            printf(" ");
        }

        for (int j = 0; j<=y; j++)
		 {
            printf("%c", str[k]);
            k++;
            if(str[k]=='\0')
               k=0;
        }

        printf("\n");
      sp-= 1; 
      y+=2;
    }

    return 0;
}


```


 ## OUTPUT

 ![446838829-3c5cf2a9-2613-4b09-8091-b65ca5abcb8d](https://github.com/user-attachments/assets/17b23238-7231-4a2e-a6ae-467563cf2f67)


 

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
``` C
#include <stdio.h>

int main() {
    int arr[10]; 
    int *parr = arr; 
    int n = 6; 

    printf("Enter %d integer elements:\n", n);
    for (int i = 0; i < n; i++) {
        scanf("%d", (parr + i)); 
    }

    printf("You entered:\n");
    for (int i = 0; i < n; i++) {
        printf("%d ", *(parr + i)); 
    }
    printf("\n");

    return 0;
}

```


## OUTPUT

![img5](https://github.com/user-attachments/assets/78dbc27d-0319-412a-93de-3b3251b1df63)


 

## RESULT

Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


