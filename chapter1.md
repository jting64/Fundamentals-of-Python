---
title       : Chapter 1-Basic Python Syntax
description : You will 
attachments :
  slides_link : https://s3.amazonaws.com/assets.datacamp.com/course/teach/slides_example.pdf

---
## test
```yaml
type: NormalExercise
lang: python
xp: 50
skills: 1
key: 82e7247ef1
---
## Lesson 1.1-Getting Started

```yaml
type: NormalExercise
lang: python
xp: 50
skills: 1
key: 954c87ad6f
```

Run the code on the side to see what happen, these are some of the things you will learn in chapter 1.

`@instructions`
- basic syntax
- variables
- operators
- tabbing

`@hint`
Press run

`@sample_code`
```{python}
chapter = '1'
def printChapter():
    print('this is chapter ' + chapter)
printChapter()
```

`@solution`
```{python}
chapter = '1'
def printChapter():
    print('this is chapter ' + chapter)
printChapter()
```

`@sct`
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki

success_msg("Now you had a look of what python codes look like, continue to the next lesson to learn more about the details.")
```

---
## Lesson 1.2-How to write codes in Python

```yaml
type: NormalExercise
lang: python
xp: 50
skills: 1
key: c51dca99b3
```

Each line of code in python act as a command. It tells the computer what to do. These code may come in many different forms, each of them has their own functions. It may be to perform an action(a function), saving datas(variables), or creating an objects(classes). Try typing the function `print('Hello World')` into the editor on the side and see what happen.

`@instructions`
- type `print('Hello World')` in the editor

`@hint`
type print('Hello World') in the editor

`@solution`
```{python}
print('Hello World')
```

`@sct`
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki
test_output_contains('Hello World', pattern=False, no_output_msg='Did you type the correct text in the editor? Your output is a bit off.')
success_msg("Great Job! Head on to the next chapter to see more details.")
```
---

## Lesson 1.3-How to write codes in Python(2)
```yaml
type: NormalExercise
lang: python
xp: 50
skills: 1
key: '6062184654'
```

the `print()` function you used in the last exercise is a "function" it tells your computer what to do. A function in python takes in an arguement which should be entered between the parentheses. In this case, the `print()` function takes in a text and display it to the screen.

`@instructions`
- use the `print()` function to display your name on the screen

`@hint`
type print("your name")

`@solution`
```{python}
print('name')
```

`@sct`
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki
test_output_contains('\w+', pattern=True, no_output_msg='Did you type the correct text in the editor? Your output is a bit off.')
success_msg("Great Job! Head on to the next chapter to see what are variables.")
```
---

## Lesson 2-variables
```yaml
type: NormalExercise
lang: python
xp: 50
skills: 1
key: b700af6d53
```

A variable is a way to store datas in python. You can name the value you want to store to make your coding process more efficient and readable. There are many types of variables, each of them function in different ways by storing different types of value. These types of values include integers, floating point numbers(number with decimal places), strings, arrays...etc. In this lesson, you will learn how to declare and use a variable.

`@instructions`
- print out the value of the variables by typing their names into the `print()` function

`@hint`
print out `1` by using `print(integer_variable)`
print out `Hi` by using `print(string_variable)`
print out `0.1` by using `print(float_variable)`

`@sample_code`
```{python}
integer_variable = 1
string_variable = 'Hi'
float_variable = 0.1

print(___)
print(___)
print(___)
```

`@solution`
```{python}
integer_variable = 1
string_variable = 'Hi'
float_variable = 0.5

print(integer_variable)
print(string_variable)
print(float_variable)
```

