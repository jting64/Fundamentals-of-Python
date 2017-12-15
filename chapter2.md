---
title       : Chapter 2-Standard Data Types
description : Insert the chapter description here
---
## Introducing Standard Data Types

```yaml
type: MultipleChoiceExercise
lang: python
xp: 50
skills: 1
key: c4dee315d7
```

Which one of these is not one of the five standard data types in Python?

`@instructions`
- Number
- While Loop
- String
- Tuple
- List
- Dictionary

`@hint`
Which does not represent or store a specific value or variable?

`@pre_exercise_code`
```{python}
# The pre exercise code runs code to initialize the user's workspace.
# You can use it to load packages, initialize datasets and draw a plot in the viewer

```

`@sct`
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki

msg_bad = "That is not correct!"
msg_success = "Exactly! A while loop is not a standard data type."
test_mc(2, [msg_bad, msg_success, msg_bad, msg_bad, msg_bad, msg_bad])
```

---
## Introducing Strings!

```yaml
type: NormalExercise
lang: python
xp: 100
skills: 1
key: b0a5dd001a
```

So... what do you think a string is?

A string is a contingous set of characters represented in quotation marks. For example, this would be a string: `"Hello, I am a string."`.

`@instructions`
- Declare a string called `string1` and set its value to `"I am the first string"`
- Print `string1`
- Declare a second string called `string2` and set its value to `"I am the second string"`
- Print `string2`

`@hint`
- You don't have to program anything for `string1`. It has already been declared, initialized, and printed.
- Use the sample code provided for `string1` to declare, initialized, and print `string2`

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
# Declare and initialize string1
string1 = "I am the first string"
# Print string1
print (string1)

# Declare and initialize string2
string2 = ___
# Print string2
print (___)
```

`@solution`
```{python}
# Declare and initialize string1
string1 = "I am the first string"
# Print string1
print (string1)

# Declare and initialize string2
string2 = "I am the second string"
# Print string2
print (string2)
```

`@sct`
```{python}
# SCT written with pythonwhat: https://github.com/datacamp/pythonwhat/wiki
test_object("string1", eq_condition="equal", do_eval=True, undefined_msg="Your string1 has not been defined", incorrect_msg="Your string1 is not initialized properly")
test_object("string2", eq_condition="equal", do_eval=True, undefined_msg="Your string2 has not been defined", incorrect_msg="Your string2 is not initialized properly")
test_output_contains("I am the first string", pattern=False, no_output_msg= "You have not printed string1 correctly")
test_output_contains("I am the second string", pattern=False, no_output_msg= "You have not printed string2 correctly")

success_msg("Great work!")
```

---
## String Operations

```yaml
type: NormalExercise
key: 4e96055c96
lang: python
xp: 100
skills: 2
```
As we have learned in the previous lesson, in order to print a complete string, you must call "print (string_name)" 
But other than printing the entire string, are there some ways you could print a subset of a string?
`@instructions`
- There are various ways to print a subset of strings
- For example, you can specify which character to print by indicating its index within the whole string or indicating a range of indexes.
- Look at the sample code for the various ways to print a string.
- Now, work on string2 (which has already been defined for you) to print various ranges of the string.

`@hint`
- The index of the first character in a string is ZERO, not one!
`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
string1 = "My favorite fruit is "
print (string1)          # Prints complete string
print (string1[0])       # Prints first character of the string
print (string1[1:5])     # Prints characters from 2nd to 5th (inclusive)
print (string1[7:])      # Prints string starting from 8th character (inclusive)
print (string1 * 5)      # Prints string 5 times
print (string1 + "apples!") # Prints concatenated string

string2 = "This is an exercise to print strings."
print ("1."+ ___) # 1. Print the complete string
print ("2."+ ___) # 2. Print the 5th character
print ("3."+ ___) # 3. Print characters starting from the 5th to 7th (inclusive)
print ("4."+ ___) # 4. Print all characters starting from the 9th character (inclusive)
print ("5."+ ___) # 5. Print the string 7 times
print ("6."+ ___) # 6. Print a concatentated string by adding "YAY!"
```

