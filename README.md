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
SOLID principle supports good object-oriented design and programming. Five of these principles are described as SOLID: 
<b>S</b>ingle responsibility<br/>
<b>O</b>pen-closed<br/> 
<b>L</b>iskov substitution<br/>
<b>I</b>nterface segregation<br/>
<b>D</b>ependency inversion<br/>
(Check out SOLID Principles Repository)

# Separation of Concerns
A key principle of software development and architecture is the notion of separation of Separation-of-Concerns-Feb-2013concerns.  At a low level, this principle is closely related to the Single Responsibility Principle of object oriented programming.  The general idea is that one should avoid co-locating different concerns within the design or code.

# Once and Only Once
The Once and Only Once principle can be thought of as a subset of the Don’t Repeat Yourself principle, and is one of the most fundamental principles of software development.  Once and Only Once basically states that any given behavior within an application is defined Once and Only Once.  Duplication of behavior is one of the most common sources of bugs in software systems, since it becomes increasingly likely that changes to behavior defined in one location may not be propagated to all locations where this behavior is defined.  Eliminating the duplication caused by not following the Once and Only Once principle is one of the primary reasons for refactoring and is also at the core of many design patterns.

# STUPID
<b>S</b>ingleton<br/>
<b>T</b>ight Coupling<br/>
<b>U</b>ntestability<br/>
<b>P</b>remature Optimization<br/>
<b>I</b>ndescriptive Naming<br/>
<b>D</b>uplication<br/>
<br/>

<b>Singleton</b>

The Singleton pattern is, in my opinion, one of the most well-known design pattern as  lots of OOP design books start with this pattern. I am sure with 99% probability that singleton is the first pattern you have learnt.

 The main problem with this pattern may be based on this fact.

After you have seen this pattern like the first item in patterns list, you think the Singleton pattern is the most appropriate pattern for every case you have. In other words, you use it everywhere. That is definitely not cool.

At the same time a lot of developers consider Singleton to be an anti-pattern. “Wow!”- you said now. But it’s true, cause singleton represents a global state and there are some problems with that:

Applications using global state are more difficult to test;

Applications that rely on global state hide their dependencies;

These difficulties were particularly described in Singleton – Singleton pattern: light or dark side of the Force.

But should you really avoid them all the time? May be not, but I would say you can often replace the use of singleton by something better. Avoiding static things is important to avoid something called tight coupling.

<b>Tight Coupling</b>

Basically, you should reduce coupling between your classes or application’s modules. Coupling is a degree to which each program module relies on each one of the other modules.

Whenever your code contains implementation like Singleton::getInstance(), you are tightly coupling your code to the Singleton class. This makes extending Singleton functionally impossible and makes your code hard to reuse. That’s bad since it doesn’t allow to make further changes such as replacing the instance by an instance of a sub-class, a mock or whatever. Inability to replace this code with mocks leads to untestability.

<b>Untestability</b>

Usually you can face tight coupling problems trying to create unit tests. Unit test is used to check small module of application like a method. To test each method in class separately you need to isolate class from other dependencies. Obviously, if we have tight coupled classes it’s harder to isolate them from each other. You probably can do it somehow, through enormous efforts or some dirty tricks. There are cases when developers usually don’t do this to save time and just leave their code untested and broken.

If your code is good you can test it in no time. Only with bad code unit testing becomes a nightmare.

<b>Premature Optimization</b>

Premature optimization is not bad if we talk about:

1) Architectural optimization – for instance, optimize separated components and layers to eliminate tight coupling and follow Dependency Inversion principle.

2) Data flow optimization – optimize or change some data structure, change ways of data processing, etc.

But micro premature optimization is reason of many problems. Doing this you add redundant complexity to your application. And the worst thing that can happen, when none of team-mates except of you is be able to understand this complexity since it corresponds to some future possible/impossible application cases. Moreover, this kind of optimization can hurt current productivity. So, take care about current problems and code readability and flexibility as if you are going to expand your current code for new features or changes. That won’t be hard to do it thanks to your good architecture.

<b>Indescriptive Naming</b><br/>

Indescriptive class/field/method naming is a bad code smell. When you write your application, please, don’t forget that another people may maintain your code in future. If  you fully understand the abbreviations in your methods, other people may not be on the same wavelength with you. Moreover, today you remember these unassociated names but what if you need to update your application in a few months or years? To my mind, you will be the first victim of absence naming strategy.

<b>Duplication</b>

Please, be faithful to DRY (Don’t repeat yourself) principle. You enhance complexity of alteration in application by making duplication in the code. It leads to situation when you need to spend a lot of time, alter different  classes (in the most cases they are not) to change some small piece of logic.

One of the reason of code duplication is tight coupling. If your code is tightly coupled, you just can’t reuse it. And here comes your duplication.

# GRASP 
GRASP (General Responsibility Assignment Software Patterns) is a design pattern in object-oriented software development used to assign responsibilities for different modules of code.

GRASP assigns seven types of roles to classes and objects in order to make for clear delineation of responsibilities. These roles are:

Controller<br/>
Information Expert<br/>
Creator<br/>
High Cohesion<br/>
Low Coupling<br/>
Polymorphism<br/>
Protected Classes<br/>

# Hollywood Principle
<b>“don’t call us, we’ll call you”.</b> At its most basic level, the principle is about reducing the coupling in a software system. It gets back to the well known phrase in software development: loose coupling and high cohesion. You can keep classes loosely coupled by ensuring that you don’t have unnecessary references and you are referencing classes and other subsystems properly.
