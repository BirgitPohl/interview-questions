# Clean Code Pinciples Questions


## 6 Figure Software Engineering Principles To Know

- SOLID - Single Responsibility, Open-Closed, Liskov, Substitution, Interface Segregation, Dependency Inversion
- KISS - Keep It Simple, Stupid
- DRY - Don’t Repeat Yourself
- YAGNI - You Aren’t Gonna Need It
- SOC - Separation of Concerns

-----

## What does open–closed principle mean? How does that relate to class design?
    Something is open for extension/change by consumers without having to change the source code or public interface.
    
    Functionality can be altered by the consumer by means of passing configurations and dependencies.
    
    Can be over engineering, could introduce unnecessary complexity.
    

## In what kind of software aiming to follow open–closed principle is especially valuable?
    Framework kind of software.
    
    Widely reused code, with larger consumer base.
    
    When breaking changes are expensive, the extra complexity introduced by making things configurable and dynamic is more likely to pay off.

## What does Single Responsibility Principle mean?
    There is only one thing a function or method does.
  
    There is only one reason for something to change.
    
    Maybe a change could have been avoided by allowing extendability, by config? Maybe too many things were hard coded?

## Do you have any non-mainstream views in programming practices?
    Your expectations