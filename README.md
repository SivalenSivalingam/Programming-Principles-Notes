# Programming Principles

# KISS
The “keep it simple, stupid” principle applies to pretty much all of life, but it’s especially necessary in medium-to-large programming projects.

It starts way in the beginning when you’re defining the scope of what you want to create. Just because you’re passionate about game development doesn’t mean you can create the next World of Warcraft or Grand Theft Auto. When you think you’ve simplified enough, simplify it one level further — feature creep is inevitable, so start small. Even after coding has begun, keep it simple. Complex code takes longer to design and write, is more prone to bugs and errors, and is harder to modify later down the road. In the wise words of Antoine de Saint-Exupery, “Perfection is achieved, not when there is nothing more to add, but when there is nothing left to take away.”

# DRY
The “don’t repeat yourself” principle is crucial for clean and easy-to-modify code. When writing code, you want to avoid duplication of data and duplication of logic. If you notice the same chunk of code being written over and over again, you’re breaking this principle.

The opposite of DRY code is WET code: “write everything twice” (or “waste everyone’s time”). One of the best ways to diagnose WET code is to ask yourself: in order to alter the program’s behavior in some way, how many areas of code would you need to modify?

# YAGNI
The “you aren’t gonna need it” principle is the idea that you should never code for functionality that you may need in the future. Chances are, you won’t need it and it will be a waste of time — and not only that, but it will needlessly increase your code’s complexity.

You could view this as a specific application of the KISS principle and a response to those who take the DRY principle too seriously. Often inexperienced programmers try to write the most abstract and generic code possible to avoid WET code, but too much abstraction ends up in bloated impossible-to-maintain code.

The trick is to apply the DRY principle only when you need to. If you notice chunks of code being written over and over, then abstract them — but never when you think a piece of code will be written over and over. More times than not, it won’t be.

# SOLID
SOLID principle supports good object-oriented design and programming. Five of these principles are described as SOLID: Single responsibility, Open-closed, Liskov substitution, Interface segregation, and Dependency inversion. (Check out SOLID Principles Repository)

# Separation of Concerns
A key principle of software development and architecture is the notion of separation of Separation-of-Concerns-Feb-2013concerns.  At a low level, this principle is closely related to the Single Responsibility Principle of object oriented programming.  The general idea is that one should avoid co-locating different concerns within the design or code.

# Once and Only Once
The Once and Only Once principle can be thought of as a subset of the Don’t Repeat Yourself principle, and is one of the most fundamental principles of software development.  Once and Only Once basically states that any given behavior within an application is defined Once and Only Once.  Duplication of behavior is one of the most common sources of bugs in software systems, since it becomes increasingly likely that changes to behavior defined in one location may not be propagated to all locations where this behavior is defined.  Eliminating the duplication caused by not following the Once and Only Once principle is one of the primary reasons for refactoring and is also at the core of many design patterns.

# STUPID
Singleton<br/>
Tight Coupling<br/>
Untestability<br/>
Premature Optimization<br/>
Indescriptive Naming<br/>
Duplication<br/>
