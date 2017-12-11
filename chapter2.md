---
title       : Insert the chapter title here
description : Insert the chapter description here
---
## Falling Distance

```yaml
type: NormalExercise
lang: python
xp: 100
key: 105e15156b
```
In this exercise, we will be utilizing all the technques we learn in the chapter and write a program that help us calculate the falling distance of a object using the equation, `d = 0.5*g*t^2`.

The variables in the formula are as follows: d is the distance in meters. g is 9.8, and t is the amount of time, in seconds, that the object has been falling.

Also, we will importing the module `random` in this program and use the function `randint()` that help us generate random numbers.
For expample,  `random.randint(5,10)` will generate an integer between 5 and 10

`@instructions`
- Write a function named `getTime` that generate a number from 1~50 (inclusive).
- Write a function named `fallingDistance` that accepts an objects's falling time (in seconds) as an argument. (The function should return the distance, in meters, that the object has fallen durin that time interval.)
- Write a function named `printDistance` that accepts the distance calculated by `fallingDistance` and print it out in the following format: `Distance = __ meters`. Ex. Distance = 10 meters.

`@hint`
- Use the keyword, `import`, to import a module. Ex. `import math`
- Use the function, `randint()`in th randome module to genertate randome number. Ex. `random.randint(5,10)`
- To define a function use the keyword `def` follow by the name of the function, just like `def Sum()`
- To print the output using the format, simply use `+` to combine them. Ex. print(`x = `+str) will print `x = Hi` if str = Hi. (Note: to combine string with numerical variable type you need to cast it to string by using `str(num)`)

`@sample_code`
```{python}
# Import module needed


# Define the funcion getTime()
 
 
# Define the funcion fallingDistance()


# Define the funcion printDistance()


#Call the function getTime()
t = 

#Call the function fallingDistance()
d = 

#Call the function printDistance()

`@solution`
```{python}
# Import module needed
import random

# Define the funcion getTime()
def getTime():
    return random.randint(1,50)
 
# Define the funcion fallingDistance()
def fallingDistance(t):
    return 0.5*9.8*t**2

# Define the funcion printDistance()
def printDistance(distance):
    return "Distance: "+str(distance)+" meters"

#Call the function getTime()
t = getTime()

#Call the function fallingDistance()
d = fallingDistance(t)

#Call the function printDistance()
printDistance(d)
```

`@sct`
```{python}
# test_import("random", not_imported_msg = "Did you import random?", same_as = True)
# test_function_definition("getTime", arg_names = False, arg_defaults = False)
# test_function_definition("fallingDistance", arg_names = False, arg_defaults = False)
# test_function_definition("printDistance", arg_names = False, arg_defaults = False)
test_function("randint", not_called_msg="Did you call `random.randint()`?", incorrect_msg="Did you call random.randint() with correct arguments?")
# test_function("str",not_called_msg="Did you call str()?")
# test_function("getTime", not_called_msg = "You didn't call the following function: getTime()")
# test_function("fallingDistance", not_called_msg = "You didn't call the following function: fallingDistance()")
# test_function("printDistance", not_called_msg = "You didn't call the following function: printDistance()")
success_msg("Great work!")
```