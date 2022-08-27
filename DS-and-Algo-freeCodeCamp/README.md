# Data Structures and Algorithms (FreeCodeCamp)

## What is a Data Structure? 
- A way of organizing data for effective usage.
- Ensures effective access,query and updation.

## Why use them? 
- To create fast and efficent algorithms. 
- Manage ad organize data.
- Ensure readability of code.

## Abstract Data Types (ADT) vs. Data Structures
- An ADT is an abstraction of a DS which provides only the interface to which a DS must adhere.
- The interface does not give any specific details about how something should be implemented or the programming language.
- Example: mode of transportation could be an ADT and car, motorbike, bicycle could be the DS. 

|Abstract Data Type            | Data Structure           |
|:---------------|:---------------|
|List| Dynamic Array, Linked List|
|Queue | Linked List-based, Array-based, Stack-based|
|Map| Tree Map, Hash Map / Hash Table|

## Computational Complexity Analysis
While writing software, we often need to answer these two important questions -
- How much **time** does an algorithm need to finish? 
- How much **space** does an algorithm need to finish?

### The Big-O Notation
Big-O notation gives an upper bound of the complexity in the **worst** case, helping to quantify performances as the input size becomes **arbitraily large**.

If 'n' is the size of our input then :

|Name|Notation|
|:---------------|:---------------|
|Constant Time| O(1)|
|Logarithmic Time| O(log(n))|
|Linear Time| O(n)|
|Linearithmic Time| O(nlog(n))|
|Quadric Time| O(n^2)|
|Cubic Time| O(n^3)|
|Exponential Time| O(b^n), b>1|
|Factorial Time| O(n!)|

### Properties of Big-O
1. O(n+c) = O(n)
2. O(cn) = O(n), c>0

Example : Let *f* be a function 

## Static and Dynamic Arrays
- Fundamental building block of any DS. 

## Queue