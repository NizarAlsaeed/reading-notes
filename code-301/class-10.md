# The Call Stack and Debugging

 a call stack is a data structure that uses the Last In, First Out (LIFO) principle to temporarily store and manage function invocation (call).

A call stack is a mechanism for an interpreter to keep track of its place in a script that calls multiple functions — what function is currently being run and what functions are called from within that function:


- When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
- Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
- When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
- If the stack takes up more space than it had assigned to it, it results in a "stack overflow" error.

A stack overflow occurs when there is a recursive function (a function that calls itself) without an exit point. The browser (hosting environment) has a maximum stack call that it can accomodate before throwing a stack error.

#### Types of error messages:

**Reference errors** when you try to use a variable that is not yet declared 

**Syntax errors** 

**Range errors** An array for instance cannot have a negative length, why would you mess with the array length? Some people use it to set an array to empty

**Type errors** this types of errors show up when the types (number, string and so on) you are trying to use or access are incompatible, like accessing a property in an undefined type of variable

#### Debugging

You can add conditional breakpoints by right-clicking a previous set breakpoint, which will make your program stop at that point only if a condition is met.

Another way to see the stack trace at any given point in your code is to just write console.trace() were you want to log it.

The worthiest outcome of using try…catch tough is the fact that your application will keep on running.
check'quokka' to evaluate your code as you type as a Tool to avoid runtime errors.