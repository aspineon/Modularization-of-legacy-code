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