`@solution`
```{python}
string1 = "My favorite fruit is "
print (string1)          # Prints complete string
print (string1[0])       # Prints first character of the string
print (string1[1:5])     # Prints characters from 2nd to 5th (inclusive)
print (string1[7:])      # Prints string starting from 8th character (inclusive)
print (string1 * 5)      # Prints string 5 times
print (string1 + "apples!") # Prints concatenated string

string2 = "This is an exercise to print strings."
print ("1."+ string2)          # 1. Print the complete string
print ("2."+ string2[4])       # 2. Print the 5th character
print ("3."+ string2[4:7])     # 3. Print characters from the 5th to 7th (inclusive)
print ("4."+ string2[8:])      # 4. Print all characters starting from the 9th character (inclusive)
print ("5."+ string2 * 7)      # 5. Print the string 7 times
print ("6."+ string2 + "YAY!") # 6. Print a concatentated string by adding "YAY!"
```

`@sct`
```{python}
test_output_contains("1.This is an exercise to print strings.", pattern=False, no_output_msg= "You have not printed the first instruction correctly")
test_output_contains("2. ", pattern=False, no_output_msg= "You have not printed the second instruction correctly")
test_output_contains("3. is", pattern=False, no_output_msg= "You have not printed the third instruction correctly")
test_output_contains("4.an exercise to print strings.", pattern=False, no_output_msg= "You have not printed the fourth instruction correctly")
test_output_contains("5.This is an exercise to print strings.This is an exercise to print strings.This is an exercise to print strings.This is an exercise to print strings.This is an exercise to print strings.This is an exercise to print strings.This is an exercise to print strings.", pattern=False, no_output_msg= "You have not printed the fifth instruction correctly")
test_output_contains("6.This is an exercise to print strings.YAY!", pattern=False, no_output_msg= "You have not printed the sixth instruction correctly")

success_msg("Great work!")
```

---
## Introducing Lists!

```yaml
type: NormalExercise
key: 8cb08ba668
lang: python
xp: 100
skills: 2
```
What is a list?
- A list in python holds a sequence of elements. Each element will have its own index (or position).
- It is also important to remember that the first index is 0. For example, in a list of [1992, "Hello", "World", -102], the first element (1992) will have an index of 0.
- Also, the elements in a list do not need to be the same type.

`@instructions`
- Elements in a list can be accessed, updated, or deleted. Look at the provided sample code to learn how to perform these operations.
- Then, follow the instructions below to complete this exercise!
    - Declare a list called `list2`
    - Initialize the list to ["Physics", "Python", "Writing", "Calculus"]
    - Print out the entire list
    - Print out the 3rd element
    - Update the 3rd element to "Chemistry"
    - Print out the 3rd element again
    - Delete the 1st element
    - Print out the entire list again
    - Print out the 2nd to 3rd elements
`@hint`

`@pre_exercise_code`
```{python}
```

`@sample_code`
```{python}
# Declares and initalizes a list
list1 = [0,1,2,3,4,5,6,"Seven", "Eight", "Nine", "Ten"]
# In order to access an element within the list, you will call list_name[index_of_element]
firstElement = list1[0]
print ("1.", firstElement) # It will print "0"
# Accesses the 4th element to the 5th element
subsetElement = list1[3:5]
print ("2.", subsetElement) # It will print "[3, 4]"
print ("Original value at index 7: ")
print ("3.", list1[7]) # It will print 
# Updates list1[7] which originally was "Seven" to 7
list1[7] = 7
print ("Updated value at index 7: ")
print ("4.", list1[7]) # It will print 
print ("5.", list1) # Prints the entire list
# Deletes the first element (with index 0)
del list1[0]
# Notice, that 0 has been deleted so all elements after it has been shifted forward one index
print ("6.", list1)
# Slicing also works for lists! This will print all the elements starting from index 3 (aka the 4th element) to index 7 (aka 8th element)
print ("7.", list1[3:8])

# Now it is your turn to practice list operations
list2 = [___ , ___ , ___ , ___]
print ("1.", ___)
print ("2.", list2[___])
list2[___] = ___
print ("3.", list2[___])
del list2[___]
print ("4.", ___)
print ("5.", ___)
```

