# Getting Started with Python

## Basic Python Data Types

- Numbers
    - Note that, unlike bash, Python can handle _both_ integers and floating point (decimal) numbers.
    - Integers - `myInt = 10`
    - Floating point numbers (decimals) - `myFloat = 3.21312`
    - If running Python interactively, variable values can be seen just by typing the name of the variable - `myFloat`.
    - If running Python in a script, variable values can be printed by using the `print()` funtion - `print(myFloat)`.
    - Define myInt and myFloat as above. Now calculate `myInt / myFloat`. What type of number is the result?
    - Now try `float(myInt)` and `int(myFloat)`. What are the results? Look back at the values of `myInt` and `myFloat`. Have they changed?
    -   float(") converts interger to float. int(") converts float to interger
    - Changing numbers from one type to another is one form of "type casting".

- Strings - `myStr = "This is a string."`
    - Strings can be of any length, but are always defined with quotes.
    - Individual characters, or subsets of characters, can be accessed using square brackets - []
      - String indices (and all indices in Python) start at 0
      - `myStr = "biology"`
      - `myStr[0]`
      - A range of indices can be defined with a colon
      - `myStr[2:5]`
    - Strings can be concatenated together with the `+` operator.
      - `myStr = "biology"`
      - `newString = myStr + "_is_super_interesting"`
      - `newString`

- Booleans - `True` or `False`
    - These variables can take the values `True` or `False` only.
      - `myBool = True`
    - These are the data types used in things like `if...else` statements and `while` loops.
    - Logical statements, like `myNum > 3` or `myStr == "test"`, return a boolean variable indicating the result of the comparison
    - In Python, the value of a Boolean can be reversed by preceding it with `not`.

## Functions

- Functions are the verbs of a programming language
- Functions take some variables or objects as input (arguments) and either do something with them or return a new variable/object.
- Functions are always written like this - `myFunction(object1,object2,...)`
- They _always_ have parentheses, even if they don't need any arguments to be passed to them
    - For example, `myFunction()`
- The number and type of arguments needed is specific to each function
- Perhaps the simplest function to use is `print()`. `print()` can take an arbitrary number of variables as arguments and will print them to the screen.
- Here are a few other really useful functions and what they do:
    - `len(string)` - Takes one argument (a string) and returns its length
    - `abs(number)` - Takes one argument (either an integer or a float) and returns its absolute value
    - `round(float)` - Takes one floating point number as an argument and rounds it to the nearest integer
    - `type(variable)` - Takes one variable as an argument and returns its type


## Methods
  
- Methods are functions (sort of like actions or verbs) that belong to a variable
- Methods are accessed and used by appending them to the name of a variable, separated by a `.`
- For instance, let's say we define a string - `myStr = "biOLogy  "`. Here are some really useful methods that can be used with that string:
    - `myStr.upper()` - Converts all characters in the string to uppercase
    - `myStr.lower()` - Converts all characters in the string to lowercase
    - `myStr.strip()` - Removes whitespace from the beginning or ending of the string
    - Methods can also be chained! - `myStr.strip().lower()`
    - `myStr.replace("y","ical")` - This method functions like find and replace, where the first argument is the text to find and the second argument is the text to use when replacing.
    - `myStr.split("O")` - Breaks up the string, using the character provided as an argument as the delimiter. This method then returns a list of new strings. We'll talk more about lists later.

## Comments in Python

- Just like with bash, comments are essential in Python.
- Comments are included in Python by putting a `#` at the beginning of a line.
- Many text editors have a shortcut keystroke to toggle lines between being commented and uncommented. 
- `# This is an example of a comment`

## String Formatting
  
- Python has a special way to format strings so that the values of variables can be included
- The operator `%` is used to indicate that the values of certain variables should be used to fill in a string
- The parts of the string where the values should go is indicated with placeholders (kinda like wildcards)
- The three most basic placeholders are:
    - `%d` - An integer
    - `%f` - A floating point number (i.e., a decimal)
    - `%s` - A string
- Try this:
    - `faveInt = 7`
    - `faveFloat = 3.14`
    - `faveString = phyleaux`
    - `print("Favorite integer is %d, favorite float is %f, and favorite string is %s." % (faveInt,faveFloat,faveString))`
