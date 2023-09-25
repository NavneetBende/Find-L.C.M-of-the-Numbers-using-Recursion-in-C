# Find-L.C.M-of-the-Numbers-using-Recursion-in-C

Find LCM of the Numbers using Recursion in C
Given two integer inputs num1 and num2, the objective is to write a code to Find LCM of the Numbers using Recursion in C. We recursively call the HCF() function and apply the formula to find the L.C.M of the numbers.

For instance.

Input : num1 = 10, num2 = 15
Output : The LCM of 10 and 15 is 5.
Find LCM of the Numbers using Recursion in C
Find LCM of the Numbers using Recursion in C
The objective of the code is to recursively find the LCM of the two integer inputs values num1 and num2 in C. We define a recursive function LCM() which returns an integer value and takes num1 and num2 as arguments. We define a base case for the code which is satisfied when the the remainder of num1 and num2 dividing smallestcm is 0 respectively. Until the base case is satisfied we recursively call the function and increment the smallestcm value by 1.
Lets try and understand the working of the code using an example. Let the integer inputs be num1 = 2 and num2 = 4. We declare a static variable smallestcm and initialize it as 1. Now we check if smallestcm is divisible by both num1 and num2. If true, we return smallestcm as the output else we increment the smallestcm variable by 1 and recursively call the function lcm(num1, num2). Now the value of smallestcm is 2. We check if it’s divisible by num1 and num2, if true we return smallestcm but as the smallestcm is divisible by num2 we increment smallestcm and recursively call the function again. The whole processes is repeated until the base case is satisfied. 
 

Find LCM of the Numbers using Recursion in C
While loop in C
C Code
Run
#include <stdio.h>

int lcm(int n1, int n2) {
    static int lowestcm = 1;    
    if(lowestcm%n1 == 0 && lowestcm%n2 == 0)
    {
        return lowestcm;
    }
    else
    {
        lowestcm++;
        lcm(n1,n2);
        return lowestcm;
    }
}


int main() {
    int n1 = 4, n2 = 8;
    printf("L.C.M of %d and %d is %d.", n1, n2, lcm(n1, n2));
    return 0;
}
Output
L.C.M of 4 and 8 is 8.
Explanation

The objective of the above code is to recursively find the LCM of the given two integer inputs num1 and num2 in C language. To do so we declare a recursive function which returns an integer value and takes num1 and num2 as arguments. We then set a base case  as, the remainders after dividing num1 and num2 with  smallestcm is 0. if not we call the function again recursively.

The algorithm for the above code is a follows,

Include the required header files using include keyword.
define a function lcm() which returns an integer value and takes num1 and num2 as arguments.
Set a base case which gets satisfied when the remainder after dividing num1 and num2 with the static variable smallestcm is zero repectively.
Until the base case is satisfied, keep calling the recursive function and and increment smallestcm by 1.
Return the smallestcm when the base case is satisfied.
In the int main section initialize all the required variables and print the returned value after calling the lcm(n1,n2) function using printf() function.
The output for the above code is  LCM of 4 and 8 is 8.
