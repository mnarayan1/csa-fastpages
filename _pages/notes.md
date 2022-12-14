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

# Unit 7: ArrayList
**Introduction**
- Mutable and contains object references

**Methods**
- ArrayList.add(int index, element)
- ArrayList.addAll(int index, Collection collection)
- ArrayList.size()
- ArrayList.clear()

**ArrayList Loops**
- For loop

```
int sum = 0;
for (int i = 0; i < roster.size(); i++) {
    sum = sum + roster.get(i).length();
}
System.out.println(sum);
```

- While loop

```
int sum = 0;
int i = 0;
while (i < roster.size() ) {
    sum = sum + roster.get(i).length();
    i ++
}
System.out.println(sum);
```

- Enhanced for loop

```
int sum = 0;
for(String name: roster) {
    sum = sum + name.length();
}
System.out.println(sum);
```

**Searching**
- The locating of data within linear structures
- Involves control structures

**Sorting**
- Sorts the ArrayList in a specified order

```
Collections.sort(list name); // ascending order
Collections.sort(ArrayList, Collections.reverseOrder()); // descending order
```

# Unit 8: 2D Arrays

**Creating a 2D Array**

```
int[][] numbers = // initialize array here;
```

**Iteration**
- Use a for loop. First iterate through the rows, then iterate over the columns

```
for(int i = 0; i< array.length; i++) {
    for(int j = 0; j < array[i].length; j++) {
        // code here
    }
}
```

- Printing backwards: 

```
for(int i = array.length-1; i>=0; i--) {
    for(int j = array[i].length-1; j>= 0; j--) {
        // code here
    }
}
```

# Unit 9: Inheritance

- A superclass can be extended by subclasses, to reduce risk of error, redundacy, and increases simplicity

```
public class Car {
    // code here
}

public class Lambo extends Car {
    // code here
}
```

- Writing constructors for subclasses: the keyword "super" is used to call the superclass constructor, but you can also add additional attributes

```
public class Lambo extends Car {
    public Lambo(String license, int price) {
        super(wheels, color);
    }
}
```

- @Override is used to give different impelementations to the superclass method
    - Override a method of the superclass
    - Make your code readable to others

# unit 10: Recursion

- A recursive method calls itself

```
public static void example(int n) {
    if (n>0) {
        example(n-1);
    }
}
```

- Recursion can also be seen with String objects, such as iterating over substrings

```
public static void mystery (String s) {
    if(s.length() > 1) {
        mystery(s.substring(2));
        System.out.println(s.substring(0,1));
    }
}
```

- Binary Search: more efficient than linear search

1) find middle number of each half of list
2) We choose each half of the list based on if it is greater or less than target value

- Merge Sort: divides array into halves, the calls itself for the two halves to sort them

```
mergeSort(myArray, low, high) {
    if(low < high) {
        middle = (low+high) /2;
        mergeSort(myArray, low, middle);
        mergeSort(myArray, middle+1, high);
        merge(myArray, low, middle high);
    }
}
```

- Can use a recursion tree to display recursive algorithm