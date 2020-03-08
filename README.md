# Modularization of legacy code

## What is modular programming?

According to Wikipedia, [modular programming](https://en.wikipedia.org/wiki/Modular_programming) is a programming technique aimed at dividing the IT system into independent, exchangeable modules so that each module contains all the necessary elements to perform a specific functionality.


## What does the module contain?
1. The module consists of two parts:
    - interface of the module;
    - implementation of the module;

2. The module interface defines what the module does.

3. The implementation of the module determines how the module interface is implemented.

4. The division of the module into the interface and implementation is very beneficial for both the system user (client) and the implementing person (module's provider).

## What is the legacy code?
Legacy code means an old code with the following properties:
1. It is about 20 years old with the spaghetti code structure.
2. It has no documentation or documentation is outdated and incomplete.
3. Employees involved in building this system either no longer work in the company or are involved in other projects
4. There is no full information about how the system works and what there were the original assumptions of the system.


## How to improve the quality of the code?

1. We say that the quality of the code is high when the new functionality in the system can be implemented quickly, cheaply and without inctroducing errors in the current functionality.

2. One (and maybe even the only) way to improve the quality of the legacy code is to divide the system into modules, i.e. execute code modularization.

## What is the result of modularization?

1. The effect of modularization is the division of the code into libraries that contain logically separate elements of the code.

2. The resulting libraries may depend on each other or be independent.

3. If libraries are treated as nodes in the graph, and the relationships between libraries are treated as edges in the graph, then the libraries after modularization form a directed dependency graph.

4. The library system is easier to extend and maintain when the dependency graph does not have cycles.

5. The cycle in the dependency graph is a sign of strong dependence between libraries. It is highly recommended to avoid cycles in dependency graph.


## What are the benefits of modularization?


1. The code after modularization is much easier to maintain, because the modularization process divided the code into smaller (usually independent) parts, which are easier to analyze.

2. After modularization it is easier to expand the code and implement new elements mainly due to the division of the code into libraries.

3. After modularization it is easier to re-code the feature, because the process of dividing the code into libraries provides valuable information about the dependencies in the code, which is a great help when making decisions about making changes in the code.

4. After modularization, the cost of implementing a new employee is reduced. Reducing the cost is due to reducing the time needed for a new employee to familiarize yourself with the system.

5. Modularization divides the system into parts, thereby allowing the system to be sold in parts.

6. Modularization allows to divide a group of programmers who maintain the entire system into teams dealing with dedicated libraries. The division of the group of programmers into teams is beneficial, because it allows to deepen the knowledge about the selected library and thus create competences directed to the given field.
    
7. Modularization allows the focusing of tests within the library, thus facilitating the maintenance of tests and decreasing the cost.

8. Modularization usually removes many unnecessary dependencies between files introduced due to excessive inclusion of files using the #include pre-processor directive. Removing these unnecessary dependencies leads to shortening the compilation time and building the system.


## What are the modularization's assumptions?

1. The basic assumption of modularization is that the system after modularization and before modularization has identical functionality and interfaces in classes are not changed. It is only after modularization that steps are taken to change the code or re-factoring the code. The division of the modernization (reconstruction) of the code into two stages (where the first stage is modularization) allows to avoid introducing errors to a greater extent.
    
2. It is preferable that the modularized code be integrated with the [Continuous Integration](https://en.wikipedia.org/wiki/Continuous_integration) system, which is used to build code and run tests.

3. Modularization does not block the simultaneous development of the system.

4. The modularization process is significantly impeded when global variables or singletons are used in the implementation, which introduce strict global dependencies between classes.


## How is modularization carried out? 

1. Modularization is carried out on the existing system, which means that the alternative version of the system is not built.

2. The first stage of modularization is to define the most basic classes that will create a library (module). After creating the module, this module is turned on and used in the system.

3. The next modularization steps involve selecting classes that only use modularized libraries and integrate them into the system. Thus, the system is transformed into a modularized systematic way.

## References

1. M. Fowler, *Refactoring: Improving the Design of Existing Code*, 2018 

1. A. Volkhover, *Become an Awesome Software Architect: Book 1: Foundation*, 2019

1. J. F. F. Dooley, *Software Development, Design and Coding: With Patterns, Debugging, Unit Testing, and Refactoring*, 2017

1. R. N. Taylor, N. Medvidovic, E. M. Dashofy, *Software Architecture: Foundations, Theory, and Practice*, 2009

1. R. C. Martin, *Clean Code: A Handbook of Agile Software Craftsmanship*, 2008

1. K. Henney, *97 Things Every Programmer Should Know: Collective Wisdom From The Experts*, 2010

1. R. S. Pressman, B. Maxim, *Software Engineering: A Practitioner's Approach*, 2014

1. J. Humble, D. Farley, *Continuous Delivery: Reliable Software Releases through Build, Test, and Deployment Automation*, 2010

1. P. Smith, *Software Build Systems: Principles and Experience*, 2011

1. I. Crnkovic, M. Larsson, *Building Reliable Component-Based Software Systems*, 2002

1. C. Szyperski, *Component Software: Beyond Object-Oriented Programming*, 2002

1. K.-K. Lau, *Component-Based Software Development: Case Studies*, 2004

1. M. Feathers, *Working Effectively with Legacy Code*, 2004
