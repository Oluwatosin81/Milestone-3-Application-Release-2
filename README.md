# Milestone-3-Application-Release-2
#include <stdio.h>  
#include <conio.h>  
#include <math.h>  
#include <stdlib.h>  
   
int addition();
int subtract();
int multiply();
int divide();
int sq();
int sqrt1();
void exit();

int main()
{
    int op;
    do
    { 
        // displays the multiple operation of the calculator
        printf(" Select an operation to perform the calculation in C Calculator: ");
        printf(" \n 1 Addition  \t \t 2 Subtraction \n 3 Multiplication \t 4 Division \n 5 Square \t \t 6 Square Root \n 7 Exit \n \n Please, Make a choice ");

        scanf_s("%d", &op); // accepts a numberic input to choose the operation


        switch (op)
        {
        case 1:
            addition(); /* it call the addition() function to add the given numbers */
            break; // break the function

        case 2:
            subtract(); /* it call the subtract() function to subtract the given numbers */
            break; 

        case 3:
            multiply(); /* it call the multiply() function to multiply the given numbers */
            break; // break the function

        case 4:
            divide(); // it call the divide() function to divide the given numbers
            break; // to break the function

        case 5:
            sq();  // it call the sq() function to square of the given numbers
            break; // to break the function

        case 6:
            sqrt1(); // it call thr sqrt1() function to get the square root of given numbers
            break; // to break the function

        case 7:
            exit(0);  // it call the exit() function to exit from the programm 
            break; 

        default:
            printf(" Something is wrong!! ");
            break;
        }
        printf(" \n \n ********************************************** \n ");
    } while (op != 7);


    return 0;
}
  // function definition
int addition()
{
    int i, sum = 0, num, f_num;    // declare a local variable
    printf(" How many numbers you want to add: ");
    scanf_s("%d", &num);
    printf(" Enter the numbers: \n ");
    for (i = 1; i <= num; i++)
    {
        scanf_s(" %d", &f_num);
        sum = sum + f_num;
    }
    printf(" Total Sum of the numbers = %d", sum);
    return 0;
}
 
// use subtract() function to subtract two numbers
int subtract()
{
    int n1, n2, res;
    printf(" The first number is: ");
    scanf_s("  %d", &n1);
    printf(" The second number is: ");
    scanf_s("  %d", &n2);
    res = n1 - n2;
    printf(" The subtraction of %d - %d is: %d", n1, n2, res);
}

// multiply() function to multiply two numbers
int multiply()
{
    int n1, n2, res;
    printf(" The first number is: ");
    scanf_s("  %d", &n1);
    printf(" The second number is: ");
    scanf_s("  %d", &n2);
    res = n1 * n2;
    printf(" The multiply of %d * %d is: %d", n1, n2, res);
}

// use divide() function to divide two numbers
int divide()
{
    int n1, n2, res;
    printf(" The first number is: ");
    scanf_s("  %d", &n1);
    printf(" The second number is: ");
    scanf_s("  %d", &n2);

    if (n2 == 0)
    {
        printf(" \n Divisor cannot be zero. Please enter another value ");
        scanf_s("%d", &n2);
    }
    res = n1 / n2;
    printf(" \n The division of %d / %d is: %d", n1, n2, res);
}
 
// use sq() function to get the square pf the given number
int sq()
{
    int n1, res;
    printf(" Enter a number to get the Square: ");
    scanf_s("  %d", &n1);

    res = n1 * n1;
    printf(" \n The Square of %d is: %d", n1, res);
}
   
// use sqrt1() function to get the square root of the given number
int sqrt1()
{
    float res;
    int n1;
    printf(" Enter a number to get the Square Root: ");
    scanf_s("  %d", &n1);


    res = sqrt(n1);
    printf(" \n The Square Root of %d is: %f", n1, res);
}
