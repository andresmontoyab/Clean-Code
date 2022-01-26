# Clean Architecture

In this repository is going to be summmary of the book `Clean Architecture by Robert C. Martin`, I really hope that this information help you to improve your programming skills.

`Getting it right is another matter entirelt. Getting software right is hard. It takes knowledge and skills that most young programmers havent yet acquired. It requires thought and insight that most programmers dont take the time to develop. It requires a level of discipline and dedication the most programmers never dreamed they  would need. Mostly, it takes a passion for the craft and desire to be a professional.`

* [Introduction](#Introduction)
    * [What Is Design And Architecture](#What-Is-Design-And-Architecture)
    * [A Tale Of Two Values](#A-Tale-Of-Two-Values)
* [Programming Paradigms](#Programming-Paradigms)
    * [Paradigm Overview](#Paradigm-Overview)
    * [Structured Programming](#Structured-Programming)
    * [Object Oriented Programming](#Object-Oriented-Programming)
    * [Functional Programming](#Functional-Programming)
* [Design Principles](#Desing-Principles)
    * [Single Responsability Principle](#Single-Responsability-Principle)
    * [Open Closed Principle](#Open-Closed-Principle)
    * [The Liskob Substitution Principle](#The-Liskob-Substitution-Principle)
    * [The Interface Segregation Principle](#The-Interface-Segregation-Principle)
    * [The Dependency Inversion Principle](#The-Dependency-Inversion-Principle)
* [Component Principles](#Component-Principles)
    * [Components](#Components)
    * [Component Cohesion](#Component-Cohesion)
        * [The Reuse/Release Equivalent Principle](#The-Reuse/Release-Equivalent-Principle)
        * [The Common Closure Principle](#The-Common-Closure-Principle)
        * [The Common Reuse Principle](#The-Common-Reuse-Principle)
        * [Tension Diagram ](#Tension-Diagram)
    * [Component Coupling](#Component-Coupling)
        * [The Acyclic Dependencies Principle](#The-Acyclic-Dependencies-Principle)
            * [Breaking The Cycle](#Breaking-The-Cycle)
        * [The Stable Dependencies Principle](#The-Stable-Dependencies-Principle)
        * [The Stable Abstractions Principle](#The-Stable-Abstractions-Principle)
        
        

    

# Introduction

## What Is Design And Architecture


- The word `architecture` is often used in the context of something at high level that is divorced from the lower-level details, whereas `design` more often seems to imply structures and decisions at a lower level.

- The low-level details and the high-level structure are all part of the same whole

- The goal of software architecture is to minimize the huma resources required to build and maintain the required system.

- The measure of design quality is simply the measure of the effort required to meet the needs of the customer. If that effort is low,
and stays low throughout the lifetime of the system, the design is good. If that effort grows with each new release, the design is bad. It is simple as that.

- These developers buy into a familiar lie: "We can clean it up later; we just have to get to market first!" Of course, things never do get cleaned up later, because market pressures never abate.

- The bigger lie that developers buy into is the notion that writting messy code makes them go fast in the short term, and just slows them down in the log term. The fact is that making messes is always slower than staying clean, no matter which time scale you are using.

- The only way to reverse the decline in productivity and the increase in cost is to get the developers to stop thinking like overconfident Hare and start taking responsability for the mess that they have made.

- Their overconfidence will drive the redesign into the same mess as the original project.


## A Tale Of Two Values

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

# Programming Paradigm

## Paradigm Overview

- `Structured Programming imposes discipline on direct transfer control`
- `Object-oriented programming imposes discipline on indirect transfer of control`
- `Functional Programming imposes discipline upon assignment`

The paradigms tell us what not to do, more than they tell us what to do.

## Structured Programming

- Structured Programming, as name suggests, is a technique that is considered as precursor to OOP and usually consists of well-structured and separated modules. In this programming, user can create its own user-defined functions as well as this methodology tries to resolve issues that are associated with unconditional transfers to allow programmers follow logic of programs. It also requires more discipline at the design and logical structing stage.

- In all structured programming languages, an unconditional transfer of control, or goto statement, is deprecated and sometimes not even available.

In structured programming we trust in:

- Sequences(`set of steps`)
- Repetitions(`while and for`)
- Structed control flow constructs of selection(`if/then/else`)

## Object Oriented Programming

- The basis of a good architecture is the understanding and application of the principles of object-oriented design(OOP)

- The implication is that OO is the proper admixture of these three things, or at least that an OO language must support these three things. 

1. Encapsulation: OO provide easy and effective encapsulation of data and functions.
2. Inheritance: Inheritance is simply the redeclaration of a group of variables and functions within an enclosing scope.
3. Polymorphism: Is an application of pointers to functions. The problem with explicitly using pointers to functions to create polymorphic behavior
is that pointers to functions are dangerous. OO languages eliminate these conventions and therefore, these dangers. Using OO language makes polymorphism trivial.

## Functional Programming

In Many ways, the concepts of functional programming predate programming itself. The paradigm is strongly based on the lambda-calculus invented by Alonzo Church in the 1930s.

- Variables in functional programming do not vary.
- All race conditions, deadlocks conditions, and concurrent update problems are due to mutable variables.
- One of the most common compromises in regard to inmutability is to segregate the application, or the services within the application, into mutable and inmutable components.

# Design Principles 

Good software system begin with clean code. On the one hand, if the bricks arent well made, the architecture of the building does not matter much. On the other hand, you can make a substancial mess with well-made bricks.

The goals of the principles is the creation of mid-level software structures that:

- Tolerate change.
- Are easy to understand 
- Are the basis of components that can be used in many software systems.

## Single Responsability Principle

Of all the SOLID principles the Single Responsability principle might be the least well understood.

It is too easy for programmers to hear the name and then assume that it means that every module should do just one thing.

```A module should have one, and only one, reason to change```

Software systems are changed to satisfy users and stakeholders: those users and stakeholders are the `reason to change` 

When we said `users` or `stakeholders` we are reffering to a group, one or more people who require that change. We will refer to that group as an actor.

Thus the final version of the SRP is:

``` A module should be responsible to one, and only one actor.```


The SRP says to separate the code that different actors depend on.

## Open Closed Principle 

``` A software artifact should be open for extension but closed for modification```

Clearly if simple extensions to the requirement force massive changes to the software, then the architects of the software system have engaged in a spectacular failure.

Open Closes Principle works at the architectural level. Architects separate functionality based on how, why and when it changes, and then organize that separated functionality into a hierarchy of components. Higher-level components in that hierarchy are protected from the changes, made to lower-level components.

The Open Closed Principle is one of the driving forces behind the architecture of systems. The goal is to make the system easy to extend without incurring a high impact of change. This goal is accomplished by partitioning the system into components, and arranging those components into a dependency hierarchy that protects higher-level components from changes in lower-level components.

## The Liskob Substitution Principle

In the early years of Object Oriented revolution, we though of the LSP as a way to guide the use of inheritance. However, over the year the LSP has morphep into a broader principle of software design that pertains to interface and implementation.

The best way to understand the LSP from an architectural viewpoint is to look at what happens to the architecture system when the principle is violate.

## The Interface Segregation Principle

It is harmful to depend on modules that contain more than you need. This is obviously true for source code dependencies that can for unnecessary recompilation and redeployment- but it is also true at a much higher level, architectural level.

The lesson here is that depending on something that carries baggage that you do not need can cause you troubles that you did not expect.
    
## The Dependency Inversion Principle 

The Dependency Inversion Principle (DIP) tells us that the most flexible systems are those in which source code dependencies refer only to abstractions, not to concretions.

Crearly, treating this idea as a rule is unrealistic, because software systems must depend on many concrete facilities, For example, the String class in Java is concrete, and it would be unrealistic to try to force it to be abstract.

It is the volatile concrete elements of our system that we want to avoid depending on. Those are the modules that we are actively developing and that are undergoing frequent change.

### Stable Abstractions.

Every change to an abstract interface corresponds to a change to its concrete implementations. Conversely, changes to the concrete implementations do not always, or even usaully, require changes to the interfaces that they implement. Therefore interfaces are less volatile than implementations.

Indeed, good software designers and architects work hard to reduce the volatility of interfaces. They try to find ways to add functionality to implementations without making changed to the interfaces. This is software design 101.

The implication, then that stable software architectures are those that avoid depending on volatile concretions, and that favor the use of stable abstract interfaces.

1. Dont refer to volatile concrete classes. Refer to abstract interfaces instead.
2. Dont derive from volatile concrete classes
3. Dont override concrete functions.
4. Never mention the name of anything concrete and volatile.

# Component Principles

If the SOLID principles tell us how to arrange the bricks into walls and rooms, then the component principles tell us how to arrange the rooms into buildings. Large software systems, like large buildings, are built out of smaller components.

## Components

Components are the unit of deployment. They are the smallest entities that can be deployed as part of the system.

Components can be linked together into a single executable. Or they can be aggregated together into a single archive.

Well desgined components always retain the ability to be independently deployable and therefore, independently developable.

## Component Cohesion

Which classes belong in which componenets? This is an important decision, and requires guidance from good software engineering principles.

In this chapter we will discuss the three principles of component cohesion:

1. REP: The Reuse/Release Equivalent Principle
2. CCP: The Common Closure Principle
3. CRP: The Common Reuse Principle

### The Reuse/Release Equivalent Principle

This principle means that classes and modules that are formed into a component must belong to a cohesive group.

Classes and modules that are grouped together into a component should be releasable together.

### The Common Closure Principle

``` Gather into components those classes that change for the same reasons and at the same time. Separate into different components those classes that change at different times and for different reasons.```

This is the Single Responsibility Principle restated for components.

If two classes are so tighly bound, either physically or conceptually, that they always change together, then they belong in the same component.

### The Common Reuse Principle

``` Do not force users of a component to depend on things they do not need```

Therefore the CRP tells us more about which classes should not be together than about which classes should be together.


``` Do not depend on things that you do not need ```

### Tension Diagram 

You may have already realized that the three cohesion principles tend to fight each other. The REP and CCP are `inclusive` principles. Both tend to make components larger. The CRP is an `exclusive` principle, driving components to be smaller.

![](https://github.com/andresmontoyab/Clean-Code/blob/master/resources/tension_diagram.jpeg) 

A good architect finds a position in that tension triangle that meets the current concerns of the development team, but is also aware that those concerns will change over time .

## Component Coupling

The next three principles deal with the relaionship between components.

### The Acyclic Dependencies Principle

``` Allow no cycles in the component dependency graph ```

When there are cycles in the dependency graph, it can be very difficult to work out the order in which you must build the components. Indeed, there probably is not correct order.

#### Breaking The Cycle

It is always possible to break a cycle of components and reinstate the dependency graph as a `direct acyclic graph`. There are two primary mechanism for doing so:

1. Apply the Dependency Inversion Principle (DIP)
2. Create a new component that both components depend on.


We dont want components that change frequently and for capricious reason to affect components that otherwise ought to be stable.

Consequently, the component dependency graph is created and molded by architects to protect stable high-value components from volatile components.

### The Stable Dependencies Principle

``` Depend in the direction of stability ```

Designs cannot be completely static. Some volatility is necessary if the design is to be maintained. By conforming to the CCP we create components that are sensitive to certain kinds of change but inmune to others. Some of these components are designed to be volatile. We expect them to change.

Any component that we expect to be volatile should not be depended on by a component that is difficult to change. Otherwise, the volatile component will also be difficult to change.

It is the perversity of software that a module that you have designed to be easy to change can be made difficult to change by someone else whosimply hangs a dependency on it. Not a line of source code in your module need change, yet your module will suddenly become more challenging to change. By conforming to `The Stable Dependencies Principle`, we ensure that modules that are intended to be easy to change are not depended on by modules that are harder to change.

``` Stability is related to the amount of work required to make a change ```

One sure way to make a software component difficult to change, is to make lots of other software components depend on it. A component with lots of incoming dependencies is very stable because it requires a great deal of work to reconcile any changes with all the dependent components.

If all the components in a system were maximally stable, the system would be unchangeable. This is not a desirable situation. Indeed, we want to desing our component structure so that some components are unstable and some are stable.

### The Stable Abstractions Principle

``` A component should be as abstract as it is stable ```

The stable abstractions principle sets up a relationship between stability and abstractness. On the one hand, it says that a stable component should also be abstract so that its stability does not prevent it from being extended. On the other hand, it says that an unstable component should be concrete since its instability allows the concrete code within it to be easily changed.

Thus, if a component is to be stable, it should consist of interfaces and abstract classes so that it can be extended. Stable components that are extensible are flexible and do not overly constrain the architecture.

``` Dependencies run in the direction of abstraction ```