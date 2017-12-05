---
title       : Chapter 1-Basic Python Syntax
description : You will 
attachments :
  slides_link : https://s3.amazonaws.com/assets.datacamp.com/course/teach/slides_example.pdf

---
## Lesson 1-Getting Started

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
## Lesson 2-How to write codes in Python

```yaml
type: NormalExercise
lang: python
xp: 50
skills: 1
key: b7c3547fdd
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

## Lesson2-How to write codes in Python(2)
```yaml
type: NormalExercise
lang: python
xp: 50
skills: 1
key: 55f46baa23
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
## Plot the movies yourself

```yaml
type: NormalExercise
lang: python
xp: 100
skills: 1
key: 1fc5142c40
```

Do you remember the plot of the last exercise? Let's make an even cooler plot!

A dataset of movies, `movies`, is available in the workspace.

`@instructions`
- The first function, `np.unique()`, uses the `unique()` function of the `numpy` package to get integer values for the movie genres. You don't have to change this code, just have a look!
- Import `pyplot` in the `matplotlib` package. Set an alias for this import: `plt`.
- Use `plt.scatter()` to plot `movies.runtime` onto the x-axis, `movies.rating` onto the y-axis and use `ints` for the color of the dots. You should use the first and second positional argument, and the `c` keyword.
- Show the plot using `plt.show()`.

`@hint`
- You don't have to program anything for the first instruction, just take a look at the first line of code.
- Use `import ___ as ___` to import `matplotlib.pyplot` as `plt`.
- Use `plt.scatter(___, ___, c = ___)` for the third instruction.
- You'll always have to type in `plt.show()` to show the plot you created.

`@pre_exercise_code`
```{python}
import pandas as pd
movies = pd.read_csv("http://s3.amazonaws.com/assets.datacamp.com/course/introduction_to_r/movies.csv")

import numpy as np
```

`@sample_code`
```{python}
# Get integer values for genres
_, ints = np.unique(movies.genre, return_inverse = True)

# Import matplotlib.pyplot


# Make a scatter plot: runtime on  x-axis, rating on y-axis and set c to ints


# Show the plot

```

`@solution`
```{python}
# Get integer values for genres
_, ints = np.unique(movies.genre, return_inverse = True)

# Import matplotlib.pyplot
import matplotlib.pyplot as plt

# Make a scatter plot: runtime on  x-axis, rating on y-axis and set c to ints
plt.scatter(movies.runtime, movies.rating, c=ints)

# Show the plot
plt.show()
```

`@sct`
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki

test_function("numpy.unique",
              not_called_msg = "Don't remove the call of `np.unique` to define `ints`.",
              incorrect_msg = "Don't change the call of `np.unique` to define `ints`.")

test_object("ints",
            undefined_msg = "Don't remove the definition of the predefined `ints` object.",
            incorrect_msg = "Don't change the definition of the predefined `ints` object.")

test_import("matplotlib.pyplot", same_as = True)

test_function("matplotlib.pyplot.scatter",
              incorrect_msg = "You didn't use `plt.scatter()` correctly, have another look at the instructions.")

test_function("matplotlib.pyplot.show")

success_msg("Great work!")
```
