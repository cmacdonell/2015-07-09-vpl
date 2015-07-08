---
layout: page
root: ../..
title: Introduction to python
---
## Introduction
In this bootcamp, we are using Wing IDE 101 as our development environment. In Wing, there are two ways that we can write python programs: using the python shell, or by  writing scripts. We'll write our first program using the command line and will then move on to writing our first script. 

## Using the Python shell
Wing IDE provides convenient command line access to python so users can test expressions and execute commands while also working on writing scripts. We will write our first program using it.

Traditionally, the first program one writes when learning a new language is called "hello world" and it is an exercise in displaying the words "hello world" using the programming language. We are going use the print command in python to do this on the python shell. In the python context, print means "display on the screen"

~~~python
>>> print "Hello, world"
~~~

When you type this in and hit enter, the phrase Hello, world appears immediately below the line of code you typed in. You've executed your first python command!

Now, let's set a variable and perform a calculation on it. Variables are set in python by declaring them. Variables are declared by using an equal sign. The variable name appears on the left side of the equals sign and its value appears on the right side. 

~~~python
>>> my_var = 5
~~~

In the above example, the variable is named my_var and it has a value of 5. This variable is stored in memory, so we can now manipulate it. Let's add 2 to my_var. To do so, we reset the value of my_var to be the current value of my_var plus 2:

~~~python
>>> my_var = my_var + 2
~~~

We do not immediately see a result returned to the screen as we need to explicitly tell python to display a result using print.

~~~ python
>>> print my_var
    7    
~~~

Next, let's add some text to our output on the screen to make it more readable. The term for combining two strings is concatenation, which means "to join together". Before we can concatenate my_var with text, however, we need to turn it into a string. Currently, it is an integer, which is a type of number. Variables with numerical data types cannot be concatenated with textual variables (known as strings); they must first be converted to strings using the str() command.

~~~ python
>>> my_var = str(my_var)
~~~

Now that we've converted our variable from an integer into a string, we can concatenate it with some text and print the result. To concatenate, you use the + sign between the two (or more) elements you wish to join. Note that strings must be contained within single or double quotes.

~~~python
>>> print "The value of my_var is currently: " + my_var
    The value of my_var is currently: 7
~~~
Note that the first appearance of the term "my_var" in the above is not replaced with the number 7 (my_var's value). This is because it is contained within the quotes, and thus python treats it as text rather than a variable. The second appearance of my_var is replaced with the number 7 as it is not within quotes and is thus evaluated as a variable by python.

We can combine the last two steps into a single line:

~~~python
>>> print "The value of my_var is currently: " + str(my_var)
    The value of my_var is currently: 7
~~~

## Writing a script
Next, we're going to write a script. Scripts are files that can be saved for reuse. This way, we don't need to type out our calculations and commands every time we want to perform a task. We can write it once and reuse it whenever we need.

Python scripts are saved with the .py extension.
  
### Writing a temperature conversion script
Now, let's write a script that converts a temperature from Celsius to Fahrenheit. First, we will create a variable that contains our temperature in Celsius and we will display it to the screen using print.

~~~ python
celsius = 15
print celsius
~~~
The formula to convert from Celsius to Fahrenheit is Celsius x 2 + 30. The multiplication sign in python is *, not x, so we type out the formula as follows:

~~~ python
celsius = 15

fahrenheit = (celsius * 2) + 30
print fahrenheit
~~~
When we run this script, the number 60 is returned. Now, let's update our script so that instead of just returning this number, the phrase "15 degrees Celsius is 60 degrees Fahrenheit" using our variables. Remember, we need to convert our numeric values into strings before we concatenate them with the text (string) we want to add to our output.

~~~ python
celsius = 15

fahrenheit = (celsius * 2) + 30
print str(celsius)+' degrees in Celsius is ' + str(fahrenheit) + ' degrees in Fahrenheit'
~~~

Currently, our variable celsius isn't actually very variable - it doesn't change! It has a "hard coded" value of 15. We can increase the usefulness of our program if we can make this variable more dynamic. For example, we could let a user input any number and we can perform the Celsius to Fahrenheit conversion on it.

To do so, we need to edit our celsius variable. Rather than setting it to the number 5, we will tell python that we want it to be a inputted number by using the input() function.

~~~ python
celsius = input()

fahrenheit = (celsius * 2) + 30
print str(celsius) + " degrees in Celsius is " + str(fahrenheit) + " degrees in Fahrenheit"
~~~

We can further improve our script by adding a textual message to our user prompt. To do so, we add the string we want to display to the user within the brackets of the input() function:

~~~ python
celsius = input("Enter a temperature in Celsius: ")

fahrenheit = (celsius * 2) + 30
print str(celsius) + " degrees in Celsius is " + str(fahrenheit) + " degrees in Fahrenheit"
~~~