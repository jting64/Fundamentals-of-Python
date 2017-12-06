---
title       : Chapter 1-Basic Python Syntax
description : You will 
attachments :
  slides_link : https://s3.amazonaws.com/assets.datacamp.com/course/teach/slides_example.pdf

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
```
