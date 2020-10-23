# Clean Code

In this repository is going to be summmary of the book `Clean Code by Robert C. Martin`, I really hope that this information help you to improve your programming skills.

`Refactoring or cleaning up our code is a lot like solving a Rubik's cube. There are lots of little steps required to achieve a large goal. Each step enables the next.`

* [Chapter 1 - Clean Code](#Chapter-1---Clean-Code)
* [Chapter 2 - Meaninful Names](#Chapter-2---Meaningful-Names)
* [Chapter 3 - Functions](#Chapter-3---Functions)
* [Chapter 4 - Comments](#Chapter-4---Comments)
* [Chapter 5 - Formating](#Chapter-5---Formating)
* [Chapter 6 - Objects and Data Structures](#Chapter-6---Objects-and-Data-Structures)
* [Chapter 7 - Error Handling](#Chapter-7---Error-Handling)
* [Chapter 8 - Boundaries](#Chapter-8---Boundaries)
* [Chapter 9 - Unit Test](#Chapter-9---Unit-Test)
* [Chapter 10 - Classes](#Chapter-10---Classes)
* [Chapter 11 - Systems](#Chapter-11---Systems)
* [Chapter 12 - Emergence](#Chapter-12---Emergence)
* [Chapter 13 - Concurrency](#Chapter-13---Concurrency)
* [Smells and Heuristics](#Smells-and-Heuristics)


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

### Use Searchable Names

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

## Chapter 6 - Objects and Data Structures.

- There is a reason that we keep our variables private. We don't want anyone else to depend on them.

- Hiding implementations is not just a matter of putting a layer of functions between the variables. Hiding implementation is about abstractions! A class does not simply push its variables out through getter and setter. Rather it exposes abstract interfaces that allow the user to manipulate the essence of the data, without having to know its implementation.

- Objects hide their data behind abstractions and expose functions that operate on that data. Data Structures expose their data and have no meaningful functions.

## Chapter 7 - Error Handling

- Things can go wrong and when they do, we as programmers are responsible for making sure that our code does what it needs to do.

- Error handling is important, but if it obscures the logic, it's wrong.

- Use exceptions rather than return codes.

- Use Unchecked exceptions, the price of checked exceptions is an Open/Closed Principle violation. If you throw a checked exceptions from a method in your code and the catch is three levels above, you must declare that expcetion in the signature of each method between you and the catch. This means that a change at a low level of the software can force signature changes on many higher levels. Also Encapsulation is broken because all the functions in the path of a throw must know about detail of that low-level exceptions.

- Each Exception that you throw should provide enough context to determine the source and location of an error.

- Dont Return null, when we are returning null, we are essentially creating work for ourselves and foisting problems upon our callers. All it takes is one missing null check to send an application spinning out of control.

- Dont pass null, returning null from methods is bad, but passing null into methods is worse. You should avoid passing null whenever possible.

## Chapter 8 - Boundaries

- We seldom controll all the software in our system. Sometimes we buy third party packages or use open source.

- Learning a third party code is hard. Integrating the third party code is hard too. Doing both at the same time is doubly hard.

- A good approach to undersntad third party is write some tests to explore our understanding of the third party code. Those test are known as `learning test`.

- In learning test we call the third party API, as we expect to use it in our application. We're essentially doing controlled experiments that check our understanding of that API.

- Learning tests are better than free, we had anyway to learn the API, and writting those tests was an easy and isolated way to get that knowledge.

## Chapter 9 - Unit Test 

Nowadays I would write a test that made sure that every nook and cranny of that code worked as I expected it to.

- Without a test suite they lost the ability to make sure that changes to their code base worked as expected. Without a test suite they could not ensure that changes to one part of their system did not break other parts of their system.

- Test code is just as important as production code. It is not a second-class citizen. It requires thought, design, and care. It must be kept as clean as production code.

- Is is unit test that keep our code flexible, maintainable, and reusable. The reason is simple, if you have test, you do not fear making changes to the code! Without test every change is a possible bug

### The Three Laws of TDD

1. *First Law*: You may not write production code until you have written a failing unit test.

2. *Second Law*: You may not write more of a unit test that is sufficiente to fail, and not compiling is failing

3. *Third Law*: You may not write more production code than is sufficient to pass the currently failing test.

### Keeping Tests Clean

- Having dirty test is equivalent to, if not worse than having no test. The problem is that test must change as the production code evolves. The dirtier the test, the harder they are to change.

- What makes a clean test? Three things. Readability, readability and readability. What makes a test readable? The same thing that makes the code readable: clarity, simplicity, and density of expression

- Single Assert Per Test

- Single Concept per test, we dont want long test functions that go testing one miscellaneous thing after another.

### F.I.R.S.T

Clean test follow five other rules.

 - *Fast*: Test should be fast. They should run quickly. When tests run slow, you wont want to run them frequently. If you don't run them frequently, you wont find problems early enough to fix them easily.

 - *Independent*: Test should not depend on each other. One test should not set up the conditions for the next test. You should be able to run each test independently and run the tests in any order you like.

 - *Repeatable*: Test should be repeatable in any environment, you should be able to run the test in the production environment, in qa environment and on your laptop while riding home on the train without network.

 - *Self-Validating*: Test should have a boolean output. Either they pass or fail. You should not have to read though a log file to tell wheter the tests pass.

 - *Timely*: The test need to be written in a timely fashion. Unit tests should be written just before the production code that makes them pass. If you write tests after the production code , then you may find the production code to be hard to test.

 ## Chapter 10 - Classes

 - Classes should be smmal, the first rule of classes is that they should be small. The second rule of classes is that they should be smaller than that.

 - With function we measured size by counting physical lines. Which classes we use a different measure. We count responsability

 - The Single Responsability principle states that a class or module should have one, and only one, reason to change. This principle gives us both a definition of responsability, and a guideline for class size. Classes should have one responsability-one reason to change

 - We want our system to be composed of many small classes , not a few large ones. Each small classes encapsulates a single responsibility, has a single reason to change, and collaborates with a few others to achieve the desired system.

 ### Cohesion

 - Classes should have a small number of instance variables. Each of the methods of a class should manipulate one or more of those variables. In general the more variables a method manipulated the more cohesive that method is to its class. A class in which each variable is used by each method is maximally cohesive.

 - We would like cohesion to be hight, when cohesion is high, it means that the methods and variables of the class are co-dependent and hang together as a whole.

 - When classes lose cohesion, split them.

 ## Chapter 11 - Systems

 Could you manage all the details yourself? Probably not. Even managing an existing city is too much for one person. Cities also also work because they have evolved apropiate levels of abstraction and modularity that make it posible for individuals and the "components" they manage to work effectively, even without understanding the big picture.

 - Software system should separate the startup process, when the application objects are constructed and the dependencies are wired togethe, from the runtime ñpgic that takes over after startup.

 - One way to separate construction from use is simply to move all aspects of construction to main, or modules called by main, and to design the rest of the system assuming that all objects have been constructed and wired up appropriately.

- System need domain specific languages(DSL), a good DSL minimizes the communication gap between a domain concept and the code that implements it. If you're implementing domain logic in the same language that a domain uses, there is less risk that you will incorrectly translate the domain into the implementations.

 ### Dependency Injection

 - A powerful mechanism for separating construction from use is Dependency Injection(DI), the application of Inversion of Control (IoC) to dependency management. Inversion of control moves secondary responsibilities from an object to other objects that are dedicated to the purpose, thereby supporting the Single Responsibility principle.

 - True dependency injection goes one step further. The class takes no direct steps to resolve its dependencies; It is completely passive instead, it provides setter methods or constructor arguments, that are used to inject the dependencies.

 ## Chapter 12 - Emergence

 A desing is simple if it follow these rules

 ### Runs all the test

 - A system that acts as intended. A system might have a perfect design on paper. But if there is no simple way to verify that the system actually works as intended, then all the paper effort is questionable.

 - The fact that we have these test eliminates the fear that cleaning up the code will break it.

 ### Contains no duplication

 - Duplication is the primary enemy of a well-design system. It represents additional work, aditional risk, and aditional unnecessary complexity.

 ### Expressive.

 - It's easy to write code that we understand, because at the time we write it we're deep in an understanding of the problem we're trying to solve. Other mainteners of the code arent going to have so deep an understanding.

 - The clearer the author can make the code, the less time others will have to spend understanding it. This will reduce defects and shrink the cost of maintenance.

## Chapter 13 - Concurrency

Objects are abstractions of processing. Thread are abstractions of schedule.

Writing clean concurrent programs is hard- very hard. It is much easier to write code that executes in a single thread. It is also easier to write multithreaded code that looks fine on the surface but is broken at a deeper level.

### Why Concurrency

Concurrency is a decoupling strategy. It helps us decouple what gets done from when it gets done. In single thread application what and when are so strongly coupled that the state of the entire application can be determined by looking at the stack backtrace.

Decoupling what from when can dramaticaly improve both the throughput and structures of an application. From a structural point of view the application looks like many litle collaborating computers rather than one big main loop.

### Concurrency Defense Principles

- Keep your concurrency-related code separate from other code.

- Take data encapsulation to heart; severely limit the acess of any data that may be share.

- Attempt to partition data into independent subsets than can be operated on by independent threads, possible in different procesors.

- Avoid using more than one method on a shared object.

- Keep your synchronized sections as small as possible.

- Write tests that have the potential to expose problems and then run them frequently, with different programatic configurations and system configurations and load. If tests ever fail, track down the failure. Don't ingore a failure just because the test pass on a subsequent run.

- Make your thread-based code especially pluggable so that you can run it in varios configurations.

## Smells and Heuristics

- Innapropriate Information

- Obsolote Comment

- Redundant Comment

- Poorly Written Comment

- Commented-Out Code

    `When you see commented-out code, delete it! Dont worry, the source control system still remembers it.`

- Build requires more than one step

- Test requires more than one step

- Too Many Arguments

- Flag Arguments

- Dead functions

- Multiple Languages in one source file

- Duplication

- Code at wrong level of abstraction

- Base classes depending on their derivates.

- Too much information

- Dead Code

    ` Dead code is code that isn't executed`

- Vertifical Separation

    ` Variables and function should be defined close tow ehere they are used.`

- Inconsistency

    ` If you do something a certain way, do all similar thing in the same way`

- Artificial Coupling

    ` Things that dont depend upon each other should not be artificially coupled`

- Feature Envy

    ` The methods of a class should be interested in the variables and functiones of the class they belong to, and not the variables and functions of other class`

- Obscure Intent

    ` We want code to be expressive as posible`

- Misplacced Responsibility

    ` Code should be placed where a reader would naturally expect it to be`

- Use Explanatory Variables

- Functions Names should say what they do

- Prefer Polymorphism to If/else or Switch/Case

- Follow Standard Conventions

- Replace Magic Numbers with named constants

- Be precise

    ` When you make a decision in your code, make sure you make it precisely. Know why you have made it and how you will deal with any exceptions`

- Encapsulate Conditionals

    ` Boolean logic is hard enough to understand without having to see it in the context. Extract functions that explain the intent of the conditional.`

- Avoid Negative Conditionals

- Functions Should do one thing.

- Don't be Arbitrary

    ` Have a reason for the way you structure your code, and make sure that reason is communicated by the structure of the code. If a structure appears arbitrary, others will feel empowered to change it`

- Functions should descend only one level of abstraction

- Keep configurable data and high levels

- Avoid transitive navigation

    ` If A collaborates with B, and B collaborates with C, we dont want modules that use A to know about C (The Law of Demeter)`

- Avoid long import list by using wildcards

- Dont inherit constant

- Constants versus enums

- Choose descriptive names

- Use standard nomeclature where possible

- Unambiguous names

- Use long names for long scopes

- Avoid encodings

- Names should describe side-effects

- Insufficiente Tests

- Use a coverage tool

- Dont skip trivial tests

- An Ignored test is a question about an ambiguity

- Test should be fast