- Note how the variables holding the values are provided in the same order inside parentheses after the `%`.

## User Input

- Python has a special function, `input("Message:" )`, to accept input from a user.
- This function reads the user input and returns it. But be sure to store it in a variable!
    - `userStr = input("Input some string: ")`
- You can use the string methods outlined above to standardize user input - like stripping out excess whitespace, changing character case, etc.

## Getting help from Python
  
- If you need help remembering what methods are available for a given object, use `dir(<OBJECT>)`
- Note that methods starting and ending with "__" are not meant for users to call. They are methods to be used by the system.
- Try creating a string variable (e.g., `myStr = "some text"`).
    - Now run `dir(myStr)`
    - Pick a method you haven't used before and see what it does with `myStr`.

## Practice Exercise 1

```
Write a Python script that does the following:

(1) Creates two variables to store decimal (floating point) numbers

(2) Assigns values to these variables

(3) Performs some mathematical operation with these variables (e.g., addition, subtraction, multiplication, or division)

(4) Creates a string that describes the mathematical operation (e.g., "This script multiplied 8.0 times 2.0 and got 16.0").

(5) Prints the string describing the operation to the screen
```

## `if` statements

- These are similar in form to bash, but simpler.
- The general form is:

```
if <CONDITION>:
    <DO_THIS>
```
   
- The `if` statement has to finish with a `:`.
- Also, in Python, the code block _inside_ the `if` statement must be indented. You can use either tabs or a certain number of spaces. When using spaces, you must use the __same__ number of spaces throughout your code. The official recommendations for Python style strongly suggest using 4 spaces, rather than tabs.
- Note that the syntax for conditions is pretty intuitive in Python
    - `myStr != "other text"`
- `if` statements can be used on their own, but no code will be executed when the condition is false.


## `if...else` statements

- To include code blocks that should be executed when the condition is false, you'll need to use an if...else statement. These have the general form:

```
if <CONDITION>:
    <DO_THING_WHEN_TRUE>
else:
    <DO_THING_WHEN_FALSE>
```
            
- Sometimes, you'll want to test a series of conditions to decide what to do. In that case you could use a nested set of `if...else` statements:

```
nuc = "A"
if nuc == "A":
    print("Nucleotide is an A.")
else:
    if nuc == "C":
        print("Nucleotide is a C.")
    else:
        if nuc == "G":
            print("Nucleotide is a G.")
        else:
            if nuc == "T":
                print("Nucleotide is a T.")
```
                        
- However, you'll notice that this can get pretty cumbersome pretty quickly. Thankfully, python offers another, more compact, way to write this:

```
nuc = "A"
if nuc == "A":
    print("Nucleotide is an A.")
elif nuc == "C":
    print("Nucleotide is a C.")
elif nuc == "G":
    print("Nucleotide is a G.")
elif nuc == "T"
    print("Nucleotide is a T.")
```
            
- The `elif` statements stand for `else...if` and capture what we tried to do above with the nesting.
- It is important to realize that as we've currently written these statements, nothing would happen if the variable `nuc` didn't have the value `A`, `C`, `G`, or `T`. This can be a big problem when accepting input from a user or file that might provide a nonsensical value. To capture these cases, it's always best to close with a simple `else`:

```
nuc = "A"
if nuc == "A":
    print("Nucleotide is an A.")
elif nuc == "C":
    print("Nucleotide is a C.")
elif nuc == "G":
    print("Nucleotide is a G.")
elif nuc == "T":
    print("Nucleotide is a T.")
else:
    print("This is not a valid nucleotide!")
```

## Practice Exercise 2

```
One recipe for jambalaya calls for the following ingredients:

- sausage
- chicken
- celery
- onion
- broth
- rice
- seasoning

Write a script that asks a user to enter five items they plan to purchase from the grocery store. For each item, the 
script should tell the user if that item is part of the jambalaya recipe. Also, if they enter a jamabalaya ingredient 
more than once, the script should tell them that they've already purchased that ingredient.
```

## Lists

