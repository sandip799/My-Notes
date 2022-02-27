# Introduction To Algorithm
`what do you mean by algorithm?`
- Algorithm is nothing but a step by step procedure for solving the computational problem..
- Again we know that a program is also a step by step approach to solving a problem...
then what is the difference between these?

| ALGORITHM              | PROGRAM               |
| ---------------------- | --------------------- |
| Design                 | Implementation        |
| Domain Knowledge       | Programming Knowledge |
| Any language           | Programming language  |
| H/W and OS independent | H/W & OS Dependent    | 
| Analyze                | Testing               |
- Lets understand all these concepts, suppose you are working on a project and you have to create a software, `then what do you do ?`
- First you have to gain knowledge about the project which you are working on,if you have't any knowledge about this then you should find a person who know about all these so that he can write the algorithm.
- So here we question arises if i am a programmer then can i write algorithm? yes you can but you have the proper knowledge about that and you have to draw a blue print of what you will have to implement in future , if you don't draw any diagram or blue print  and direct work on the problem then there is 99% chance that you end up with failure or if you will able to create the software then that will be not efficient...
- So basically design is done by the person which have the knowledge about algorithm with domain knowledge
- Again you can write algorithm in any language but the important thing is it can be understandable by the programmer who will implement this using programming language in future
- As you can write it using pen and paper so this is not hardware and os dependent
- Again you have to analyze the algorithm that this satisfying the requirement or not and it is efficient in terms of time and space or not and after that the programmer will test with different types of input to check how it work when certain types of input is given
	
# Priori & Postreriori
	
| PRIORI ANALYSIS         | POSTERIORI ANALYSIS  |
| ----------------------- | -------------------- |
| Algorithm               | Program              |
| Independent of language | Language dependent   |
| Hardware independent    | Hardware dependent   |
| Time and space function | Watch time and bytes |                        |                      |

- So basically the person who write the algorithm will analyze it deeply and here we talking about time and space function not in nano sec or bytes, that we will analyze in posterier analysis that is while programming
	
# Characteristics of Algorithm
- **INPUT**-Algorithm can take 0 or more output
- **OUTPUT**- Algorithm must generate one output
- **DEFINITENESS**-Every statement should be unambiguous and it should have single and exact meaning , you can't write any statement which is can't be solved, if human can't solve then how we answer our computer
	- **EXAMPLE**- You cannot use root of -1 because it is an unknown value
- **FINITENESS**- Algorithm have some end point, it may be 10 line or 10,000 line but it has some ending point
- **EFFECTIVE**-You can't write unnecessary thing in the algorithm, the objective is it has some purpose in the algorithm or it helps to full fill something but not unnecessary things.
	- **EX**- Suppose you are cooking something and you cut some vegetable but you cant use them so this is unnecessary thing

# How to Write & Analyze an Algorithm
- **Time**- How much time your algorithm will take, and we calculate this using time function
- **Space**- How much memory space it will consume
- **N/W**- Now a days network is more important, so we have to analyze this like is there any unnecessary data transferring in the network, or how to send data so that it will traverse efficiently
- **Power**- Now a days most of the devices are handheld so power consumption is also a important criteria
- **CPU Register**- If you writing software for device driving or system level program then how much CPU Register your algorithm consuming, that is also a important factor

#### Example
- `First question is why we have to analyze the algorithm ?`lets understand this with an example, suppose you have to go to your friends house so at this point you don't analyze that how much money or oil it cost in general but if you working on a project and the aim of this is to make a spaceship which can take you to the mars, then at that time you have to analyze every single details deeply, like this in the field of computer science when write an algorithm for our customer then we have to analyze it deeply so that it should be efficient in time as well as space
- So as we use time function to analyze time in the algorithm so  every simple statement in algorithm takes one unit of time
- and for every one variable we take one word, `why word ?` because we don't know what memory it will cost when it implement in programming language

```c
Algorithm swap (a, b)
{
	temp = a
	a = b
	b = temp
}
```
- this is a simple swap algorithm where time complexity f(n) = 3 units and space complexity s(n) = 3 words and these all are constant so we denote it as O(1), this means order of 1
# Frequency Count Method
```c
Algorithm Multiply (A,B,C)
{
	for (i = 0; i < n; i++) ---------------------> (n + 1)
	{
		for (j = 0; j < n; j++)------------------> (n + 1) * n
		{
			c[i,j] = 0; -------------------------> n * n
			for (k = 0; k < n; k++)--------------> n * (n + 1) * n
			{
				c[i,j] = c[i,j] + A [i, k] * B[k, j];--> n * n * n
			}
		}
	}
}
```
- in the for loop (i < n ) loops for n + 1 times because at last the condition is checked when the loop breaks
- but i = 0 executes only one time and i ++ executes for n times
- and in this example f(n) = O(N^3)