`@solution`
```{python}
# Declares and initalizes a list
list1 = [0,1,2,3,4,5,6,"Seven", "Eight", "Nine", "Ten"]
# In order to access an element within the list, you will call list_name[index_of_element]
firstElement = list1[0]
print ("1.", firstElement) # It will print "0"
# Accesses the 4th element to the 5th element
subsetElement = list1[3:5]
print ("2.", subsetElement) # It will print "[3, 4]"
print ("Original value at index 7: ")
print ("3.", list1[7]) # It will print 
# Updates list1[7] which originally was "Seven" to 7
list1[7] = 7
print ("Updated value at index 7: ")
print ("4.", list1[7]) # It will print 
print ("5.", list1) # Prints the entire list
# Deletes the first element (with index 0)
del list1[0]
# Notice, that 0 has been deleted so all elements after it has been shifted forward one index
print ("6.", list1)
# Slicing also works for lists! This will print all the elements starting from index 3 (aka the 4th element) to index 7 (aka 8th element)
print ("7.", list1[3:8])

# Now it is your turn to practice list operations
list2 = ["Physics", "Python", "Writing", "Calculus"]
print ("1.", list2)
print ("2.",list2[2])
list2[2] = "Chemistry"
print ("3.",list2[2])
del list2[0]
print ("4.", list2)
print ("5.", list2[1:3])
```

`@sct`
```{python}
test_output_contains("1.['Physics', 'Python', 'Writing', 'Calculus']", no_output_msg= "You have not printed list2 correctly")
test_output_contains("2. Writing",no_output_msg= "You have not printed the 3rd element correctly")
test_output_contains("3. Chemistry",no_output_msg= "You have not printed the updated 3rd element correctly")
test_output_contains("4.['Python', 'Chemistry', 'Calculus']", no_output_msg= "You have not printed the updated list2 correctly")
test_output_contains("5.['Chemistry', 'Calculus']", no_output_msg= "You have not printed sliced list2 correctly")

success_msg("Great work!")
```

---
## Basic List Operations

```yaml
type: NormalExercise
key: c04253f812
lang: python
xp: 100
skills: 2
```
Other than simply deleting or updating elements in a list, there are also other list operations.
1. Concatenation
2. Repetition
3. Membership

`@instructions`
Following the sample code provided, work on the exercise below:
- Initialize `list1` to ["I ", "am ", "a ", "list ", "of ", "strings."]
- Initialize `list2` to ["a", "b", "c", "d"]
- Concatenate list1 and list2 to list3
- Print list3
- Check if "b" is inside of list1
- Check if "b" is inside of list3
`@hint`

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
practice1 = [1,2,3,4,5]
practice2 = [6,7,8,9,10]
# This concatentates practice1 and practice2 to practice3; practice3 will become [1,2,3,4,5,6,7,8,9,10]
practice3 = practice1 + practice2
print ("1.", practice3)
# This checks whether 3 is in practice2
print ("2.", 3 in practice2)
# This checks whether 3 is in practice3
print ("3.", 3 in practice3)

list1 = [___,___, ___,___, ___,___]
list2 = [___,___,___,___]
list3 = ___ + ___
print ("1.", ___)
print ("2.", ___ in ___)
print ("3.", ___ in ___)
```

`@solution`
```{python}
practice1 = [1,2,3,4,5]
practice2 = [6,7,8,9,10]
# This concatentates practice1 and practice2 to practice3; practice3 will become [1,2,3,4,5,6,7,8,9,10]
practice3 = practice1 + practice2
print ("1.", practice3)
# This checks whether 3 is in practice2
print ("2.", 3 in practice2)
# This checks whether 3 is in practice3
print ("3.", 3 in practice3)

