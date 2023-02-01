# [High cohesion, loose coupling](https://asleekgeek.com/high-cohesion-loose-coupling-1731b1f74bf6)

> The only thing that separates the good software from the bad one is the value of the software for the business at that particular point in time. In order to prolong the value of the software for a long period of time you have to make it respond easier to change

## Cohesion

We want to write module that are cohesive. The main thing to keep in mind is: module purpose.

- Is my new functionality part of this purpose?
- How many purposes this module has?
- Extracting this to another module would require repeating some existing code?
- How many public functions the module has?


## Low coupling

Writing less coupled code means that you will need less maintainence. To do so you don't want you implementation to depend on the internal of other components. Two main advices:

- Use Dependency Injection. Leave the role of instantiating modules to others and receive it ready to use.
- Rely on interfaces and never on the actual implementation. The less you know about other components, the better.
