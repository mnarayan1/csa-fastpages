---
toc: true
layout: post
description: Important ideas and terms
categories: [markdown]
title: Notes
image: images/data_types.png
---
# Notes

## Primitives Lesson
![data types]({{site.baseurl}}/images/data_types.png)
- **Primitives**: Basic data types, don't store any information beyond the data itself (ie. int, char, float, double)
- **Wrapper Classes**: More complex, similar to objects. Can run methods on wrapper classes (ie. String)

## Objects
- Create **instance** of object:
```
Painter mypainter = new Painter();
Scanner myScanner = new Scanner(System.in);
```
- Call **methods** on object
```
myPainter.turnLeft();
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