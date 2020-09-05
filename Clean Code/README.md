# Clean Code

In this repository is going to be summmary of the book `Clean Code by Robert C. Martin`, I really hope that this information help you to improve your programming skills.

* [Chapter 1 - Clean Code](#Chapter-1---Clean-Code)
* [Chapter 2 - Meaninful Names](#Chapter-2---Meaningful-Names)
* [Chapter 3 - Functions](#Chapter-3---Functions)
* [Chapter 4 - Comments](#Chapter-4---Comments)
* [Chapter 5 - Formating](#Chapter-5---Formating)


## Chapter 1 - Clean Code

- Clean code is a code that has been taken care of. Someone has taken the time to keep it simple and orderly. They have paid appropriate attention to details. They have cared.

- Spending time keeping your code clean is not just effective, it's a matter of professional survival.

- The managers and marketers look to us for the information they need to make promises and commitments; even when they dont look to us, we should not be shy about telling them what we think.

- Managers aregoing to defend the schedule and requirements with passion; but that's their job. It's your job to defend the code with equal passion.

- In short, a programmer who writes clean code is an artist who can take a blank screen through a series of transformations until is elegantly coded system.

- Making the code easier to read actually makes it easier to write.

### Boy Scout Rule

`Leave the campground cleaner than you founf it.`

## Chapter 2 - Meaningful Names

### Use Intention-Revealing Names

- Choosing good names takes time but saves more than it takes. So take care with your names and change them when you find better ones. Everyones who reads your code(including you) will be happier if you do.

- The Name of a variable, function, or class, should answer all the big questions. It should tell you why it exists, what it does, and how it is used.

### Use Pronounceable Names

- Humans are good at words. A significant part of our brains is dedicated to the concept of words. And words are, by definition pronounceable.

### Use Searchabñe Names

- Single-letter names and numeric constants have a particular problem in that they are not easy to locate across a body text. One might easily grep for MAX_CLASSES_PER_STUDENT, but the number 7 could be more troublesome.

### Avoid Mental Mapping

- Readers shouldnt have to mentally translate your names into other names they already know.

### Class Names

Classes and objects should have noun or noun phrase names like Customer or Account. A class name should not be a verb.

### Method Names

- Methods should have verb or verb phrase names.

### Use Solution Domain Names

- Remember that the people who read  your code will be programmers. So go ahead and use computer science terms, algorithm names, pattern names, math names and so forth.

## Chapter 3 - Functions

### Small

- The first rule of functions is that they should be small. The second rule of functions is that they should be smaller than that.

### Blocks and Indenting

- Functions should not be large enough to hold nested structures. Therefore, the indent level of a function should not be greater that one or two. This, of course, makes the functions easier to read and understand.

### Do One thing

`FUNCTIONS SHOULD DO ONE THING. THEY SHOULD DO IT WELL. THEY SHOULD DO IT ONLY`

### One Level Of Abstraction per Function

- In order to make sure our functions are doing "one thing" we need to make sure that the statements within our function are all at the same level of abstraction.

### The Stepdown Rule

- We want to be able to read the program as though it were a set of paragraphs, each of which is describing the current level of abstraction and referencing subsequent paragraphs to the next level down.

### Switch Statements 

- It's also hard to make a switch statement that does one thing. By their nature switch statements always do N things. Unfortunately we cant always avoid switch statements, but we can make sure that each switch statement is buried in a low-level class and is never repeated. We do this, of course with polymorphism.

- My general rule for switch statement is that they can be tolerated if they appear only once, are used to create polymorphic objects, and are hidden behind inheritance.

### Descriptive Names

- Dont be afraid to make a name long. A long descriptive name is better than a short enigmatic name.

- Choosing descriptive names will clarify the design of the module in your mind and help you to improve it.

### Function Arguments

- The Ideal number of arguments for a function is zero (niladic). Next comes one(monadic), followed closely by two (dyadic). Three arguments (triadic) should be avoided where posible. More than three (polyadic) requires very special justification-and then shouldnt be used anyways.

- When a function seems to need more than two arguments. It is likely that some of those arguments ought to be wrapped into a class of their own.

### Flag Arguments

- Flag arguments are ugly. Passing a boolean into a function is a truly terrible practice. It immediately complicates the signature of the method, loudly proclaiming that this functions does more than one thing.

### Have No Side Effects

- Side effects are lies. Your function promises to do one thing, but it also does other hidden things.

### Command Query Separation.

- Functions should either do something or answer something, but not both. Either your function should change the state of an object , or it should return some information about that object.

### Don't Repeat Yourself

- Duplication may be the root of all evil in software. Many principles and practices have been created for the purpose of controlling or eliminating.

## Chapter 4 - Comments

`Dont Comment Bad code`

- The proper use of comments is to compensate for our failure to express ourself in code. Note that I used the word failure. I meant it. Comments are always failures.

- Inaccurate comments are far worse than no comments at all. They delude and mislead. They set expectations that will never be fulfilled.

- Truth can only be found in one place: The code. Only the code can truly tell you what it does.

- Clear and expressive code with fre comments is far superior to cluttered and complex code with lots of comments.

- Sometimes our corporate coding standars force us to write certain comments for legal reason.

- If you're writing a public API, then you should certainly write good javadocs for it. But keep in mind the rest of the advice in this chapter. Javadocs can be just as misleading, nonlocal, and dishonest as any other kind of comment.

- Dont use comment when you can use a function or a variable.

- Short functions dont need much description. A well-chosen name for a small function that does one thing is usually better than a comment header.

## Chapter 5 - Formating

- You should choose a set of simple rules that govern the format of your code, and then you should consistently apply those rules. If you're working on a team, then the team should agree to a single set of formatting rules and all members should comply.

- It appears to be posible to build significant systems out of files that are typically 200 lines long, with an upper limit of 500. Although this should not be a hard and fast rule, it should be considered very desirable. Small files are usually easier to understand than large files are.

- Concepts that are closely related should be kept vertically close to each other.

- If one function call another, they should be vertically close, and the caller should be above the callee. If at all posible. This gives the program a natural flow.

- Regarding Horizontal formatting, How wide should a line be? I used to follow the rule that you should never have to scroll to the right.
