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
- Create instance of object:
```
Painter mypainter = new Painter();
Scanner myScanner = new Scanner(System.in);
```
- Call methods on object
```
myPainter.turnLeft();
```
- Switch statements can be used in control flow 
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
