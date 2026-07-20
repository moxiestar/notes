## **Useful resources**

***Python exercises:***
- https://genepy.org/exercises/
- https://www.practicepython.org/
- https://roadmap.sh/python

***References:***
- https://comp110-25ss1.github.io/topics/
- https://quickref.me/python

***Memory diagram practice:***
- https://comp110-25ss1.github.io/topics/pages/environments.html#environment-diagram-practice
- https://20f.comp110.com/students/resources/practice/env-practice.html
- https://20f.comp110.com/students/resources/quiz2-practice.html
- https://comp110-24s.github.io/resources/practice/MemDiagrams.html


-------------------------------------------------------------------

## **May 14: Lesson 1**

***Key takeaways:***
- **REPL (read execute print loop):**
	- Interaction with computer
	- Initialized by typing python in terminal
- **Running a module from terminal:** python -m my_file_name
- **Assignments can be resubmitted with no penalty**
- Quizzes are on paper (for some reason)

***First exercise:*** 
- https://comp110-25ss1.github.io/exercises/ex00_hello_world.html
- Defining functions: 
	  **def greet(name: str) -> str:**
		**"""A welcoming first function definition."""**
		**return "Hello, " + name + "!"**
	- Function name: **greet**
		- Function definitions begin with the keyword **def**
		- Here, **greet** is an **identifier** 
	- Parameters: **name: str**
		- Parameters are inputs given to a function when it is called
	- Return type: **str**
	- Documentation string: **"""A welcoming first function definition."""**
		- Doc strings define functions and denote their purpose
	- Return expression: **"Hello, " + name + "!"**
		- This expression is a string concatenation
- Function call expression: **greet(name="Student")**
	- Like any other expression, the function call evaluates to a value of a specific type
	- Function call expressions begin with identifiers (name of the function)
	- Arguments are contained within parentheses 
	- This argument is a keyword argument, which specifies the name of the parameter we are providing an input value for
- Final code: 
	  if __name__ == "__main__": 
		  print(greet(name=input("What is your name?")))

-------------------------------------------------------------------

## **May 15: Lesson 2**

***Comments vs. doc strings:***
- **Comments:** 
	- Lines that start with #
	- Used to explain the purpose of your code
- **Doc strings**
	- Strings are denoted by “““ ”””
	- String at the top of every file to describe purpose

***Objects:***
- *Typed units of data* stored in computer memory
- The *object’s type* classifies it, helping the computer interpret it
- **Types of literal data:**
	- Numerical: 
		- Integers (int)
		- Floating-point decimals (float)
	- Logical:
		- Boolean (bool)
			- Evaluates to True or False (case-sensitive)
	- Textual:
		- Strings (str)
			- Sequence of character(s)
			- Denoted by “ ”
- **Indexing:**
	- Subscription syntax uses square brackets [] to access an item in a sequence
	- Index numbering starts from 0
- **Checking an object’s type:**
	- type() ← data goes in parentheses
- **Changing (“casting”) an object’s type:**
	- float()/str()/int() ← data goes in parentheses
- **Evaluating length:**
	- len() evaluates the length of a string

***Expressions:***
- Fundamental building block in programs
- Two main ideas behind expressions:
	- Expressions evaluate to a typed value
	- An object’s type tells you how to use it
	- An expression is an intent to do something
- Expressions can be mathematical, just single integers, or strings
- PEMDAS applies
- **Numerical operations:**
	- Addition:
		- float + float = float
		- int + int = int
		- float + int = float
		- string + string = stringstring (concatenation)
	- Subtraction is exclusive to numerical types
	- Multiplication:
		- string x int → string is repeated int number of times
		- string x float does not work
		- The type of the output depends on the operands
	- Division:
		- Exclusive to numerical types
		- Always results in float
	- Remainders (modulo):
		- Exclusive to numerical types
		- Output type depends on the operands
		- If x is even, “x % 2” → 0
	- Exponentiation
		- Exclusive to numerical types
		- Output type depends on the operands
	- Numerical operators in python:![[Screenshot 2025-05-15 at 10.41.37 AM.png]]
- **Relational operators:**
	- Operations always result in bool (True or False)
	- Equals (= =, no space) vs not equal (!=)
	- Greater than (>), at least (>=), less than (<), at most (<=)
	- **Always start with the innermost parentheses on the right side of an expression**
	- Relational operators in python:![[Screenshot 2025-05-15 at 11.07.42 AM.png]]

