# Math In Programming
## Prime Number
- Those numbers which have only two factors that is 1 and itself then these type of numbers are called as Prime Number
- **Brut Force Method For Finding A Number Is Prime Or Not** - 
	- Run loop from 2 to n -1, if the number is divisible by one of them then return true else false
- **Optimized Way**-
	- Let suppose you are checking that 40 is prime or not 
	- Then Factors are
	-  1 * 40
	-  2 * 20
	-  4 * 10
	-  5 * 8
	-  8 * 5
	-  10 * 4
	-  20 * 2
	-  40 * 1
- If you look carefully the same numbers are repeating after 5 * 8, so we can ignore these 
- Again it will get repeating after the square root of the given number, so if we run our loop till the square root of N then we will optimize our program
- Before it takes **n**  time and after that it will take **square root of N**
- **Finding All Prime Number Between Two Number**-
	- We already talked about the optimized way to find out the number is prime or not and we can easily apply the same formula in this but can we optimize this more ?
	- Yes we can, if you 
	- Suppose you are finding all the prime number between 0 to 40, then if 2 is a prime number then all the multiple between 40 are eliminated because these are not prime numbers, similarly if 3 is a prime then all the multiple of 3 are not prime number numbers
	- Again suppose you are eliminating all the multiple of 2 then you will notice that you are also eliminating some multiple of 3 and 5 also, so this process helps to reduce the time complexity but it will take an array that's why its space complexity is O(n).
	![[{7D485A0A-AAF2-4921-87AC-5DC8447D9BBF}.png 1.jpg]]
	- **Time Complexity**-
		- How many elements are between 40 which is divisible by 2 ? Ana:-20, simple math
		- Similarly for 3, 40/3 , for 5 40/5 and so on till the largest prime number between the interval
		- (n/2 + n/3 + n/5 + n/7 + ..... + n/p), p is the largest prime number in the range
		- n(1/2 + 1/3 + 1/5 + .... 1/p) here **(1/2 + 1/3 + 1/5 ....) is the harmonic progression for the prime** and time complexity is **log(log(n))**
		- so total time complexity is **O(n *  log(log n))**
## Newton-Raphson Method
- **Equation**
	- *root = (x + N/x) / 2*
	- Here **root** is the actual root of the number that you entered and x is the square root that you assumed
- **Why This Formula Worked ?**
	- Let suppose your guess is correct then it becomes *( sqrt(n) +(n / sqrt(n)) ) / 2 = sqrt(n)*, here the equation gets satisfied
	- Basically here we are trying to minimize the error, then **What is error ?** it basically **abs value of( root -  x )**,  and here  x is given number
	- so we are keep changing the value of x till the error becomes minimum
	- let suppose your error is less than 1 or 0.5 or 0.2 according to your desire , return the answer
	- Remember that if you minimize the error bound then more number of steps are required to find out the root
## Factors Of A Number
- **Brut Force Method**- 
	- Run the loop from 1 to n, and divide each number with n, if the reminder is 0 then print that otherwise skip
	- its time complexity is O(n)
- **Optimized Way**-
	- We can apply the same prime number trick to optimize this 
	- But hear we have to take a extra space that is a array
## Modulus Properties
- **(a + b) % m** = ((a % m) + (b % m)) % m
- **(a - b) % m** = ((a % m) - (b % m)) % m
- **(a * b) % m** = ((a % m) * (b % m)) % m
- **(a / b) % m** = ((a % m) - (b^-1 % m)) % m ***(b^-1 = b inverse)*** & ***(b^-1 % m  = Multiplicative Modulo Inverse)***
- **(a % m) % m** = (a % m)
- **(m ^ x % m)** = 0 (for all x belongs to positive integer)
## Die Hard Example
- 