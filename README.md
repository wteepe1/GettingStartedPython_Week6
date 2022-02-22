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

## Additional Python Resources

- [Python](https://www.python.org)
- [Software Carpentry - Intro. to Python](http://swcarpentry.github.io/python-novice-inflammation/)