`@sct`
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki
test_output_contains("1", pattern=False, no_output_msg="did you typed use the variable \"integer_variable\"?")
test_output_contains("Hi", pattern=False, no_output_msg="did you typed use the variable \"string_variable\"?")
test_output_contains("0.5", pattern=False, no_output_msg="did you typed use the variable \"float_variable\"?")
success_msg("Great Job! Head on to the next chapter to see what are operators.")
```
---
## Lesson 3.1-Operators
```yaml
type: MultipleChoiceExercise
lang: python
xp: 50
skills: 1
key: 381492d879
```

Operators are used for making calculations. Most of the operators are very intuitional, it looks just like the ones we used everyday. For example, `+` represents plus, `-` represents minus, `*` represents multiplying and `/` represents division. You can use `**` for raising a number to a power, for example `a**b` is a raised to the b power. Note that the order of operation still applies even though the compiler reads your code line by line.

what is the output of 12**2+4/2?

`@instructions`
- 146
- 146.0
- 74
- 74.0

`@hint`
type the expression into the python shell to test what the output is.

`@sct`
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki
msg1 = "Division in python 3 always returns a floating point number."
msg2 = "Correct! The .0 at the end indicates that the output is a floating point number. Head on to the next lesson to learn how to combine variables and operators."
msg3 = "Remember that the order of operation still applies, also, division in python 3 always returns a floating point number."
msg4 = "Remember that the order of operation still aplies."
test_mc(2, [msg1, msg2, msg3, msg4])
```

---
## Lesson 3.2-Combining Operators and Variables
```yaml
type: NormalExercise
lang: python
xp: 50
skills: 1
key: '22803e5741'
```
Now that you learned about operators and variables, it is time to combine these two together. It works just like how normal operators on numbers would, however, it has a few more features. You can add a `=` after the operator to assign results to a variable. For example, the expression `a+=b` is equivalent to `a=a+b` and `a/=b` is equivalent to `a=a/b`. 

`@instructions`
use the description above to help you finish the code.

`@hint`

`@sample_code`
```{python}
a = 4
b = 2
# assign the sum of a and b to a new variable called sum_ab
sum_ab = ___
# print out the variable sum_ab
___
# assign the product of a and b to a new variable called product_ab
product_ab = ___
# print out the variable product_ab
___
```

`@solution`
```{python}
a = 4
b = 2
# assign the sum of a and b to a new variable called sum_ab
sum_ab = a + b
# print out the variable sum_ab
print(sum_ab)
# assign the product of a and b to a new variable called product_ab
product_ab = a * b
# print out the variable product_ab
print(product_ab)
```
`@sct`
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki
test_output_contains("6", no_output_msg = "Did you assign the sum of a and b to sum_ab and print it out?", pattern = False)
test_output_contains("8", no_output_msg = "Did you assign the product of a and b to sum_ab and print it out?", pattern = False)
success_msg("Great Work! Head on to the next lesson to do one more exercise on operators and variables")
```

---
### Lesson 3.3-Combining Operators and Variables(2)
```yaml
type: NormalExercise
lang: python
xp: 50
skills: 1
key: ef4bbe63f7
```
Now that you learned about operators and variables, it is time to combine these two together. It works just like how normal operators on numbers would, however, it has a few more features. You can add a `=` after the operator to assign results to a variable. For example, the expression `a+=b` is equivalent to `a=a+b` and `a/=b` is equivalent to `a=a/b`. 

`@instructions`
use the `+=`, `-=`, `*=`, `/=` operator to perform the tasked described.

`@hint`
use `a-=1` or `a=a-1` to minus 1 from the variable a.

`@sample_code`
```{python}
a = 5
# add 5 to the variable a
a __ 5
# print out the variable a
print(__)
a = 5;
# minus 5 to the variable a
a __ 5
# print out the variable a
print(__)
a = 5;
# multiply 5 to the variable a
a __ 5
# print out the variable a
print(__)
a = 5;
# divide a by 5
a __ 5
# print out the variable a
print(__)
```

`@solution`
```{python}
a = 5
# add 5 to the variable a
a += 5
# print out the variable a
print(a)
a = 5;
# minus 5 to the variable a
a -= 5
# print out the variable a
print(a)
a = 5;
# multiply 5 to the variable a
a *= 5
# print out the variable a
print(a)
a = 5;
# divide a by 5
a /= 5
# print out the variable a
print(a)
```
`@sct`
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki
test_student_typed("+=", not_typed_msg = "Did you use the += operator?", pattern = False)
test_student_typed("-=", not_typed_msg = "Did you use the -= operator?", pattern = False)
test_student_typed("*=", not_typed_msg = "Did you use the *= operator?", pattern = False)
test_student_typed("/=", not_typed_msg = "Did you use the /= operator?", pattern = False)
test_output_contains("10", no_output_msg = "Did you use the += operator?", pattern = False)
test_output_contains("0", no_output_msg = "Did you use the += operator?", pattern = False)
test_output_contains("25", no_output_msg = "Did you use the += operator?", pattern = False)
test_output_contains("1", no_output_msg = "Did you use the += operator?", pattern = False)
success_msg("Great Work! Head on to the next lesson to learn about importing")
```