-------------------------------------------------------------------

## **May 16: Lesson 3**

***Functions:***
- Shorthand: **fn**
- Functions execute chunks of code with certain inputs
- Similar to recipes - must be called (cf cooking) to produce something
- **Fundamental pattern:**
	- Begins with input
	- Contains the steps to a program
	- Produces an output
- Parameterized function definition allows you to substitute different input arguments and get intentionally different results 
- **Structure of functions:**
	- Function signature:
		1. Begins with “def” 
		2. The function is named (textually)
		3. (parameter: type) is a parameter list
			- Inputs are within parentheses 
			- You can have one or multiple parameters
			- Parameters are **only** present in **function definitions**
		4. → return type: specifies the output (type = bool, int, etc)
	- Function body:
		-  Must be indented
		1. Doc string explains the purpose of the function
		2. Return statement includes an expression to produce the output
	- Function call:
		1. Function name
		2. (argument=value) is an argument list that includes the input values for the parameters
		3. **Not all return statements are function calls**

***Memory diagrams:***
- Evaluation of a program depends on many interrelated values
- Things to keep track of:
	- Current line of code (frame of execution)
	- Sequence of function calls that lead to the current line
	- Names of parameters and variables, as well as the values they are bound to
- Memory diagrams provide a record of the environment and its state
	- Runtime environment: names in your program mapped to their locations in memory
	- State: values stored in those locations
- Three parts:
	- Output: printed returns
	- Stack: list of function calls
		- Globals: information that is globally accessible within the program 
		- RA: return address, line of code where function was called
		- RV: return value, value that the function call produced
	- Heap: computer memory 

***Other notes:***
- = ties a value to a variable
- return provides the result for the computer
- print shows you the results


-------------------------------------------------------------------

## **May 20: Lesson 4**

***Boolean Operators***
- The **or** operator
	- If at least one side is true, the result will be true
		- False or False = False
		- True or False = True
		- False or True = True
		- True or True = True
- The **and** operator
	- False and False = False
	- True and False = False
	- False and True = False
	- True and True = True
- The **not** operator
	- not False = True
	- not True = False
- **+** > **>** > **not** > **and** > **or**

***Conditional Control Flow:***
- Control flow is linear
- If-then-else statements:
	- If-statements must evaluate to a boolean value
	- One choice for when the if-statement is true (then)
	- Another choice for when the if-statement is false (else)
	- Then the code continues:![[Screenshot 2025-05-20 at 10.40.53 AM 1.png]]
- If-elif statements:
	- elif: else if statement
		- Tests for a second condition
		- If the first if-statement is false, the control will continue to the else-if statement
	- Like this:![[Screenshot 2025-05-20 at 10.43.41 AM 1.png]]


-------------------------------------------------------------------

## **May 21 & 22: Lesson 5 & 6**

***Warm-up exercise:***![[Screenshot 2025-05-21 at 9.57.42 AM.png]]

***F-strings:***
- Formatted string literals
- Example: print(f“They are {30 + 1}”) → returns “They are 31”
	- Curly brackets ONLY surround the things to be converted to strings
	- Quotes surround the entire output
- Another example: ![[Screenshot 2025-05-21 at 10.14.17 AM.png]]

***Types of arguments:***
- **Keyword arguments:**
	- Values are assigned based on parameter names
	- Order does not matter
- **Positional arguments:**
	- Values are assigned based on order of arguments/parameters
	- Order does matter

***Named constants:***
- Variables that hold a value that does not change throughout the program
- Naming convention: all uppercase, underscores for spaces

***Default parameters:***
- Parameter in a function signature that is assigned a default value
- If a function call does not override the default value, then the default value is used
- Default parameters come after normal parameters

***Recursion:***
- Stack overflow/recursion error: function call stack overflows as a result of a function calling itself infinitely
- Avoiding recursion errors:
	- **Base cases:**
		- A branch in a recursively defined function that does not recur
		- Typically an if-statement
	- **Edge cases:**
		- Unlikely inputs - tested to ensure the function always works properly
	- **Recursive cases:**
		- Change the arguments of recursive calls so that they make progress towards a base case
		- Typically an else-statement

***Resources:***
- Resources on f-strings: https://comp110-25ss1.github.io/lessons/strings.html
- Resources on recursion: https://comp110-25ss1.github.io/lessons/recursion.html


-------------------------------------------------------------------

## **May 27: Lesson 7**

