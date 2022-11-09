---
toc: true
layout: post
description: Important ideas and terms
categories: [markdown]
title: Notes
image: images/data_types.png
---
# Notes

# Unit 1 - Primitive Types
![data types]({{site.baseurl}}/images/data_types.png)
- **Primitives**: Basic data types, don't store any information beyond the data itself (ie. int, char, float, double)
- **Wrapper Classes**: More complex, similar to objects. Can run methods on wrapper classes (ie. String)

# Unit 2 - Using Objects
- Create **instance** of object:
```
Painter mypainter = new Painter();
Scanner myScanner = new Scanner(System.in);
```
- Call **methods** on object
```
myPainter.turnLeft();
```

# Unit 3 - Boolean Expressions and Control Structures
- **Boolean**: a primitive data type that is either true or false
```
boolean computersAreCool = true;
boolean paperIsCool = false;
```

- **Boolean Expression**: an expression that evaluates as either true or false
```
1==1                    // is true, because 1 will always be equal to 1
a < 1                   // will sometimes be true, because not all values of a will be less than 1
“paper” == “good”       // is false, because the string “paper” is not equal to the string “good”
```

We can use boolean expressions in control structures to run programs when certain conditions are met. 

- **if** statements will run a code block if a particular condition is true. 

Structure: 
```
if(condition) {
    // code will run when condition is true
}
```

A single `if` statement only takes one condition, but what if we wanted to specify more conditions? We can add ``else if`` and ``else`` statements to accomplish this. 

Structure:
```
if(condition) {
    // code to execute when condition is met
} else if (condition 2) {
    // code to execute when condition is false but condition 2 is true
} else {
    // code to execute when condition and condition 2 are false
}
```

- **Switch statements** can be used in control flow 
```
switch (selection) {
    case 0:  
        System.out.print("Goodbye, World!");
        quit = true;
        break;
    case 1:
        System.out.print("Hello, World!");
        break;
    default:
        System.out.print("Error!");
        break;
}
```

- **DeMorgan's Laws** show how to deal with the negation of a conditional statements. When ``!`` is applied: 
- ``true`` will become ``false``
- ``false`` will become ``true``
- && will become \|\|

# Unit 4: Iteration
- **While Loops:** Repeat code while boolean expression evaluates to true
```
while (condition) {
    // code to run
}
```
- While loops are useful to iterate over arrays

```
int[] array = {1, 2, 3, 4}
int total = 0;
int i = 9;

while(i < array.length) {
    total += array[i];
    i++;
}

System.out.println(total);
```

- Infinite while loops run over and over again, since the condition is always true; useful for user input

```
while(true) {
    System.out.println("Choose an option");
}
```

**For Loops**

Three Parts of a For Loop
- Initialize Variable
- Test Condition
- Change of variable

```
for(int x = 1; x<=5; x++) {
    System.out.println(x);
}
```

**For Each Loops**
- Iterates through elements of arrays and collections (ArrayList)

```
for(dataType item : array) {
    // code here
}
```

# Unit 5: Writing Classes

- **Constructor**: Can set initial values of an object

```
public class Number {
  int x;

  public Number() {
    x = 5;  //initializing value of x in constructor
  }
}
```

-**Inheritance**: An object can inherit the characteristics of a parent object (ie. methods)

```
public class PainterPlus extends Painter { //must extend parent class
    public PainterPlus() {
        super(); //must call this in constructor
    }
}
```

**Data Encapsulation**

- Can restruct access to read-only or write-only through accessor/mutator methods

**5.4 Accessor Methods (getters)**
- Non-void, includes a return type
- ``toString`` will return a string from an object's properties

```
public String toString() {
    return "Type: " +  type;
}
```

**5.5 Mutator Method (Setter)**

- Usually a void avriable that changes static variables

**Static Variables and Methods**
- Static variables and methods belong to a class and are called with a ClassName rather than the object name

**this keyword**
- refers to the instance variables in a class

# Unit 6: Array

**6.1 Array Creation and Access**
- Arrays are used to store one data type
- Unlike Arraylists, arrays have a fixed size and cannot be changed
- Arrays can be denoted using braces {}
- To use an array you have to use the command import java.util.Arrays;

**6.3 Enhanced for loop for Arrays**

```
for(dataType i: arrayName) {
    do something with i
}
```