list1 =["I ", "am ", "a ", "list ", "of ", "strings."]
list2 = ["a", "b", "c", "d"]
list3 = list1 + list2
print ("1.", list3)
print ("2.", "b" in list1)
print ("3.", "b" in list3)
```

`@sct`
```{python}
test_output_contains("1. ['I ', 'am ', 'a ', 'list ', 'of ', 'strings.', 'a', 'b', 'c', 'd']", pattern=False, no_output_msg= "You have not printed list3 correctly")
test_output_contains("2. False")
test_output_contains("3. True")
success_msg("Great work!")
```

---
## Built-In List Functions

```yaml
type: NormalExercise
key: 7cf98920aa
lang: python
xp: 100
skills: 2
```

Lists have some built-in functions that can be used. These are a few commonly used functions.
1. len(list1)
2. max(list1)
3. min(list1)
4. list.extend(seq)
5. list.count(obj)
6. list.insert(index, obj)
7. list.sort()

`@instructions`
- Initialize `list1` to [51,203,73,4000,-10]
- Print out the length of `list1`
- Delete the third element
- Print out the length of `list1`
- Print out the maximum in `list1`
- Print out the minimum in `list1`
- Append the following elements to `list1`: [51,51,51,51,-10,203,-10]
- Count how many 51's are in the list
- Insert 3 at the 2nd index
- Print `list1`
- Sort `list1`
- Print `list1`

`@hint`

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
practice1 = [12,400,723,4100,-100]
# Prints the length of `practice1`
print ("1.", len(practice1))
# Prints the maximum of `practice1`
print ("2.", max(practice1))
# Prints the minimum of `practice1`
print ("3.", min(practice1))
# Appends [51,51,51,51,-10,203,-10] to practice1
practice1.extend([12,401,12,723,-10,203,-10])
# Count the number of 723s in practice1
print ("4.", practice1.count(723))
# Inserts 100 at the 2nd index
practice1.insert(2,100)
print ("5.", practice1)
# Sorts list1
practice1.sort()
print ("6.", practice1)

list1 = [___,___,___,___,___]
print ("1.", ___(___))
del list1[___]
print ("2.", ___(___))
print ("3.", ___(___))
print ("4.", ___(___))
list1.___([___,___,___,___,___,___,___])
print ("5.", list1.___(___))
list1.___(___,___)
print ("6.", ___)
list1.___()
print ("7.", ___)
```

`@solution`
```{python}
practice1 = [12,400,723,4100,-100]
# Prints the length of `practice1`
print ("1.", len(practice1))
# Prints the maximum of `practice1`
print ("2.", max(practice1))
# Prints the minimum of `practice1`
print ("3.", min(practice1))
# Appends [51,51,51,51,-10,203,-10] to practice1
practice1.extend([12,401,12,723,-10,203,-10])
# Count the number of 723s in practice1
print ("4.", practice1.count(723))
# Inserts 100 at the 2nd index
practice1.insert(2,100)
print ("5.", practice1)
# Sorts list1
practice1.sort()
print ("6.", practice1)

list1 = [51,203,73,4000,-10]
print ("1.", len(list1))
del list1[2]
print ("2.", len(list1))
print ("3.", max(list1))
print ("4.", min(list1))
list1.extend([51,51,51,51,-10,203,-10])
print("5.", list1.count(51))
list1.insert(2,3)
print ("6.", list1)
list1.sort()
print ("7.", list1)
```

