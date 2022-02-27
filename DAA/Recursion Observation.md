# Recursion Tricks
- If you are working on a number where in recursion the number gets reduced and you are multiplying all the returning values, then at that time stop the recursion when the base case i.e n == 1
-  Stack Overflow
```java
static void fun(int n) {
	if(n == 0)
		return 0;
	System.out.println(n);
	fun(n--);
}
```
- Sometimes you might need some variables inside the function parameter, at that time make another helper function