***Variables:***
- **Variable declaration:**
	- Done after a function definition
	- Type is stated and value is provided: **name: type = x** 
	- Similar to parameters
- **Variable assignment**: binding a new value to a variable with **=** operator
	- **Variable initialization:** *first time* a variable is assigned a value
- **Variable access:** reading or using a variable in an expression or return statement
- Variables are useful (vs parameters) because we can assign return values of function calls to variables for reference later
- Stored in memory diagrams within a function call frame (in stack, not globals)
	- **Do not write the variable as the return value**
- **Common variable errors:**
	- UnboundLocalError: attempt to access a variable that has been declared but not initialized
	- NameError: attempt to access a variable that has not been declared

***While-loops:***
- Conditional loops
- Unlike if-statements, while-loops incorporate repeat blocks following a test condition
	- As long as the test condition is true, the repeat will continue
	- When the test condition is false, the code progresses to the next statement
	- To avoid infinite running, while loops must progress towards the false condition
- **Syntax:**
	- while **condition**:
		- execute repeat block
	- next statement
- For a **while** loop **(n)** with a nested **if** loop **(m)**, we will iterate through it **n • m** times


-------------------------------------------------------------------

## **May 28: Lesson 8**

***Relative reassignment operators:***
- Example: 
	  **var: int = 1** 
	  **var = var + 1**
	  INSTEAD: **var += 1**
- Works for all operators (addition, subtraction, division, multiplication, etc)

***Lists:***
- Data structures (**sequences**) that allow us to organize the data for more efficient access
- Lists are mutable - their values can be changed after initialization
- Length is not fixed, but must be finite
- Printing a list prints the list literal
- Lists are stored in **globals** in memory diagrams, and when they called as parameters, the **id** is listed in place of a value
- To access a list within a list, use the following syntax: `list_name[index value][index value]`
	- For example: `deeznuts[0][1]`
- Lookups are slow and difficult
- Duplicates are allowed

| Feature                    | Syntax                         | Purpose                                                       |
| -------------------------- | ------------------------------ | ------------------------------------------------------------- |
| **Parameter format**       | var: list[type]                | Declaring a list parameter                                    |
| **Type Declaration**       | list_name: list[type]          | States the type of the list                                   |
| **Constructor (function)** | list_name: list[type] = list() | The constructor is a function that returns the literal **[]** |
| **List Literal**           | list_name: list[type] = []     |                                                               |
| **Access Value**           | list_name[index]               | Accesses a value at a given index                             |
| **Assign Item**            | list_name[index] = item        | Assigns the item at a given index                             |
| **Length of List**         | len(list_name)                 | Checks the length of a list                                   |
| **Remove Item**            | list_name.pop(index)           | Removes item at a specified index                             |
| **Append item**            | list_name.append(item)         | Adds a value to the end of the list                           |

-------------------------------------------------------------------

## **May 29: Lesson 9**

***Reference types:***
- Reference types refer to an exact location (address) in memory
- Multiple lists can be housed in the same ID in memory diagrams
	- They can be updated simultaneously


-------------------------------------------------------------------

## **June 2: Lesson 10**

***General:***
- **in** operator refers to items in a given lists/category

***Sets:***
- **set[type]** is a data structure for storing variables 
- **sets** are unordered and each value must be unique - duplicates are not allowed
- You cannot index **sets**
- Lists of values are stored within curly braces **{}**
- Adding a value to a set: **set.add()**
- Removing a value from set: **set.remove()**
- Lookups are fast
- Sets are called in alphabetical, ascending order?

| Feature                    | Syntax                      | Purpose                                                       |
| -------------------------- | --------------------------- | ------------------------------------------------------------- |
| **Type Declaration**       | set_name: set[type]         | States the type of the set                                    |
| **Constructor (function)** | set_name: set[type] = set() | The constructor is a function that returns the literal **{}** |
| **Set Literal**            | set_name: set[type] = {}    |                                                               |
| **Assign/add Item**        | set_name.add(item)          | Assigns/adds an item                                          |
| **Length of Set**          | len(set_name)               | Checks the length of a set                                    |
| **Remove Item**            | set_name.remove(item)       | Removes item                                                  |

***Dictionaries:***
- **dict[type, type]** is a data structure for storing variables
- **dictionaries** are indexed by **keys** associated with **values**, forming key-value pairs
	- This is known as **one-way mapping** - you can only search by **keys**, not **values**