`@sct`
```{python}
test_output_contains("1. 5", pattern=False, no_output_msg= "You have not printed the length of list1 correctly")
test_output_contains("2. 4", pattern=False, no_output_msg= "You have not printed the length of list1 correctly")
test_output_contains("3. 4000", pattern=False, no_output_msg= "You have not printed the maximum of list1 correctly")
test_output_contains("4. -10", pattern=False, no_output_msg= "You have not printed the minimum of list1 correctly")
test_output_contains("5. 5", pattern=False, no_output_msg= "You have not printed the number of occurences for 51 correctly")
test_output_contains("6. [51, 203, 3, 4000, -10, 51, 51, 51, 51, -10, 203, -10]", pattern=False, no_output_msg= "You have not printed list1 correctly")
test_output_contains("7. [-10, -10, -10, 3, 51, 51, 51, 51, 51, 203, 203, 4000]", pattern=False, no_output_msg= "You have not printed list1 correctly")
test_object("list1")

success_msg("Great work!")
```

---
## Introducing Dictionaries!

```yaml
type: NormalExercise
key: 3d80ac58c0
lang: python
xp: 100
skills: 2
```
What is a dictionary in Python?
- A way of looking at a dictionary is a set of `key: value` pairs with the requirement that a key must be unique within that dictionary.
- Like a list, a dictionary also contains a sequence of elements. However, the difference is that it is not indexed by a range of numbers, instead by keys.
- Keys can be any immutable data type such as numbers, strings, tuples containing numbers, strings, or tuples. It is important to remember that if the tuple contains a mutable object, it cannot serve as a key.
- Also, there cannot be more than one entry per key. When duplicate keys are encountered, the last assignment wins.

`@instructions`
Following the sample code provided, work on the exercise below:
- Declare and initialize a dictionary called `dict1` as {'Physics': 'A+', 'Biology': 'B+', 'Chemistry': 'A-', 'Python': 'A'}
- This dictionary uses various classes as keys and the grade within that class as the value
- Print out the value for the key "Biology"
- Update the grade for "Chemistry" to B-
- Add a new class called "Calculus" and set its value to "D+"
- Delete the entry with a key of "Python"

`@hint`

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
# Declares and initializes a dictionry with the values {'iPhone5': 7000, 'iPhone4': 5000,'iPhone6':100000,'iPhone7': 200000, 'iPhone8': 400000, 'iPhoneX': 1050000}
# The keys are the various iPhones, while the value represents their individual price. 
practice1 = {'iPhone5': 7000, 'iPhone4': 5000,'iPhone6':100000,'iPhone7': 200000, 'iPhone8': 400000}
# str(dict_name) converts a dictionary to a string representation, then the print function will print the string representation
print ("1.", str(practice1))
# Access and print the value with the key 'iPhone7'
print("2.", practice1['iPhone7'])
# Updates the price of an iPhone4 to 0
practice1['iPhone4'] = 0
# Adds a new entry within the dictionary
practice1['iPhoneX'] = 1050000
# Deletes the entry with the key of 'iPhone5'
del practice1['iPhone5']
print ("3.", str(practice1))

dict1 = {'___': '___', '___': '___', '___': '___', '___': '___'}
print (dict1['___'])
dict1['___'] = '___'
dict1['___'] = '___'
del dict1['___']
```

`@solution`
```{python}
# Declares and initializes a dictionry with the values {'iPhone5': 7000, 'iPhone4': 5000,'iPhone6':100000,'iPhone7': 200000, 'iPhone8': 400000, 'iPhoneX': 1050000}
# The keys are the various iPhones, while the value represents their individual price. 
practice1 = {'iPhone5': 7000, 'iPhone4': 5000,'iPhone6':100000,'iPhone7': 200000, 'iPhone8': 400000}
# str(dict_name) converts a dictionary to a string representation, then the print function will print the string representation
print ("1.", str(practice1))
# Access and print the value with the key 'iPhone7'
print("2.", practice1['iPhone7'])
# Updates the price of an iPhone4 to 0
practice1['iPhone4'] = 0
# Adds a new entry within the dictionary
practice1['iPhoneX'] = 1050000
# Deletes the entry with the key of 'iPhone5'
del practice1['iPhone5']
print ("3.", str(practice1))

