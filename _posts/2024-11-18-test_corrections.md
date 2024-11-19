---
layout: post
title: 2018 MC Test Corrections
permalink: /test_corrections
comments: true
---

# AP CSP 2018 MCQ Corrections

## Question 1
![Question 1]({{ site.baseurl }}/images/question1.png)
- **Mistake**: 
  *C is incorrect. The code segment never changes the value of second.*

- **Correction**: 
  *B is correct. The code segment assigns the initial value of first to temp, then assigns the initial value of second to first. The initial value of first, which has been stored in temp, is then assigned to second. Therefore, the initial values of first and second have been interchanged.*

---

## Question 21
![Question 21]({{ site.baseurl }}/images/question21.png)
- **Mistake**: 
  *A is incorrect. This code segment moves the robot forward two squares, rotates it right one time so that the robot faces the bottom of the grid, and then moves the robot forward three squares.*

- **Correction**: 
  *B is correct. This code segment moves the robot forward two squares, rotates it right three times so that the robot faces the top of the grid, and then moves the robot forward three squares to the gray square.*

---

## Question 26
![Question 31]({{ site.baseurl }}/images/question26.png)
- **Mistake**: 
  *I chose C, which moves the robot forward regardless of its orientation, but this fails to consider the robot's ability to avoid obstacles or navigate properly.*

- **Correction**: 
  *The correct answer is A. This code rotates the robot right when it can move right and then moves forward, ensuring the robot follows a proper path without colliding with obstacles.*

---

## Question 31
![Question 31]({{ site.baseurl }}/images/question31.png)
- **Mistake**: 
  *I selected B, assuming Program II correctly navigates to the gray square but Program I does not. However, I failed to properly analyze the execution of Program I.*

- **Correction**: 
  *The correct answer is C. Both Program I and Program II successfully navigate the robot to the gray square. Program I uses a deterministic sequence of movements, while Program II evaluates conditions dynamically to adjust its movements.*

---


## Question 44
![Question 44]({{ site.baseurl }}/images/question44.png)
- **Mistake**: 
  *C is incorrect. The operation 10 plus 7 causes an overflow error, but 12 plus 3 does not produce a result large enough to cause an overflow error.*

- **Correction**: 
  *B is correct. With a 4-bit integer representation, 2 to the fourth power values can be represented, which allows for the values between 0 to 15, inclusive. If an operation results in a value greater than 15, an overflow error will occur. Of the operations given in the options, only 10 plus 7 gives a result larger than 15.*

---

## Question 46
![Question 46]({{ site.baseurl }}/images/question46.png)
- **Mistake**: 
  *A is incorrect. It is not possible to create an algorithm to solve an undecidable problem for all programs and inputs.*

- **Correction**: 
  *D is correct. An undecidable problem is one in which no algorithm can be constructed that always leads to a correct yes-or-no answer.*

---

## Question 55
![Question 55]({{ site.baseurl }}/images/question55.png)
- **Mistake**: 
  *A is incorrect. The procedure always returns false.*

- **Correction**: 
  *This option is correct. The expression response = y, AND, response = yes, always evaluates to false because it is not possible for the variable response to be equal to both y and yes. Therefore, the procedure will always return false.*


### Reflection on AP CSP 2018 MCQ

#### **What I Learned from the Quiz**
- I need to carefully analyze how code segments execute step by step.  
- Understanding conditions, logic, and program behavior is critical for correct answers.  
- Reviewing foundational concepts like overflow errors, undecidable problems, and Boolean logic helps prevent mistakes.  

---

#### **What Types of Questions I Feel Weak On**
- **Code Execution**: Missteps in following the logic of a program (e.g., robot navigation).  
- **Data Representation**: Misunderstanding limits like 4-bit integer overflow.  
- **Theoretical Concepts**: Difficulty grasping undecidable problems and algorithm limitations.  
