# Clean Code

## Good code.

When we are writing code we need to ensure a quality standart of the code and in order to achieve this code quality we need to keep in mind 
the nexts factors:

1. Simple
2. Organized
3. Clear
4. Easy to understand.
5. Easy to modified.
6. Not repeat code.
7. Easy to extend.

## Naming

### Reveal intention

``
hp
accountList
``

Instead of the above

``
hypotenuse
accounts
``

### Distintion with meaning

public void copyChars(char a1[], char a2[]) { 
    ...
}

Instead of the above

public static void copy(char source[], char destination[]) { 
    ...
}


### Use speakable variables

## Interfaces vs Implementations

``
IReader
ReaderImpl

// Would be better

Reader
InMemoryReader
DatabaseReader
``

## Use Nouns for Naming clases

## Use verb for naming methods

## Functions

1. Clear Naming.
2. Short Functions
3. Every functions must have just one reason of change.
4. Function must have in the same abstraction level.
5. Step Down Rule
6. Evade swicht statement.
7. Less Arguments is better -> More than 3 arguments could be a bad design.
8. Dont use flags
9. Use objects as parameters, instead of primitive types.
10. Dont have side effects.
11. Separate command/query
12. USe exceptions instead of error codes.
13. Dont repeat yourselft.!
14. Dont use try/catch.

## Comments

1. Try to dont use comments.
2. If you think a comment is require first think is re-write your code.
3. Some comments are good like legal comments or to explain high complex algorithms.
4. If there is something pending a todo is a valid comment.


## Formatted

1. Vertical
	- Amount of line per method. (Acceptable size 10-20 lines)
	- Group methods by their responsability and their relations.
	- Know when to use a blank line.

2. Horizontal	
	- Amount of characteres per line (Define the amount of characteres per line 80-120)
	- Divide parameters by space

	- 
	
## DTO

Is only require when we need to transfer info.

## Active record

An active record could an abstraction that maps one to one to database tables.


## Exceptions

1. Use unchecked exceptions when is posible.
2. Deal with expcetion in the methods
3. Never return null -> Return a Null Object (It is an object that represent that object but it is empty)

## Code Smell

### Duplicated Code

Disadvantages.

1. Complex to update (Because the code is repeat you have to update every update in all the places.)

Solutions

1. If within the same class is repeat code we could extract the repeated code into a new private method.
2. If two related classes use the same code, we could use the inheratance in order to use the repeat code.
3. Also we can use composition in order to solve the problem

### Long Methods

What is a long method?

It depends

- Method with more than 10-20 lines
- Methods that does not fit in the screen

Whatever which definition of "long method" you choose, the important here is that all the team share the same idea.

### Long classes

Usually when a class grows a lot we idenfied that the Single Responsability principle is being broken, for this reason
we need to split up that class.

1. Split up classes and use composition
2. Create a subclass.