dict1 = {'Physics': 'A+', 'Biology': 'B+', 'Chemistry': 'A-', 'Python': 'A'}
print (dict1['Biology'])
dict1['Chemistry'] = 'B-'
dict1['Calculus'] = 'D+'
del dict1['Python']
```

`@sct`
```{python}
test_output_contains("B+", pattern=False, no_output_msg= "You have not printed the value for the key 'Biology' correctly")
test_dictionary('dict1')
success_msg("Great work!")

```

---
## Built-In Dictionary Functions

```yaml
type: NormalExercise
key: d0c377494d
lang: python
xp: 100
skills: 2
```
There are various built-in functions that can be used with dictionaries. The following are a few examples of the most common functions:
1. len(dict)
2. str(dict)
3. dict.keys()
4. dict.values()
5. dict.items()

`@instructions`
Utilize the introduced built-in functions for the following exercise
- Declare and initialize a dictionary called `dict1` as {'Physics': 'A+', 'Biology': 'B+', 'Chemistry': 'A-', 'Python': 'A'}
- Print the length of `dict1`
- Print a list of all the keys in `dict1`
- Print a list of all the values in `dict1`
- Print a list of tuples for all the elements in `dict1`

`@hint`

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
practice1 = {'iPhone5': 7000, 'iPhone4': 5000,'iPhone6':100000,'iPhone7': 200000, 'iPhone8': 400000}
# Prints the length of practice1
print (len(practice1))
# Prints all the keys of practice1
print ("Keys:")
print (practice1.keys())
# Prints all the values of practice1
print ("Values:")
print (practice1.values())
# Prints all the elements of practice1 in a tuple
print ("Elements:")
print (practice1.items())

dict1 = {'___': '___', '___': '___', '___': '___', '___': '___'}
print ("1.", ___(___))
print ("2.", ___.___())
print ("3.", ___.___())
print ("4.", ___.___())
```

`@solution`
```{python}
practice1 = {'iPhone5': 7000, 'iPhone4': 5000,'iPhone6':100000,'iPhone7': 200000, 'iPhone8': 400000}
# Prints the length of practice1
print (len(practice1))
# Prints all the keys of practice1
print ("Keys:")
print (practice1.keys())
# Prints all the values of practice1
print ("Values:")
print (practice1.values())
# Prints all the elements of practice1 in a tuple
print ("Elements:")
print (practice1.items())

dict1 = {'Physics': 'A+', 'Biology': 'B+', 'Chemistry': 'A-', 'Python': 'A'}
print ("1.", len(dict1))
print ("2.", dict1.keys())
print ("3.", dict1.values())
print ("4.", dict1.items())
```

`@sct`
```{python}
test_output_contains("1. 4", pattern=False, no_output_msg= "You have not printed the length for the dictionary correctly")
test_output_contains("2. dict_keys([", pattern=False, no_output_msg= "You have not printed the keys for dict1 correctly")
test_output_contains("3. dict_values([", pattern=False, no_output_msg= "You have not printed the values for dict1 correctly")
test_output_contains("4. dict_items([", pattern=False, no_output_msg= "You have not printed the items for dict1 correctly")

test_dictionary('dict1')
success_msg("Great work!")

```


---
## Lets Practice Using Strings & Lists & Dictionaries!

```yaml
type: NormalExercise
key: 3f818a9030
lang: python
xp: 100
skills: 2
```
After learning how to use strings, lists, and dictionaries in this chapter, lets have an exercise to review all the information you have learned.

