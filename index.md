# The Basics
## Prelogue

Prepare the class by finishing in datacamp:
* Importing Data in Python (Part 1) ==> Introduction and flat files

Solve Rosalind
* Solve problem 2: Variables and Some Arithmetic.

### Classroom trainings: The basics way to talk in Python3

Variable assignment is very straightforward in Python. Take a look at these examples:

```python
price   = 5
tax     = 1.19
total   = price * tax
welcome = "Welcome to our online shop!"
```

We now have defined four variables: the number (integer) price, the floating-point number (float) tax, the string welcome and the float total, which is defined as the product of price and tax. Python has six basic operations for numbers:


| *Operation*   | *Symbol*      | *Example* |
| ------------- |:-------------:| -----:|
| Addition     | + | 1 + 2 == 3 |
| Subtraction     | -      |  4 - 3 == 1 |
| Multiplication | *      | 5 * 2 == 10 |
| Division     | / | 20 / 4 == 5 |
| Subtraction     | **      | 5 **2 == 25 |
| Multiplication | %      | 14 % 3 == 2 |

Note that the operations described above work on numbers and behave differently (or will not work at all) on strings. In this light you should be aware of the fundamental difference between these two lines (explain what's the difference):

```python
price = 4
price = "4"
```

Printing variables is also easy:

```python
print(welcome)
print("The price without tax is",price,", the price with tax is",total,".")
```

Now it's up to you to try this. Copy the assignment and print statements to pycharm, and save and run the script. Now, change tax to 1.19785. The output would then be:

>Welcome to our online shop! <br />
>The price without tax is 5 , the price with tax is 5.98925 .

```python
print("The price without tax is", price, ", the price with tax is %.2f" % total)
```
Change your script accordingly and run it. Looks better, right? %.2f"%total converts the float total to a string with 2 decimals after the decimal point. Now change your print statement to %10.3f"%total and examine the output.

*Converting integers, floats, etc to a string is done with the % symbol. Integers are converted with %i, floats with %f and strings with %s.* <br />
When printing variables into strings, this often the most readable and efficient route to take. So, our example would end up looking like this:
```python
print("The price without tax is %i, the price with tax is %.2f" % (price, total))
```
If you are not sure what type a value has, the Pyton interpreter can tell you.
```python
type(price)

type(tax
```

### <i class="fas fa-puzzle-piece" aria-hidden="true"></i> Exercise 1
* **Write a program which prints the result of 12 * 14.5782, with only 3 decimals significance. Declare the required variables first!**

### Classroom trainings: Count to 10

This is were the real stuff starts. We have arrived at our first control structure. Normally the computer starts reading at the first line and then goes down from there. Control structures can be used to determine the order in which statements are executed or to decide if a certain statement will be run at all.

The first control structure we will discuss is the socalled while loop. Here is a program that uses it:

```python
i = 0
while i < 10:
    i = i + 1
    print(i)
print("Finished!")
```
First try to predict what the output of this code will be. Then copy and run it to see the output.

Plese note that two lines of the loop are "indented" (contain spaces at the beginning of the line). These lines will be executed as a part of the   while   loop. Following lines without the indentation (  print "Finished!"  ) are "outside" the loop and will be executed after the loop has finished.

A short note on adding something (1 for example) to a variable. It is possible to use a shortcut for this. Instead of typing   i = i + 1  , you can use   i += 1  , which is shorter and therefore more convenient.

Another example that uses a while loop:

```python
number = 1
total = 0
print("Print Number to add to the total.")
print("Enter 0 to quit.")
while number != 0:
    print("Current total = %i."%total)
    response = input("Number? ")
    number = int(response)
    total += number
print("Total = %i" % total)
```

This program starts with total equal to zero, prints the current sum and will then ask the user for a number (using the raw_input) function). User's response will be stored as a string in responsevariable. Subsequently, the response in converted to an integer (int function), which is added to the total. It will continue to do this, as long as number is not equal (that's what != means) to zero. Notice that print "Total total = %i"%total is only run once at the end. The while statement only affects the lines that are indented.

A dangerous side of while loops is that you can very easy generate programs that will run forever:

```python
while 1 == 1:
    print("Help, I'm stuck in a loop!")
```

This program will print it's output untill the heat death of the universe or you stop it... The way to stop it is hit the Control (or Ctrl) button and the 'c' at the same time. This will kill the program.

### <i class="fas fa-puzzle-piece" aria-hidden="true"></i> Exercise 2
* **Write a program like the second example above, but yours will start with a counter at 100 and then ask the user for a number, which it will then subtract from the counter. Your program should continue to do so untill the counter drops below zero.**

For extra information watch: 
[![4 hour video of python with Pycharm](http://img.youtube.com/vi/rfscVS0vtbw/0.jpg)](http://www.youtube.com/watch?v=rfscVS0vtbw)
