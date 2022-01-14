# Clean Architecture

In this repository is going to be summmary of the book `Clean Architecture by Robert C. Martin`, I really hope that this information help you to improve your programming skills.

`Getting it right is another matter entirelt. Getting software right is hard. It takes knowledge and skills that most young programmers havent yet acquired. It requires thought and insight that most programmers dont take the time to develop. It requires a level of discipline and dedication the most programmers never dreamed they  would need. Mostly, it takes a passion for the craft and desire to be a professional.`

* [Chapter 1 - What Is Design And Architecture](#Chapter-1---What-Is-Design-And-Architecture)
* [Chapter 2 - Meaninful Names](###Chapter-2---A-Tale-Of-Two-Values)
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


## Chapter 1 - What Is Design And Architecture

- The word `architecture` is often used in the context of something at high level that is divorced from the lower-level details, whereas `design` more often seems to imply structures and decisions at a lower level.

- The low-level details and the high-level structure are all part of the same whole

- The goal of software architecture is to minimize the huma resources required to build and maintain the required system.

- The measure of design quality is simply the measure of the effort required to meet the needs of the customer. If that effort is low,
and stays low throughout the lifetime of the system, the design is good. If that effort grows with each new release, the design is bad. It is simple as that.

- These developers buy into a familiar lie: "We can clean it up later; we just have to get to market first!" Of course, things never do get cleaned up later, because market pressures never abate.

- The bigger lie that developers buy into is the notion that writting messy code makes them go fast in the short term, and just slows them down in the log term. The fact is that making messes is always slower than staying clean, no matter which time scale you are using.

- The only way to reverse the decline in productivity and the increase in cost is to get the developers to stop thinking like overconfident Hare and start taking responsability for the mess that they have made.

- Their overconfidence will drive the redesign into the same mess as the original project.


## Chapter 2 - A Tale Of Two Values

- Every software system provides two different values to the stakeholders: `behavior` and `structure`. Software developers are responsible for ensuring that both those values ramain high. Unfortunately, they often focus on one to the exclusion of the other.

### Behaviour

- The first value of software is its behavior. Programmers are hired to make machines behave in a way that makes or saves money for the stakeholders.

- Many programmers believe that is the entirety of their job. They believe their job is to make the machine implement the requirements and to fix any bugs. They are sadly mistaken

### Architecture

- To fulfill its purpose, software must be soft - that is, it must be easy to change. When the stakeholders change their minds about a feature, that change should be simple and easy to make.

- The more this architecture prefers one shape over another, the more likely new features will be harder and harder to fit into that structure. Therefore architectures should be as shape agnostic are practical.

___


- Functions or architecture? Which of these two provides the greater value? It is more important for the software system to work, or is it more important for the software system to be easy to change?. If you ask business managers, they will often say that it is more important for the software system to work. Developers, in turn, often go along with this attitude. But it is the wrong attitude.

1. `If you give a program that works perfectly but it is imposible to change, then it wont work when the requirement change, and wont be able to make it work. Therefore the progrman will become useless.`

2. `If you game a program that does not work but is easy to change, then I can make it work, and keep it working as requirements change. Therefore the program will remain continually usefull.`

-  The dilemma for software developers is that business managers are not equipped to evaluate the importance of architecture. `Thats what software developers were hired to`. Therefore it is the responsibility of the software development team to assert the importance of architecture over the urgency of features.

- Remember as a software developer you are a stakeholder. You have a stake in the software that you need to safeguard. thats part of your role, and part of your duty and its a great part of why you were hired .

- Just remember if architecture comes last, then the system  will become ever more costly to develop, and eventually changed will become practically impossiblefor part or all of the system. If that is allowed to happen, it means the software development team did not fight enough for what they knew was neccesary

## Chapter 3 - Paradigm Overview

- `Structured Programming imposes discipline on direct transfer control`
- `Object-oriented programming imposes discipline on indirect transfer of control`
- `Functional Programming imposes discipline upon assignment`

The paradigms tell us what not to do, more than they tell us what to do.

## Chapter 4 - Structured Programming

- Structured Programming, as name suggests, is a technique that is considered as precursor to OOP and usually consists of well-structured and separated modules. In this programming, user can create its own user-defined functions as well as this methodology tries to resolve issues that are associated with unconditional transfers to allow programmers follow logic of programs. It also requires more discipline at the design and logical structing stage.

- In all structured programming languages, an unconditional transfer of control, or goto statement, is deprecated and sometimes not even available.

In structured programming we trust in:

- Sequences(`set of steps`)
- Repetitions(`while and for`)
- Structed control flow constructs of selection(`if/then/else`)

## Chapter 5 - Oriented Programming

- The basis of a good architecture is the understanding and application of the principles of object-oriented design(OOP)

- The implication is that OO is the proper admixture of these three things, or at least that an OO language must support these three things. 

1. Encapsulation: OO provide easy and effective encapsulation of data and functions.
2. Inheritance: Inheritance is simply the redeclaration of a group of variables and functions within an enclosing scope.
3. Polymorphism: Is an application of pointers to functions. The problem with explicitly using pointers to functions to create polymorphic behavior
is that pointers to functions are dangerous. OO languages eliminate these conventions and therefore, these dangers. Using OO language makes polymorphism trivial.

