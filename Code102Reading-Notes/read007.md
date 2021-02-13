# Operators and Loops
## Comparison and logical operators
### comparison operators 
* you can evaluate a situation by comparing **one value** in the script to what you expect it might be.
* the result will be a **boolean** : *true* or *false*
now lets look at those operators:

| operator   |  meaning  | function
:-------------|:-------------| :-------------
|== | equal to  | compares 2 values to see if they are the same
|!= | not equal to  | compares 2 values to see if they are not the same
|===| strict equal to  | compares 2 values to check that both data type and value are the same
|!==| strict not equal to  | compares 2 values to check that both data type and value are not the same
|> | greater than  | checkes if the number on the left is greater than the number on the right
|< | less than  | checkes if the number on the left is less than the number on the right
|>= | greater than or equal to  | checkes if the number on the left is greater than or equal to the number on the right
|<= | less than or equal to  | checkes if the number on the left is less than or equal to the number on the right

***
***
### logical operators
* comparison operators usually return single valuew of *true* or *false*
* they allow you to compare the results of more than one comparison operator

![img](/read007p/Capture1.PNG)

| operator   |  meaning  | number of conditions tested| function
:-------------|:-------------| :-------------|:-------------
|&& | AND  | more than one condition |T+T=T ,T+F=F ,F+T=F ,F+F=F
| ![OR](/read007p/D1.PNG) | OR| at least one condition | T+T=T ,T+F=T ,F+T=T ,F+F=F
| ! | NOT | Single boolean value | !T=F , !F=T |
***
***
## LOOPS
* loops check a condition. if it returns true, a code block will run .
* the condition will be checked again and it it still true, the code block will reun again.
* it repeats until the condition refurns false 
### common types of loops
1. ### for
if you want to run a code a specific number of times

* a for loop uses a counter as a condition. 
* it imstructs the code to run a specific number of times.


here you can see the condition is made up of three statments :

![IMG5](/read007p/D5.PNG)
* The variable is only created the first time the loop is run
* the value of i was initially set to 0
so in this case it'll run 10 times before stopping
* one is added to the counter using the incremment (++)
![img6](/read007p/D6.PNG)
![img7](/read007p/D7.PNG)

***
2. ### While 
if you don't know how many times the code should run

3. ### Do While
similer to while loop, but runs the statment inside the curly braces at least once even if the condition evaluates to false

![img4](/read007p/D4.PNG)

***
***
### USING WHILE LOOPS 
Here is an example of awhil e
loop. It writes out the 5 times table. Each time the loop is run, another calculation is written
into the variable called msg. 
![IMG2](/read007p/D2.PNG)
![IMG3](/read007p/D3.PNG)