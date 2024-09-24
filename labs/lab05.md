# Lab 5: Refactoring and Anti-Patterns

## Introduction 
A lot of the design principles and heuristics we have discussed in this class are there to encourage good design *up-front*. But you do not always have control over how a system you are using gets created. 


**Anti-patterns** are common examples of bad design. They tend to come about due to a program’s natural evolution, coupled with poor choices early on, which leads to code that is increasingly *tangled*, badly coupled, low on cohesion, etc. These are often signaled by **code smells** -- heuristic, but not guaranteed indicators of anti-patterns, like overly long methods, or a class that calls a lot of another class’ code (feature envy, signals high coupling).

In this lab, you will become a refactoring agent who detects anti-patterns and poor design decisions within the code, and attempts to fix them.
## Deliverables

- [ ] Identify one design problem with Frogger crossing the road (in Frogger.java and Road.java). Explain the design problem to the TA and show an improved implementation that fixes the design problem.
- [ ] Identify one design problem with Frogger recording themselves (in Frogger.java and Records.java). Explain the design problem to the TA and show an improved implementation that fixes the design problem.
- [ ] Identify at least two issues (no need to name the anti-pattern) associated with the Drawing System, and explain how you would refactor it to the TA. No coding required.

## Instructions

### Setup
<u>Fork</u> and clone the repo from [https://github.com/CMU-17-214/f24-lab05](https://github.com/CMU-17-214/f24-lab05).
The task is provided in Java. If you would like some additional exercise, feel free to look into the "accounts" folder and identify the anti-pattern associated with it.

In the appendix, we have provided a non-comprehensive list of anti-patterns. You might want to read and refer to when doing the tasks. 

### Task 1
Frogger is trying to cross the road, which she holds as a "Road" object in her fields. The Road object holds a boolean array indicating which steps are “occupied”; Frogger is on a specific square (“position”) and provides a move method (either forward or backward).

In the frogger folder, navigate to the Frogger.java and Road.java classes and take a look at the code. What is it doing and which anti-pattern is present? Try to fix the design by modifying the two classes.

> Hint: 
> + What information should Frogger hold? Does it do things that appear unusual for a Frogger?


### Task 2

Frogger crossed the road and remembered: she was here to *record* her identity status at the Frogger Office. This is held in the "Records" object in her field. Frogger tries to fill in the fields according to the Record object. But there are simply too many things to fill in.

Take a look at Records.java and then Frogger.java (again). What anti-pattern is present? Then try to fix the design by modifying the two classes. Alternatively, take a look at FroggerID.java. How might you use it?

### Task 3

Next, let's study the “drawing” system. Open the drawing folder--and start by reading Drawing.java. There seem to be several design problems involved: think through them. For each of the poor design decisions below, think about how you would refactor them (no need to write actual code), and explain two of these refactorings to your TA. (The entire folder contains more design problems than the ones we've described below. If you would some additional practice, feel free to explore!)

1. The "draw" function seems to duplicate itself. How would you refactor it so that we don't need to rewrite the functionality everytime we introduce a new file type?
2. Take a look at ``` Drawing.java ```. Somewhere inside the "draw" function, the code seems to be explicitly creating an array of Lines and feeding it to the shape. How would you refactor it so that we don't need to expose and rely on such information inside our Drawing class?


## Appendix

Below are a few anti-patterns/code smells, together with a brief explanation and possible refactoring actions. This list is not meant to be a comprehensive: it only includes several common examples. You don’t need to memorize this list. Instead, try to learn to recognize these patterns using the examples provided. You should also be able to discover new ones using the resources pointed to.

1. **Feature envy**: this antipattern happens when one class uses a lot of another’s functionality. This strongly indicates that some of the work being done in the former belongs in the latter (information expert).
  - Refactoring: move methods/fields, possibly part or some of them, to the information expert. This might work for inappropriate intimacy (below), but if both classes really need the same fields, create a delegate that can be used by both instead.
  - Related: **inappropriate intimacy**, where one class relies too much on the implementation details (fields, protected methods) of another.

2. **Large (“god”) class**: one class that has many responsibilities (poor cohesion).
  - Refactoring: extract classes to delegate to, sub-class if you need inheritance. It can also help to extract an interface, by identifying important components.
  - Related: **middle man**, where one class only exists to delegate work elsewhere. This smell applies to classes that don’t do any actual work, and can also show up in small classes.

3. **Message chains**: one method makes a series of calls on the return values of another. Think of the CardDeck → FlashCard.getStatus() → CardStatus.getSuccesses example.
  - Refactoring: create a delegate method in the intermediate class (e.g. ‘getSuccesses’ on ‘FlashCard’).

4. **Shotgun Surgery**: making any change requires changing a lot of code (bad responsibility assignment).

5. **Long method**: a method does too many things at once.
  - Refactoring: extract any cohesive parts to separate methods.

6. **Long parameter list**: a long list of parameters provided to a method.
  - Refactoring: identify an object that already holds all or most of these parameters, or create a “parameter Object” to pass instead. If this does not apply, identify if any parameters require a method call to compute on the caller’s side and move that method call into the method.

7. **Refused bequest**: two classes are connected through inheritance despite rather limited similarities (excessive coupling).
  - Refactoring: either restructure the hierarchy to a much simpler superclass object (if inheritance is really appropriate), or (more commonly) extract a delegate for the shared functionality.

8. **Excessive Instanceof**: a function uses multiple "instanceOf" calls to determine the type of the object it is interacting with. This is bad encapsulation and hard to extend.
  - Refactoring: restructure the code by invoking a more general class or interface that the subclasses may program against.
