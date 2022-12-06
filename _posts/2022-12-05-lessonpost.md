---
toc: true
layout: post
comments: true
description: All Videos
categories: [markdown]
title: Unit 3 Sections 9 and 11
---

## 3.9 Video 1
### Essential Knowledge
- Algorithms can be written in different ways and still accomplish the same tasks
- Algorithms that appear similar can yield different side effects or results
- Some conditional statements can be written as equivalent Boolean expressions
- Some Boolean expressions can be written as equivalent conditional statements
- Different algorithms can be developed or used to solve the same problem

### Dice Game
Do these two algorithms give the same results?

```python
print("What did you roll on the dice?")
diceRoll = int(input())
if diceRoll >= 4:
    print("Nice roll!")
else:
    if diceRoll >= 2:
        print("Meh... You can do better")
    else:
        print("That was not a great roll!")
```

```python
print("What did you roll on the dice?")
diceRoll = int(input())
if diceRoll >= 4:
    print("Nice roll!")
if diceRoll >= 2:
    print("Meh... You can do better")
if diceRoll < 2:
    print("That was not a great roll!")
```

- In what instances do the algorithms yield different results for the same input?
- Why does this happen?

### Can we adjust the second algorithm to yield the same results?

```python
print("What did you roll on the dice?")
diceRoll = int(input())
if diceRoll >= 4:
    print("Nice roll!")
if diceRoll >= 2 and diceRoll < 4:
    print("Meh... You can do better")
if diceRoll < 2:
    print("That was not a great roll!")
```

**What can be taken away from this?**
- Small changes/mistakes can have a big impact on the result
- There is often more than one way to achieve the same result

### Conditional vs Boolean
- How could this conditional scenario be replaced with a boolean scenario?   

- IF (isHoliday)   
- {   
    - school⟵false   
- }   
- ELSE   
- {   
    - IF(isWeekday)   
    - {   
        - school⟵true   
    - }   
    - ELSE   
    - {   
        - school⟵false   
    - }   
- }   

**What needs to be true and what needs to be false in order for you to go to school?**
- First conditional: If isHoliday is true, you do not need to go to school
- Second conditional: If isWeekday is true, you do need to go to school. However, if it is false, school also becomes false

**Therefore, in pseudo code, this statement could be written as:**
- school⟵((NOT (isHoliday)) AND (isWeekday))
- Keep in mind that both of these statements yield the same results, and neither of them are incorrect

### More Comparing Algorithms
The algorithms below are to sum the odd numbers from 1 to 9 (1+3+5+7+9). Do they each work as intended?

1. 
- sum⟵1
- counter⟵3
- REPEAT 4 TIMES
    - sum⟵sum + counter
    - counter⟵counter + 2
- DISPLAY sum

2. 
- sum⟵0
- counter⟵9
- REPEAT UNTIL counter < 1
    - sum⟵sum + counter
    - counter⟵counter - 2
- DISPLAY sum

**Why is it important to understand that algorithms can be written in different ways and still accomplish the same tasks?**

## 3.9 Video 2
### Essential Knowledge 
- Algorithms can be created from an idea, 
  by combining existing algorithms, 
  or by modifying existing algorithms.

### Vocab
- Iteration: Repeating steps, or instructions over and over again. 
( this could be also often called a loop ) 
- Selection: is a decision or question. At some point in an algorithm there may need to be a question because the algorithm has reached a step where one or more options are available.

### Create an Algorithm

<a href="https://trentcardall.github.io/period4yeung/images/example1triangle.png">
    <img src="https://trentcardall.github.io/period4yeung/images/robotanswer.png">
</a>

- Create an algorithm to move the robot to the gray square for the grid of squares on the right.
- The robot is represented by a triangle, which is initially facing towards the top of the grid.
- The robot can move into a white or gray square but cannot move into a black region.

**Answer is hidden so you guys don't cheat**

- You might notice that certain parts would be repeated if you listed all the steps.
- To more easily represent the algorithm, without showing every step, we could use iteration.
- By using iteration, we can better see the flow of the algorithm.
- The algorithm below uses the procedure goalReached, which returns true if the robot is in gray square and returns false otherwise.
![photo]({{site.baseurl}}/images/flowchart robot.png)
- We can represent this algorithm using pseudocode    

    
- REPEAT UNTIL (goalReached)
- {
    - MOVE_FORWARD ()
    - ROTATE_RIGHT ()
    - MOVE_FORWARD ()
    - ROTATE_LEFT ()
- }

### Practice Question

Choose which algorithm that uses selection and/or iteration to determine the cost of one item in the store is correct

The display at the store says the following:

All Green Tag Items - 25% off
All Red Tag Items - 60% off

Suppose that the tax on all items is 10%

**Algorithm A:**

- DISPLAY ("What is the cost of the item?")
- cost←INPUT ()
- IF (greenTag)
- {
    - cost ← 0.75 * Cost 
- }
- IF (redTag)
- {
    - cost ← 0.40 * Cost 
- }
- cost ← 1.10 * cost

**Algorithm B:**

- DISPLAY (What is the cost of the item)
- cost←INPUT ()
- IF (greenTag)
- {
    - cost ← 0.75 * Cost 
- }
- IF (redTag)
- {
    - cost ← 1.10 * cost
- }
- cost ← 0.40 * Cost


## 3.9 Video 3

### Essential Knowledge 
- Knowledge of existing algorithms can help in constructing new ones. Some existing algorithms include:
Determining the maximum or minimum value of two or more numbers.
Computing the sum or average of two or more numbers.
Identifying if an integer is or is not evenly divisble by another integer.
Determining a robat's path through a maze.
- Using existing correct algorithms as building blocks for constructing another algorithm has benefits such as reducing development time, reduce testing, and simplifying the idectification of errors.

### Vocab 
..

How can we make this work??
![]({{site.baseurl}}/images/incorrectexample.png)
- Create a algorithm to move the robot to the grey square for the grid above
- The robot is represented by a triangle
- The robot can move into white and grey squares but cannot move into a black square
![]({{site.baseurl}}/images/algorithmforvideo3.png)

What is wrong with the grid and why wouldn't this algorithm work? What black squares would need to be added or removed to make this work?

## Hacks
1. **Write this Boolean statement in the form of a conditional (if/else) statement:**
stayInside⟵((isCold) OR (isRaining))

2. **Create an algorithm that uses selection and/or iteration that will represent one player's complete turn.**

During a turn, each player gets 4 attempts/chances to get the greatest number possible.

during each attempt, the player will use a random number generator to select a random number from 1 to 10.

After they have had 4 chances, their score is the greatest number they received from the random number generator, and their turn is over.

3. **How can we change this algorithm to make this grid work?**
![]({{site.baseurl}}/images/incorrectexample.png)
![]({{site.baseurl}}/images/algorithforvideo3lesson.png)

4. Something relating to Binary search (samarth)