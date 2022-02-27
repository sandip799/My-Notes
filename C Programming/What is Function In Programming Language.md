//Back-Link [[Function in General]]

# Function In Programming Languages
### Definition
- A function is **a block of organized, reusable code that is used to perform a single, related action**. 
- Functions provide better modularity for your application and a high degree of code reusing

### But Here, The Question is Why Function is Very Important in Programming languages & Why Programming Languages Can't Exist Without Functions?

####  What is Function ?
- A function is a block of code that performs a task. It can be called and times
- You can pass information to a function and it can send information back
- When you call a function, the program will pause the current program and execute the function. 
- The function will be read from top to bottom.
-  Once the function is complete, The program continues to run where it had paused.
-   Every function has a return type, If the function returned a value, that value will be used where the function was called.

Once you define a function, you put code in it just like you would anywhere else in the program. By giving the function a name and defining parameters it should accept, you can pass information to the function and return some result. Functions are re-usable, so once you write one, you can call it anywhere else in your program.

## 1. Function Encapsulates Task
- Introductory programming classes often describe function as a **black box**.
- `Why Blackbox ?` because when a programmer calls a function, they don't care what exactly the code inside it does; they just need the result
- when you write `printf("hello world");` you don't think about how printf function  works internally, you just give input text as parameter and except an output
- encapsulate means we just put all the instruction that is useful for function to work properly and then point it as a unit.

   #### Real Life Example
   - When you are suffering from fever you take medicine, remember that capsule which has small small round elements enclosed or **Encapsulated** in a container

 ## 2. Functions Separate Tasks
 - It divide a programs into small small components that helps to understand the program easily
 - as it splits a big program into multiple components then multiple user can work on a single program

## 3. Functions Let You Reuse Code
- There are many chances that when you write some code to perform a task, you'll use it more than once in your program
- if you copy the same code and paste it then it will be complicated to read, to debug and take more space
- Functions eliminate this problem. They make it easy to reuse code anywhere else in your program.
-  Once you've defined a function, you can call it anytime and be sure that it will run the same way.
-  This saves time and reduces complexity, which are two welcome qualities for a program.

## 4. Functions Enable Easier Shareability
- suppose you are working at a company and every employee uses same programming language then it will be easy to share function
- that saved times because we have to think logic and then writing it, and time is very expensive 

## 5. Functions Make Testing and Debugging Easier
  - Without clear functions, programs jump all over the place. This makes it hard to debug, and a massive pain for someone coming in fresh to understand.
  - so if you use function then it breaks the code so that it helps to easily find out where the error occurs 
  - programmers can use **unit tests** to confirm that these functions work as they should.
  - it increases readability so that a clean set of code goes long way in making it easy to maintain.
    ### Real Life Example
 	 - You notice that when your are new in programming field, you write messy code and when there some error arises then you spent lots of times to find out the error
 	 - again if you are working on a big project and it will take months to be complete then you have to write all the codes in a way that after few days when you analyze this then it will be understandable by you and others who working on that same project.
 	 - so if you use function and if you write all the function names or parameters in understandable way then it will help you in future

## 6. Functions Divide Data and Logic
- functions help you separate the steps from the actual data
- As long as you pass the function parameters it's expecting, it doesn't care what the data is. Each run of that function creates temporary variables and then discards them after it returns a result
- Keeping your important data outside the functions helps prevent unwanted modification. 
- This is a smart step in modern programming.

## 7. Built-In Functions Are Important Too
- no matter which language you're using, you don't have to write functions for basic arithmetic, printing text to the screen, and similar tasks.
-  Can you imagine what a waste of time it would be if you were required to tell the computer how to perform these basic operations?
-  so built in function are very very important 

# Summary
- Now you know why programming languages use functions, and why they're so important. The biggest reasons for including functions all come down to one truth: **functions allow you to break a program into more manageable pieces**. 
- When you do this, your program becomes simpler to manage, easier to test, and apt for reuse.
- Without functions, programs would have loads of duplicate code, wouldn't flow in a logical order, and would have no separation of utility. That would be a nightmare for managing, testing, and debugging.