`@instructions`
- Initialize a string called `string1` and set it to "Python"
- Initialize a string called `string2` and set it to " and Game Programming"
- Initialize a string called `string3` and set it to the concatenation of `string1` and `string2`
- Print out `string3` five times
- Print out the first character of `string3`
- Print out the 3rd to 8th characters of `string3`
- Initialize a list called `list1` and set it to ['Python','Ethics','Economics','PE','Robotics']
- Initialize a list called `list2` and set it to [88,93,70,93,100]
- Print out the maximum in `list2`
- Print out the minimum in `list2`
- Print out the number of 93s in `list2`
- Extend `list1` to include `list2`
- Delete the first element in  `list2`
- Sort `list2`
- Print `list1`
- Print `list2`
- Initialize a dictionary called `dict1` and set it to {'Assignment1': 88, 'Assignment2': 93, 'Assignment3': 70, 'Assignment4': 93, 'Assignment5': 100}
- Print out the length of `dict1`
- Add a new entry inside `dict1` with the key 'Assignment6' and the value of 90
- Print out the length of `dict1`
- Delete the entry with the key 'Assignment3'
- Print out a string form of `dict1`
`@hint`

`@pre_exercise_code`
```{python}

```

`@sample_code`
```{python}
string1 = "___"
string2 = "___"
string3 = ___ + ___
print ("1.", ___ * ___)
print ("2.", string3[___])
print ("3.", string3[___ : ___])
list1 = [___,___,___,___,___]
list2 = [___,___,___,___,___]
print ("4.", ___(list2))
print ("5.", ___(list2))
print ("6.", list2.___(93))
list1.___(list2)
del list2[___]
list2.___()
print ("7.", list1)
print ("8.", list2)
dict1 = {___: ___, ___: ___, ___: ___,___: ___,___: ___}
print ("9.", ___(dict1))
dict1[___] = ___
print ("10.", ___(dict1))
del dict1[___]
print ("11.", ___(dict1))
```

`@solution`
```{python}
string1 = "Python"
string2 = " and Game Programming"
string3 = string1 + string2
print ("1.", string3 * 5)
print ("2.", string3[0])
print ("3.", string3[2:8])
list1 = ['Python','Ethics','Economics','PE','Robotics']
list2 = [88,93,70,93,100]
print ("4.", max(list2))
print ("5.", min(list2))
print ("6.", list2.count(93))
list1.extend(list2)
del list2[0]
list2.sort()
print ("7.", list1)
print ("8.", list2)
dict1 = {'Assignment1': 88, 'Assignment2': 93, 'Assignment3': 70, 'Assignment4': 93, 'Assignment5': 100}
print ("9.", len(dict1))
dict1['Assignment6'] = 90
print ("10.", len(dict1))
del dict1['Assignment3']
print ("11.", str(dict1))
```

`@sct`
```{python}
test_output_contains("1. Python and Game ProgrammingPython and Game ProgrammingPython and Game ProgrammingPython and Game ProgrammingPython and Game Programming", pattern=False, no_output_msg= "You have not printed string3 five times correctly")
test_output_contains("2. P", pattern=False, no_output_msg= "You have not printed the first character of string3 correctly")
test_output_contains("3. thon a", pattern=False, no_output_msg= "You have not printed 3rd to 8th characters of string3 correctly")
test_output_contains("4. 100", pattern=False, no_output_msg= "You have not printed the maximum for list2 correctly")
test_output_contains("5. 70", pattern=False, no_output_msg= "You have not printed the minimum for list2 correctly")
test_output_contains("6. 2", pattern=False, no_output_msg= "You have not printed the number of times 93 appears in list2 correctly")
test_output_contains("7. ['Python', 'Ethics', 'Economics', 'PE', 'Robotics', 88, 93, 70, 93, 100]", pattern=False, no_output_msg= "You have not printed list1 correctly")
test_output_contains("8. [70, 93, 93, 100]", pattern=False, no_output_msg= "You have not printed list2 correctly")
test_output_contains("9. 5", pattern=False, no_output_msg= "You have not printed the length of dict1 correctly")
test_output_contains("10. 6", pattern=False, no_output_msg= "You have not printed the updated length of dict1 correctly")
test_dictionary('dict1')
test_object("list1")
test_object("list2")
test_object("string1")
test_object("string2")
test_object("string3")
test_student_typed("str(dict1)", pattern = False)
success_msg("Great work!")
```