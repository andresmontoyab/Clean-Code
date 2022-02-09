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
* [Architecture](#Architecture)
    * [What is Architecture?](#What-is-architecture?)
        * [Development](#Development)
        * [Deployment](#Deployment)
        * [Maintenance](#Maintenance)
        * [Keeping Options Open](#Keeping-Options-Open)
    * [Independence](#Independence)
    * [Boundaries](#Boundaries)
    * [Policy And Level](#Policy-And-Level)
    * [Business Rules](#Business-Rules)
        * [Entities](#Entities)
        * [Business Use Case](#Business-Use-Case)
    * [Screaming Architecture](#Screaming-Architecture)
    * [The Clean Architecture](#The-Clean-Architecture)
    * [Partial Boundaries](#Partial-Boundaries)
    * [Layers and Boundaries](#Layers-and-Boundaries)
    * [The Main Components](#The-Main-Components)
    * [The Test Boundary](#The-Test-Boundary)
* [Details](#Details)
    * [The Database Is A Detail](#The-Database-Is-A-Detail)
    * [The Web Is A Detail](#The-Web-Is-A-Detail)
    * [Frameworks Are Details](#Frameworks-Are-Details)
* [The Missing Chapter](#The-Missing-Chapter)
    * [Package By Layer](#Package-By-Layer)
    * [Package By Feature](#Package-By-Feature)
    * [Ports And Adapters](#Ports-And-Adapters)
    * [Package By Component](#Package-By-Component)

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

# Architecture

## What is Architecture?

First of all, a software architect is a programmer: and continues to be a programmer. Never fall for the lie that suggest that software architects pull back from code to focus on high-level issues. They do not! Software architects are the best programmers, and they continue to take programming tasks, while they also guide the rest of the team toward a design that maximizes productivity. Software architects may not write as much code as other programmers do, but they continue engage in programming tass. They do this because they can not do their jobs properly if they are not experiencing the problems that they are creating for the rest of the programming.

The architecture of a software system is the shape given to that system by those who build it. The form of that shape is in the division of that system into components, the arrangement of those components, and the ways in which those components communicate with each other.

The purpose of that shape is to facilitate tge development, deployment, operation and maintenance of the software system contained within it.

``` The strategy behind that facilitation is to leave as many options open as possible, for as long as possible ```

The primary purpose of architecture is to support the life cycle of the system. Good architecture makes the system easy to understand, easy to develop, easy to mantain and easy to deploy. The ultimate goal is to minimize the lifetime cost of the system and to maximize programmer productivity.

### Development

A software system that is hard to develop is not likely to have a long and healthy lifetime. So the architecture of a system should make that system easy to develop, for the team who develop it.

### Deployment

To be effective , a software system must be deployable. the higher the cost of deployment, the less usefull the system is. A goal of a software architecture, then, should be to make a system that can be easily deployed with a single action.

### Maintenance

Of all the aspects of a software system, maintenance is the most costly. The never-ending parade of new features and the inevitable trail of defects and corrections consume vast amounts of human resources


### Keeping Options Open

Software was invented because we needed a way to quickly and easily change the behavior of machines.

The way you keep software soft is to leave as many options open as possible, for as long as possible. What are the options that we need to leave open? `They are the details that don matter`

All software systems  can be decomposed into two major elements: policy and details. The policy element embodies all the businessrules and procedures. The policy is where the true value of the system lives.

The details are those thing that are necessary to enable humans, other systems, and programmers to communicate with the policy, but that do not impact the behavior of the policy at all. They include I/O Device, databases, web systems, servers, frameworks, communication protocols and so forth.

The goal of the architect is to create a shape for the system that recognizes policy as the most essential elememnt of the system while making the details irrelevant to that policy.

If you can develop the high-level policy without committing to the details that surround it , you can delay and defer decisions about those details for a long time. And the longer you wait to make those decision, the more information you have with which to make them properly.

This also leaves you the option to try different experiments. If you have a portion of the high-level policy working, and it is agnostic about the database, you could try connecting it to several different databases to check applicability and performance.

``` A good architect maximizes the number of decisions not made. ```

## Independence

As we previously stated, a good architecture must support.

- The use cases and operation of the system.
- The Maintenance of the system.
- The Development of the system.
- The Deployment of the system

### Use Cases

The first bullet - use cases- means that the architecture of the system must support the intent of the system. If the system is a shopping cart application, then the architecture must support shopping cart use cases.

The most important thing a good architecture can do to support behavior is to clarify and expose that behavior so that the intent of the system is visible at the architectural level.

### Development

Architecture plays a significant role in supporting the development environment. This is where Conways Law comes into plays: Conways law says:

``` Any organization that designs a system will produce a design whose structure is a copy of the organizations communication structure ```

### Deployment

The architecture also plays a huge role in determining the ease with which the system is deployed. A good architecture helps the system to be inmmediately deployable after build.

Again, this is achieved through the proper partitioning and isolation of the components of the system, including those master components that tie the whole system together and ensure that each component is properly started, integrated, and supervised.

### Decoupling Modes

There are many ways to decouple layers and use cases. They can be decoupled at the source code level, at the binary code level and at the execution code level.

- `Source level`: We can control the dependencies between source code modules so that changes to one module do not force changes or recompilation of others.

- `Deployment Level`: We can control the dependencies between deployable units such as jar files.

- `Service Level`: We can reduce the dependencies down to the level of data structure.

What is the best mode to use?

One solution is to simply decouple at the service level by default.

My preference is to push the decoupling to the point where aservice could be formed. Should it become neccesary: but then to leave the components in the same address space as long as possible. This leaves the option for a service open.

A good architecture will allow a system to be born as a monolith, deployed in a single file, but then to grow into a set of independently deployable units, and then all the way to independent services and/or microservices.

## Boundaries

software architecture is the art of drawing lines that I call boundaries. Those boundaries separate software elements from one another, and restrict those on one side from knowing about those on the other.

### Which lines do you draw, and when do you draw them?

You draw lines between thing that matter and things that do not. The GUI does not matter to the business rules, so there should be a line between them. The database does not matter to the GUI, so there should be a line between them. The database does not matter to the business rules, so there should be a line between them.

Some of you may have rejected one or more of those statements, especially the part about the business rules not caring about the database. Many of us have been taught to believe that the database is inextricable connected to the business rules. Some of us have even been conviced that the database is the embodiment of the business rules.

The database is a tool that the business rules can use inderectly. The business rules do not need to know about the schema, or the query language, or any of the other details about the database. All the business rules need to know is that there is a set of functions that canbe used to fetch or save data. This allows us to put the database behind an interface.

The core business rules are kept separate from, and independent of those components that are either optional or that can be implemented in many different forms.

Boundaries are drawn where there is an axis of change. The components on oneside of the boundary change at different rates and for different reasons, than the component on the other side of the boundary.

This is the Single Responsibility principle again. The SRP tell us where to draw the lines.

You should recognize this as an application of the Dependency Inversion Principle and Stable Abstraction Principle. Dependency arrow are arranged to point from lower-level details to higher level abstractions

## Policy And Level

Software system are statements of policy. Indeed, at its core, that's all a computer programm actually is. A computer program is a detailed description of the policy by which inputs are transformed into outputs.

Policies that change for the same reasons and at the same times, are at the same level and belong together in the same component. Policies that change for different reasons or at different times, are at different levels and should be separated into different components.

### Level

A strict definition of `level` is `the distance from the inputs and outputs`. The farther a policy is from both the input and output of the system, the higher its level. The policies that maange the input and output are the lowest-level policies in the system.

Keeping these policies separate, with all sources code dependencies pointing in the direction of the higher-level policies, reduces the impact of change. Trivial but urgen changes at the lower levels of the system have little or no impact on the higher, more important, levels.

## Business Rules

Business Rules are rules or procedures that make or save the business money.

We shall call these rules `Critical Business Rules` because they are critical to the business itself, and would exist even if there were not system to automate them.

`Critical Business Rules` usually require some data to work with. We shall call this data `Critical Business Data`. This is the data that would exist even if the system were not automate.

The `Critical Rules` and `Critical Data` are inextricably bound, so they are a good candidate for and object. We will call this kind of object an `Entity`.

### Entities

An `Entity` is an object within our computer system that embodies a small set of `Critical business rules` operating on `Critical business Data`. The `Entity` object either contains the `Critical Business Data` or has very easy access to that data. The interface of the `Entity` consists of the functions that implement the critical business rules that operate on that data.

``` The Entity is pure business and nothing else```

### Business Use Case

Not all business rules are as pure as `Entities`. Some business rules make or save money for the business by defining and constraining the way that an `automated` system operates. These rules would not be used in a manual environment, because they make sense only as part of an automated system.

A `Use Case` is a description of the way that an automated system is used. It specifies the input to be provided by the user, the output to be returned to the user, and the processing steps involved in producing that output. A use case describes application-specific business rules as opposed to the Critical Business Rules within the entity.

```Use cases contains rules that specify how and when the Critical Business Rules within the Entities are invoked. Use cases control the dance of the Entities```

High-level concepts, such as Entities, know nothing of the lower-level concepts, such as use cases. Instead the lower level use cases know about the higher-level Entities.

The `Use Case` class accepts simple request data structures for its input, and return simple response data structure as its output. These data structure are not dependent on anything. They do not derive from standard framework interfaces such as `HttpRequest` and `HttpResponse`. They know nothing of the web, nor do they share any of trapping of whatever user interface might be place.

You might be tempted to have these data structures contain references to Entity objects. You might think this makes sense because the Entities and the request/response models share so much data. Avoid this temptation! The purpose of these two objects is very different. OVer time they will change for very different reasons, so trying them together in any way violates the Commom Closure and Single Responsibility Principle. The result would be lots of tramp data, and lots of conditionals in your code.

## Screaming Architecture

Just as the plans for a house or a library screams about the use cases of those buildings, so should the architecture of a software application scream about the use cases of the application.

A good software architecture allows decisions about frameworks, databases, web servers, and other environmental issues and tools to be deferred and delayed.

A good architecture emphasizes the use cases and decouples them from peripheral concers.

Your architecture should tell readers about the system, not about the framework you used in your system.

## The Clean Architecture

Over the last several decades we have seen a whole range of ideas regarding the architecture of systems.


![](https://github.com/andresmontoyab/Clean-Code/blob/master/resources/clean-architecture.jpeg) 

Although these architectures all vary somewhat in their details, they are very similar. They have the same objective, which is the separation of concerns.

Each of these architectures produces systems that have the following characteristics.

1. Independent of frameworks
2. Testable
3. Independent of the UI
4. Independent of the database
5. Independent of any external agency.

### The Dependency Rule

``` Source code dependencies must point only inwards, toward higher-level policies ```

Nothing in an inner circle can know anything at all about something in an outer circle. In particular, the name of something declared in an outer circle must not be mentioned by the code in an inner circle. That includes functions, classes, variables, or any other software entity.

### Entities

Entities encapsulate enterprise wide `Critical Business Rules. An Entity can be an object with methods, or it can be a set of data structures and functions. It does not matter so long as the entities can be used by many different applications in the enterprise.

### Use Cases

The Software in the use cases layer contains `application-specific` business rules. It encapsulates and implements all of the use cases of the system. These use cases orchestrate the flow of data to and from the entities, and direct those entities to use their `Critical Business Rules` to achieve the goals of the use case.

### Interface Adapters

The software in the interface layer is a set of adapters that convert data from the format most convenient for the use cases and entities, to the format most convinient for some external agency such as the database or the web.


### Frameworks and Drivers

The framework and drivers in this layer is where all the details go. The web is a detail. The database is a detail. We keep these things on the outside where they can do little harm.

## Partial Boundaries

In Many situations, a good architect might judge that the expense of such a boundary is too high, but might still want to hold a place for such a boundary in case it is needed later.

This kind of anticipatory design is often frowned upon by many in the Agile community as a violation of `YAGNI: You aren't going to need it`. Architects however, sometimes look at the problem and think, " Yeah, but I might", in that case they may implemenet a partial boundary.

One way to construct a partial boundary is to do all the work necessary to create independently compilable and deployable components, and then simply keep them together in the same component.

It is one of the functions of an architect to decide where an architectural boundary might one day exist, and wheter to fully or partially implement that boundary.

## Layers and Boundaries

As Software architect, you must see the future. You must guess--intelligently. You must weight the costs and determine where the architectural boundaries lie, and which should be fully implemented, and which should be partially implemented, and which should be ignored.

But this is not a one time decision. You do not simply decide at the start of the project which boundaries to implement and which to ignore. Rather, you `watch`. You pay attention as the system evolves. You note where boundaries may be required, and then carefully watch for the first inkling of friction because those boundaries does not exist.

At that point, you weigh the cost of implementing those boundaries versus the cost of ignoring them--and you review that decision frequently. Your goal is to implement the boundaries right at the inflection point where the cost of implementing becomes less than the cost of ignoring.

It takes a watchful eye.

## The Main Components

In every system, there is at least one component that creates, coordinates and oversees the others. I call this component `Main`

The `Main` component is the ultimate detail--the lowest level policy. It is the inital entry point of the system. Nothing, other than the operating system, depends on it. Its job is to create all the factories, strategies, and other global facilities, and then hand control over to the high-level abstract portions of the system.

The point is that `Main` is a dirty low-level module in the outermost circle of the clean architecture. It loads everything up for the high-level system, and then hands control over to it.

Think of `Main` as a plugin to the application-- a plugin that sets up the initial conditions and configuration, gathers all the outside resources, and then hands control over to the high-level policy of the application. Since it is a plugin, it is possible to have many `Main` components, for each configuration of your application.

## The Test Boundary

Yes, that's right: The test are part of the system, and they participate in the architecture just like every other of the system does.

Test by their nature, follow the dependency rule; They are very detailed and concrete; and they always depend inward toward the code beign tested. In fact, you can think of the tests as the outermost circle in the architecture. Nothing within the system depends on the tests, and the tests always depend inward on the components of the system. 

### Design for testability

Test that are not well integrated into the design of the system tend to be fragile, and they make the system rigid and difficult to change.

The issue, of course, is coupling. Test that are strongly coupled to the system must change along with the system. Even the most trivial change to a system component can cause many coupled tests to breakor require changes.

Changes to common system components can cause hundreds or even thousands of tests to break. this is known as the `Fragile Tests Problem`

The solution is to design for tesability. The first rule of software design wheter for testability or for any other reason is always the same: `Don't depend on volatile things`. GUI are volatile. Test suites that operate the system through the GUI must be fragile. Therefore design the system and the test so that business rules can be tested without using the GUI.

### Testing API.

The way to accomplish this goal is to create a specific API that the test can use to verify all the business rules.

### Structural Coupling

Image a test suite that has a test class for every production class, and a set of tets methods for every production method. Such a test suite is deeply coupled to the structure of the application.

When one of those production methods or classes changes, a large number of tests must be change as well. Consequently the test are fragile and they make the production code rigid.

The role of the testing API is to hide the structure of the application from the tests. This allows the production code to be refactored and evolved in ways that don't affect the tests. It also allows the tests to be refactored adn evolved in ways that do not affect the production code.

Tests are not outside the system; rather, they are parts of the system that must be well desgined if they are to provide the desired benefits of stability and regresion. Tests that are not desgined as part of the system tend to be fragile and difficult to maintain.

## Details

### The Database Is A Detail

From an architectural point of view, the database is a non-entity, it is a detail that does not rise to the level of an architecture element.

The database is a utility that provides access to the data. From the architecture's point of view, that utility is irreleant because it's a low-level detail, a mechanism. And a good architect does not allow low-level mechanism to pollute the system architecture.

Many data access framework allows database rows and tables to be passed around the system as objects. Allowing this is an architectural error. It couples the use cases, business rules, and in some cases even the UI to the relational structure of the data.

This reality is why I say the database is a detail. It's just a mechanism we use to move the data back and forth between the surface of the disk and RAM. The database is really nothing more than a big bucket of bits where we store our data on a long-terms basis. But we seldom use the data in that form.

Thus, from an architectural view point, we should not care about the form that the data takes while it is on the surface of a rotating magnetic disk. Indeed, we should not acknowledge that disk exist at all.

The organizational structure of data, the data model, is architecturally significant. The technologies and system that move data on and off a rotating magnetic surface are not. Relational databases system that force the data to be organized into tables and accessed with SQL have much more to do with the latter than with former. The data is significant. The database is a detail.

### The Web Is A Detail

Do you remember how we looked at our old client-server architectures with disdain in the face of the shiny new technology of the web?

Actually the web didn't change anything. Or, at least, it shouldn't have. The web is just the lattest in a series of oscillations that our industry has gone through since the 1960s. These oscillations move back and forth between putting all the computer power in central servers and putting all the computer power out at the terminals.

Of course, it would be incorrect to think that those oscillations started with the web. Before the web, there was client-server architecture. Before that, there were central minicomputers with arrays of dumbs terminals. Before that, there were mainframes with smart green-screen terminals. Before that, there were computer rooms and punched cards.

And so the story goes. We can't seem to figure out where we want the computer power. We go back and forth between centralizing it and distributing it. And, I Imagine those oscillations will continue for some time to come.

As architect, though, we have to look at the long term. Those oscillations are just short-term issues that we want to push away from the central core of our business rules.

The GUI os a detail. The Web is a GUI. So the web is a detail. And as an architect you want to put details like that behind boundaries that keep them separate from your core business logic.

### Frameworks Are Details

Frameworks have become quite popular. Generally speaking, this is a good thing. There are many frameworks out there that are free, powerful and useful.

However, frameworks are not architectures, though some try to be.

Framework authors know their own problems, and the problems of their coworkers and friends. And they write their frameworks to solve those problems, not yours.

You must make a huge commitment to the framework, but the framework author makes no commitment to you whatsoever.

```What are the risk?```

1. The Architecture of a framework is often not very clean. Frameworks tend to violate the Dependency rule. They asked you to inherit your code into your business objects, your Entities.

2. The framework may evolve in a direction that you don't find helpful. You may be stuck upgrading to new versions that don't help you.

3. A new and better framework may come along that you wish you could swicht to.

```What is the solutuon?```

```Don't marry the framework```

Oh, you can use the framework, just don't couple to it. Keep it at arm's length. Treat framework as a detail that belong in one of the outer circles of the architecture.

Don't let frameworks into your core code. Instead, integrate them into components that plug in to your core code, following the dependency rule.

## The Missing Chapter

All of the advice you've read so far will certainly help you design better software, composed of classes and components with well-defined boundaries, clear responsabilities, and controlled dependencie. But it turns out that the devil is in the implementations

### Package By Layer

sdfasdf

### Package By Feature

assdaf

### Ports And Adapters

asfsadf

### Package By Component

fdgsdfgsd