- Lists of values are stored within curly braces **{}
- To add a value, state the new key and its new value: **dict[key] = value**
- Duplicate values are allowed, but not duplicate keys
- To check if **key** is present in a **dict**, use **in**: **key in dict**
- To remove an item: **dict.pop(key)**
- Lookups are fast

| Feature                    | Syntax                               | Purpose                                                       |
| -------------------------- | ------------------------------------ | ------------------------------------------------------------- |
| **Parameter format**       | var: dict[type, type]                | Declaring a dict parameter                                    |
| **Type Declaration**       | dict_name: dict[type, type]          | States the types of keys and values                           |
| **Constructor (function)** | dict_name: dict[type, type] = dict() | The constructor is a function that returns the literal **{}** |
| **Dict Literal**           | dict_name: dict[type, type] = {}     |                                                               |
| **Access Value**           | dict_name[key]                       | Accesses a value for a given key                              |
| **Assign Item**            | dict_name[key] = value               | Assigns a value for a given key                               |
| **Length of Dict**         | len(dict_name)                       | Checks the length of a dict                                   |
| **Remove Item**            | dict_name.pop(key)                   | Removes item at a specified key                               |

***For loops:***
- **for** loops iterate over every item in a list/dict/set by default
- Example: **for item in list: print(item)**
- YIPPEEEEE!


-------------------------------------------------------------------

## **June 4: Lesson 12**

***General***
- I am fucking stupid and I hate computer!


-------------------------------------------------------------------

## **June 5: Lesson 13**

***Testing functions***
- Key questions when designing tests:
	- What are the use cases (typical arguments) and expected return values?
	- What are the edge cases and expected return values?
		- Examples: empty strings, incorrect inputs
- **Unit testing:** using functions to test the validity of other functions
	- Strategy:
		- Create a skeleton for your main function
		- Come up with use and edge cases
		- Write a test function to call main function
		- Use test function return to troubleshoot the main function
- **Regressions:** disrupting older code with newer code
- File conventions: 
	- Testing files end with `_test`
	- Testing functions begin with `test_`
	- You have to use the beaker or terminal to run functions, not the play button
	- **Tests do not have parameters**
	- Formatting: 
		- **def test_func() → None:**
			  **assert x**


-------------------------------------------------------------------

## **June 9: Lesson 14**

***Object-orientated programming***
- In the real world, objects can be physical or abstract
- In python, objects are different types of data that can be used in different ways
	- Objects are instances of types and instances of **classes**
	- **Classes** are like templates, and objects are like one prototype of the template
	- **Object characteristics:**
		- Data type
		- Internal data representation
		- Set of procedures for usage
		- Interface for interacting with the object
			- Defines behaviors but hides implementation
- **Abstraction:** in classes, we only want to keep track of relevant information
- **Object formatting:**![[Screenshot 2025-06-09 at 10.06.36 AM.png]]
	- **Classes** use **attributes**, similar to **parameters**
		- Attributes are declared (first block), then initialized (second block)
		- Attributes can be updated
		- Attributes are accessed with periods
	- **Classes** use **methods**, functions defined within a class (start of second block)
		- The whole second block here is the **initializer** of this class
		- Every **method** has an **initializer** with the same formatting
		- **self** is always the first parameter in a **method**, and refers to the location where the method is stored in memory
		- In function calls, the **initializer** will always return what **self** returns
	- **Instantiation:** calling and creating an empty class object (**my_prof: Profile = Profile()** here)
	- **Magic methods:** ways to print classes
		- `def __str__(self) -> type:` allows for readable printing of method calls![[Screenshot 2025-06-12 at 10.48.44 PM.png]]
- **Adding a follower (method calling):**![[Screenshot 2025-06-09 at 11.04.18 AM.png]]


-------------------------------------------------------------------

## **June 11: Lesson 15**

***Linked lists***
- **Nodes** contain values and can refer to other nodes as values
- Below, “next” refers to the next **node** - “None” indicates that there are no other nodes
	- The first **node** is referred to as the **head**
	- Using recursion, we can test the number of total **nodes** by determining whether each **node** leads to another **node**… super efficient
		- Base case is **next = None**
	- When creating nodes, we have to work from **right** to **left**, starting with the final node
		- The first node cannot refer to another node that does not yet exist
- **Example format:**![[Screenshot 2025-06-12 at 11.02.21 PM.png]]

| node      |      |
| --------- | ---- |
| **Value** | 1    |
| **next**  | None |

