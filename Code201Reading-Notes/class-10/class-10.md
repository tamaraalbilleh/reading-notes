# Duckett JS book: Ch. 10 : Error Handling & Debugging
## order of execution 
*  some tasks cannot complete until another statement or function has been run
* to find the source of an error it helps understanding this order 
## EXECUTION CONTEXTS 
* The JavaScript interpreter uses the concept of execution contexts.
There is one global execution context; plus, each function creates a new
execution context. They correspond to variable scope. 
### execution context 
every statement in JS lives in one of three execution contexts :
1. global context
2. function context 
3. `Eval` context (not shown)
### variable scope
1. global scope 
2. function-level scope
## the stack
* the JS interpreter process one line of code at a time 
* when a statement needs data from another function it stacks the new function on top of the current task
* once the task has been performed , the interpreter can go back to the task in hand
## EXECUTION CONTEXT & HOISTING
Each time a script enters a new execution context, there are two phases
of activity:
1. prepare : creating a new scope and determining the value of this 
2. execute : assigning values to the variables and executing statement 
## UNDERSTANDING SCOPE
* In the interpreter, each execution context has its own va ri ables object
* It holds the variables, functions, and parameters available within it. 
* Each execution context can also access its parent's v a ri ables object. 
* functions in JS have lexical scope : they are linked to the objects that are defined in them
## UNDERSTANDING ERRORS
If a JavaScript statement generates an error, then it throws an exception.
At that point, the interpreter stops and looks for exception-handl ing code.
## ERROR OBJECTS 
Error objects can help you find where your mistakes are
and browsers have tools to help you read them. 
* when an error is created it contains the following properties :
---------------------------------------------
| property    | description                    |
|-------------|-----------------------------|
| name        | type of execution              |
| message     | description                    |
| fileNumber  | Name of the JavaScript file |
| lineNumber | Line number of error |
---------------------------------------
* There are seven types of built-in error objects in
JavaScript. You'll see them on the next two pages:
---------------------------------------------------
| OBJECT | DESCRIPTION |
|--------|-------------|
| Error | Generic error - the other errors are all based upon this error |
| Syntax Error | Syntax has not been followed |
| ReferenceError  | Tried to reference a variable that is not declared/within scope |
| TypeError | An unexpected data type that cannot be coerced |
| Range Error | Numbers not in acceptable range |
| URI Error | encodeURI ().decodeURI(),and similar methods used incorrectly |
| Eval Error  | eva l () function used incorrectly |
 
## HOW TO DEAL WITH ERRORS 
 there are two things you can do with the errors. 
 1. DEBUG THE SCRIPT TO FIX ERRORS
 (debug the code, track down the source of the error,
and fix it. )
 2. HANDLE ERRORS GRACEFULLY
 (You can handle errors gracefully using try, catch,
throw, and f i na 1 ly statements. )
## A DEBUGGING WORKFLOW 
* Try to narrow down where the problem might be, then look for clues. 
## BROWSER DEV TOOLS & JAVASCRIPT CONSOLE
* The JavaScript console will tell you when there is a problem with a script,
where to look for the problem, and what kind of issue it seems to be. 
The JavaScript console is just one of several developer tools that are
found in all modern browsers. 
* The console will show you when there is an
error in your JavaScript. It also displays the line
where it became a problem for the interpreter. 
* Browsers that have a console have a console object, which has several
methods that your script can use to display data in the console.
The object is documented in the Console API. 
## BREAKPOINTS
* You can pause the execution of a script on any
line using breakpoints.
*  Then you can check the
values stored in variables at that point in time. 
* If you set multiple breakpoints, you can step
through them one-by-one to see where values
change and a problem might occur. 
## conditional break-points 
* You can indicate that a breakpoint should be
triggered only if a condition that you specify is
met. The condition can use existing variables. 
* You can create a breakpoint
in your code using just the
debugger keyword. When the
developer tools are open, this
will automatically create a
breakpoint. 
* You can also place the debugger
keyword within a conditional
statement so that it only triggers
the breakpoint if the condition is
met. This is demonstrated in the
code below. 
* It is particularly important to
remember to remove these
statements before your code
goes live as this could stop
the page running if a user has
developer tools open. 
## HANDLING EXCEPTIONS 
If you know your code might fail, use try, catch, and finally.
Each one is given its own code block. 
### try 
First, you specify the code
that you think might throw an
exception within the try block
## CATCH
If the try code block throws an
exception, catch steps in with an
alternative set of code. 
## FINALLY
The contents of the finally
code block will run either
way - whether the try block
succeeded or failed. 
## THROWING ERRORS
If you know something might cause a problem for your script, you can
generate your own errors before the interpreter creates them. 
To create your own error, you use the following line:
`throw new Error( 'message ') ;`
* Being able to throw an error at the time you know
there might be a problem can be better than letting
that data cause errors further into the scrip
* If you try to use a string in a
mathematical operation (other
than in addition), you do not get
an error, you get a special value
called NaN (not a number). 
## COMMON ERRORS
Here is a list of common errors you might find with your scripts.
### go back to the basics 
1. JavaScript is case sensitive so
check your capitalization
2. If you did not use var to declare
the variable, it will be a global
variable
3. If you cannot access a variable's
value, check if it is out of scope
4. Do not use reserved words or
dashes in variable names
5. Check that your single I double
quotes match properly.
6. Check that you have escaped
quotes in variable values.
7. Check in the HTML that values
of your id attributes are unique.
### missed/ extra characters
1. Check that there are no
missing closing braces } or
parentheses ) .
2. Check that there are no commas
inside a , } or , ) by accident.
3. Always use parentheses tosurround a condition that you
are testing.
4. Check the script is not missing
a parameter when calling a
function.
5. undefined is not the same
as nu 11 : nu 11 is for objects,
undefined is for properties,
methods, or variables.
6. Check that your script has
loaded (especially CDN files).
7. Look for conflicts between
different script files. 
### DATA TYPE ISSUES
1. Using= rather than == will assign
a value to a variable, not check
that the values match.
2. If you are checking whether
values match, try to use strict
comparison to check datatypes
at the same time. (Use ===
rather than ==.)
3. Inside a switch statement. the
values are not loosely typed (so
their type will not be coerced).
4. Once there is a match in a switch
statement, all expressions will be
executed until the next br eak or
return statement is executed.
5. The replace() method only
replaces the first match. If you
want to replace all occurrences,
use the global flag.
6. If you are using the parse Int()
method, you might need to pass
a radix (the number of unique
digits including zero used to
represent the number).