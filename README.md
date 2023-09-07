# Prime-Number-using-Recursion-in-C-

Prime Number Using Recursion in C++
Here, in this page we will discuss the program to check a number is prime number using recursion in C++ programming language. We are given with a number and check if it is prime or not. We will discuss both recursive and non-recursive approach to check if a given number is prime or not. A number is prime, if it is divisible by 1 and number itself.

Example :

Input : Number : 34
Output : No
Explanation : 34 is not a prime number, as factors of 34 are 1, 2, 17, 34.
Prime Number Using Recursion in C++
Method 1 (Using Recursion) :
Create a isprime(int n, int i=2), it return bool values)
Base condition will be :
if (n <= 2)    
return (n == 2) ? true : false;
if (n % i == 0)
return false;
if (i * i > n)   
return true;

Otherwise return isprime(n, i+2)
Time and Space Complexity
Time Complexity : O(sqrt(n))
Space Complexity : O(1)
Code to find Prime Number Using Recursion in C++
Run
#include <bits/stdc++.h>
using namespace std;

bool isPrime(int n, int i = 2)
{
    // Base conditions
    if (n <= 2) return (n == 2) ? true : false; if (n % i == 0) return false; if (i * i > n)
       return true;

    return isPrime(n, i + 1);
}

// Driver Program
int main()
{
    int n = 34;
    if (isPrime(n))
       cout << "Prime Number";
    else
       cout << "Not a Prime";

    return 0;
}
Output :

Not a Prime
Related Pages
Finding Number of times x digit occurs in a given input
 
Finding number of integers which has exactly x divisors
 
Smallest element in an array

Power of a Number

Largest element in an array

Method 2 (Using loop) :
Create a isprime(int n), it return bool value.
Run a loop from i=2 to i<= sqrt(n),
Inside the loop if (n%i==0) then return false
Otherwise return true after termination of the for loop.
Time and Space Complexity
Time Complexity :O(sqrt(n))
Space Complexity : O(1)
Code to find Prime Number Using Loop in C++
Run
#include <bits/stdc++.h>
using namespace std;

bool isPrime(int n)
{
   for(int i=2; i<=sqrt(n); i++){
       if(n%i==0)
         return false;
   }

   return true;
}

// Driver Program
int main()
{
   int n = 21;
   if (isPrime(n))
      cout << "Prime Number";
   else
      cout << "Not Prime";

   return 0;
}
Output :

Not a Prime
