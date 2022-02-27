## 90-Java Script Runtime
- it is a big box or big container that includes all the things that we needed to use java script 
- and the heart of any java script engine is the java script run time
- again java script engine is not enough, we also need web apis (dom, timer, fetch api etc) to work properly 
- Web apis are the functionalities that is provided to the js but this is not a part of js, js access it through the global window object
- again js run time also include the call back queue, this is a data structure that contain all the call back function that to be executed 
- all the event handler function like click, timer etc called as call back function, so as the event happens for example click, then it first pushed into the callback queue and then when the call stack is empty the call back function is passed to the stack so that it can be executed and this happen by something called the event loop
- again remember that js can exist outside of the browser, for example node js but we cant have web apis because we dont have browser, instead we have multiple so called bindings and a thread pool
## 91-Execution Context And The Call Stack
- Execution context is nothing but the activation record that we studied already
- remember that all the global variable are belongs to one execution context and this is the bottom most execution context inside the call stack 
- the global execution context stays inside the call stack until you close the current web tab
## 92-Scope And Scope Chain
- There are three types of scope in js, global scope, function scope and the block scope
- scope chain is nothing but the order in which functions are written in the code
- variables are accessible only inside block called block scoped 
- however this is only applies to let and const variable means if you declare a variable using the keyword var then it can be accessed outside of the block that's why we say var is function scoped
- in ES5 we have function scope and global scope
- **Variable Lookup** - a function finding for a variable which is not declared inside it, so it checks the other parent function or global scope by using the scope chain and this is called as variable lookup
## 93- Scoping Practice
- If you are declaring a function inside a block and you are calling the function outside of the block then it will run but if there is strict mode activated then it will throw an error
- again suppose there are two variable declared of same name, one is in global execution context and another one is inside a block and if you are using that variable inside that block then the variable that is declared inside of that block will be used because of scope chain.