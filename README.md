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

int main() {
    float num = 23.65;
    float *ptr = &num;
    printf("Original value: %.2f\n", num);
    *ptr = 25.0;
    printf("Modified value: %.2f\n", num);
    return 0;
}

```

## OUTPUT:
 	

![Screenshot 2025-05-21 083048](https://github.com/user-attachments/assets/39d2e3e1-8591-4064-982b-d2630f4a3291)










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
unsigned long long calculateProduct(int n) {
    if (n == 1)
        return 1;
    else
       return n * calculateProduct(n - 1);
}
int main() {
    int n;
    unsigned long long product;
    n = 12;
    product = calculateProduct(n);
    printf("The product of the first 12 natural numbers is: %llu\n", product);
    return 0;
}

```
## OUTPUT:
![Screenshot 2025-05-21 083259](https://github.com/user-attachments/assets/faeb2d2f-c804-455a-b88d-609389a99eb6)

           
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
 #include<stdio.h>
 int main()
 {
   int m,n,i,j;
   scanf("%d %d",&m,&n);
   int arr[m][n];
   for (i=0;i<m;i++){
       for (j=0;j<n;j++){
          scanf("%d",&arr[i][j]);
       }
   }
   printf("Sum of each row:\n");
   for (i=0;i<m;i++){
       int sum=0;
       for (j=0;j<n;j++){
           sum+=arr[i][j];
       }
       printf("Row %d sum = %d\n",i+1,sum);
    }
    return 0;
 }
```


## OUTPUT

![Screenshot 2025-05-21 084951](https://github.com/user-attachments/assets/a4c9079e-6e34-4c85-94bc-f97cddcbe6af)

 
 

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
    int num_rows, i, j, k, midpoint;
    printf("Enter a string: ");
    scanf("%s", str);
    printf("Enter number of rows: ");
    scanf("%d", &num_rows);

    int len = strlen(str);
    midpoint = (2 * num_rows - 1) / 2;  
    for (i = 1; i <= num_rows; i++) {
        for (j = 1; j <= num_rows - i; j++) {
            printf(" ");
        }
        for (k = 0; k < (2 * i - 1); k++) {
            printf("%c", str[k % len]);
        }

        printf("\n");
    }

    return 0;
}
```


 ## OUTPUT

![Screenshot 2025-05-28 110220](https://github.com/user-attachments/assets/7da6aff6-6738-4e6f-9bb6-b55d92d50111)



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
    int i, n;
    int arr[10];
    int *parr = arr;
    
    printf("Enter the number of elements: ");
    scanf("%d", &n);
    
    printf("Enter %d elements:\n", n);
    for (i = 0; i < n; i++) {
        scanf("%d", parr + i);
    }
    
    printf("The elements in the array are:\n");
    for (i = 0; i < n; i++) {
        printf("%d ", *(parr + i));
    }
    printf("\n");
    
    return 0;
}
```

## OUTPUT

![Screenshot 2025-06-02 164508](https://github.com/user-attachments/assets/16501be0-400f-4f8a-a964-cc552ed11fc3)

 

## RESULT

Thus the C program to read and display an array of any 6 integer elements using pointer has been executed


