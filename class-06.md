# How to use the Random Module in Python

## Randint
If we wanted a random integer, we can use the randint function Randint accepts two parameters: a lowest and a highest number. Generate integers between 1,5. The first value should be less than the second.
```
import random
print random.randint(0, 5)
```
This will output either 1, 2, 3, 4 or 5.

## Choice
Generate a random value from the sequence sequence.
```
random.choice( ['red', 'black', 'green'] ).
```
The choice function can often be used for choosing a random element from a list.
```
import random
myList = [2, 109, False, 10, "Lorem", 482, "Ipsum"]
random.choice(myList)
```

## Shuffle
The shuffle function, shuffles the elements in list in place, so they are in a random order.
```
from random import shuffle
x = [[i] for i in range(10)]
shuffle(x)
Output:
# print x  gives  [[9], [2], [7], [0], [4], [5], [3], [1], [8], [6]]
# of course your results will vary
```
## Randrange
Generate a randomly selected element from range(start, stop, step)

```random.randrange(start, stop[, step])
import random
for i in range(3):
 print random.randrange(0, 101, 5)
```


# Risk Analysis

The probability of any unwanted incident is defined as Risk. In Software Testing, risk analysis is the process of identifying the risks in applications or software that you built and prioritizing them to test. After that, the process of assigning the level of risk is done. The categorization of the risks takes place, hence, the impact of the risk is calculated.

## Why use Risk Analysis?
n any software, using risk analysis at the beginning of a project highlights the potential problem areas. After knowing about the risk areas, it helps the developers and managers to mitigate the risks. When a test plan has been created, risks involved in testing the product are to be taken into consideration along with the possibility of the damage they may cause to your software along with solutions.

## Risk Identification
There are different sets of risks included in the risk identification process. Those are as follows:

1. Business Risks: This risk is the most common risk associated with our topic. It is the risk that may come from your company or your customer, not from your project.

2. Testing Risks: You should be well acquainted with the platform you are working on, along with the software testing tools being used.

3. Premature Release Risk: a fair amount of knowledge to analyze the risk associated with releasing unsatisfactory or untested software is required

4. Software Risks: You should be well versed with the risks associated with the software development process.

5. After identifying the risks associated with your software, the next step is to assess the risks; i.e, Risk Assessment.

## Risk Assessment
In the risk analysis process, these steps prove to be the most important one. It is said that this step is way too complex and should be tackled with the utmost care. After risk identification, assessment has to be dealt programmatically. There are a few perspectives on risk assessment.

1. Early forecast of unwanted solutions in your project
2. Estimating potential loss of such situation
3. Making decition to deal with such situation
4. Avoid the future consequences

## The perspective of Risk Assessment

There are three perspectives of Risk Assessment:

- Effect

- Cause

- Likelihood

## How to perform Risk Analysis?

There are three steps:

1. Searching the risk

2. Analyzing the impact of each individual risk

3. Measures for the risk identified