- We've now covered the simple variable types in Python: integers, floats, strings, and bools.
- However, there are several more complex types of variables that allow us to store and access multiple values.
- Perhaps the most versatile and common of these more complex types are lists.
- Lists are always specified using square brackets - `[]`
- Lists can contain an arbitrary number and type of simpler variables, but we often want to use only one type in a list so as not to get confused.
    - `listOfNums = [1,2,3,4]`
    - `listOfFloats = [3.14, 2.0, 12.3]`
    - `listOfStrings = ["Ecology", "Evolution", "Systematics"]`
    - `listOfBools = [True, False, False, True]`
- Even after they are created, lists can be modified. Individual elements can be added using the append method():
    - `listOfNums.append(5)` - Examine list after executing
    - `listOfStrings.append("Neurobiology")`
- Elements can be removed using a few different methods.
    - Try `listOfFloats.pop()` - What is returned? And what does the list look like now?
    - You can remove specific values from a list, regardless of their position, by using the `remove(<VALUE>)` method. What happens when you execute `listOfBools.remove(False)`? How does the list change?
- Lists can contain lists as elements. For instance, try this:
    - `newList = []`
    - `newList.append([1,2,3])`
    - `newList.append([4,5,6])`
    - `newList.append([12,13,14])`
- But you can also add all the _individual elements_ of one list to another. Try this:
    - `newList = [1,2,3]`
    - `newList.extend([4,5,6])`
    - `newList.extend([12,13,14])`
    - How does `newList` differ from what you got when you used `append()`?
- You can view or extract parts of a list by using indices and "slicing" the list (just remember that python starts counting at 0!)
    - `newList[4:7]` - What values are returned? How do these relate to the indices you provided?
- You can also extract every n-th element of a list using notation like this:
    - `newList[::2]` - What values are returned now?
    - `newList[2:8:2]` - How about now?
- You can also alter individual elements of lists by using indices
    - `newList`
    - `newList[2] = 100`
    - `newList`

## `for` loops
  
- One of the nicest things about Python is the relationship between lists and `for` loops
- If you have an existing list, you can quickly iterate across all of its elements using this syntax:

```
for num in newList:
    print("This number is: %d" % num)
```
            
- If you still want to iterate over a series of integers, you can use the range() function.

```
for num in range(10):
    print("This number is: %d" % num)
```

## A note about "copying objects"

- Try this:
    - `firstNum = 2`
    - `secondNum = firstNum`
    - `firstNum = 5`
    - `firstNum`
    - `secondNum`
- Now try this:
    - `firstList = [1,2,3]`
    - `secondList = firstList`
    - `firstList.extend([4,5,6])`
    - `firstList`
    - `secondList`

## Tuples

- Tuples are like lists, but they're not mutable (can't be changed)
- Tuples are instantiated using parentheses - `()`
- Try this:
    - `myTuple = (1,2,3)`
    - `myTuple`
    - `myTuple[1]`
    - `myTuple[1] = 5`

## While loops

- Sometimes we want to do something repetitively, but we don't know ahead of time how many times we need to repeat it (as in a `for` loop.
- In these cases, we can use a `while` loop. A `while` loop will continue to do something until a certain condition is no longer satisfied.

```
num = 0
while num < 10:
    print(num)
    num += 1
```

- WARNING - You need to make sure to update variables such that the condition will eventually be satisified. If you don't, you could create an infinite loop!

## Dictionaries

- Dictionaries are incredibly useful for storing pairs of things - known as "keys" and "values"
- They don't store these pairs in a particular order, like lists do, but they make looking up values from keys much faster.
- The keys and values can each be different types of variables
- To create a new dictionary, you can use this syntax:
    - `myDict = {"keyOne":"valueOne", "keyTwo":"valueTwo"}`
- To look at the methods available for dictionaries, try this:
    - `dir(myDict)`
- You can access a value, as long as you know its key, either of these ways:
    - `myDict.get("keyOne")`
    - `myDict["keyOne"]`
- You can change a value using its key, this way:
    - `myDict["keyOne"] = <NEW_VALUE>`
- You can add a new key/value pair using the update method:
    - `myDict.update({<NEW_KEY:NEW_VALUE})`

## Additional Python Resources

- [Python](https://www.python.org)
- [Software Carpentry - Intro. to Python](http://swcarpentry.github.io/python-novice-inflammation/)