---
## Lesson 4.1-importing modules into python
```yaml
type: NormalExercise
lang: python
xp: 50
skills: 1
key: e88a2f919b
```
There are a lot of built in modules in python you can use to make your code more efficient. However, not all modules are built-in, you have to import a package in order to access some of it. In this lesson, you will learn how to use the `import` command in python with the math module. The `import` keyword imports the module specified after it. Usually, the line of the command is put on the very top of the program. Importing is like declaring a variable, if you do not put it in the very front, it may not be accessible to all of the code.

`@instructions`
`sqrt()` is a function in the `math` module, it is a function tat return the square root of the parameter. However, the module `math` is not defined, so it cannot be accessed. Use `import` to fix the code.

`@hint`
type `import math` at the top of the code

`@sample_code`
```{python}
___
x = 4
y = math.sqrt(x)
print(y)
```

`@solution`
```{python}
import math
x = 4
y = math.sqrt(x)
print(y)
```
`@sct`
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki
test_import("math",not_imported_msg="did you import the math module?", same_as=True)
success_msg("Head on to the next section to learn how to import the math module quicker and easier.")
```
---
## Lesson 4.2-importing modules into python
```yaml
type: NormalExercise
lang: python
xp: 50
skills: 1
key: 242ff20c30
```
When you use an imported module, you have to use the code `module name.function` it is quite inefficient if the module name is too long. Python has a way to increase your effciency. You can import a function using a different name using the keyword `as`. Now you can call the specified funtion by using `specified name.function`.

`@instructions`
`import` the module `math` as `m` and fill in the blanks. Also, take a look at the several math functions.

`@hint`
use `import math as m` to import math using the name `m`. If you want to use a certain function, use `m.function`.

`@sample_code`
```{python}
___
# rasing x to the yth power
x = 5
y = 5
z = ___.pow(x,y)
print(z)

# sine function
x = 0
y = ___.sin(x)
print (y)

# constants
x = ___.e
print(x)

x = ___.pi
print(x)

```

`@solution`
```{python}
import math as m
# rasing x to the yth power
x = 5
y = 5
z = m.pow(x,y)
print(z)

# sine function
x = 0
y = m.sin(x)
print (y)

# constants
x = m.e
print(x)

x = m.pi
print(x)

```
`@sct`
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki
test_import("math", same_as = False, not_imported_msg="did you import the math module?", incorrect_as_msg = "did you import the math module `as m`?")
sucess_msg("Head on to the next section to learn how to import specific functions using from")
```
---
## Lesson 4.3-importing modules into python(3)
```yaml
type: NormalExercise
lang: python
xp: 50
skills: 1
key: 6373db0a3b
```
You can import something contains directly in a module in python using the from command. Remember the `.sqrt()` function used in the previous lesson? It is quite annoying if you have to square a lot of things at a same time, so, you can `import` a function `from` a module using the command `from modulename import function`.

`@instructions`
figure out the code that fits the blank space on the top.

`@hint`
type `from math import sqrt` at the top of the code

`@sample_code`
```{python}
___
x = 5
y = sqrt(x)
print(y)
```

`@solution`
```{python}
from math import sqrt
x = 5
y = sqrt(x)
print(y)

```
`@sct`
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki
test_import("math.sqrt()", same_as = False, not_imported_msg="did you import sqrt from math?" )
success_msg("Great Job, head on to the next section to learn about how to use file I/O")
```
---
## Lesson 5.1 File I/O