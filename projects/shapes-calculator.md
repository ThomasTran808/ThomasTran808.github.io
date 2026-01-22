---
layout: project
type: project
image: img/shapes-square.png
title: "Geometric Shape Calculator"
date: 2024-12-09
published: true
labels:
  - C++
  - Object-Oriented Programming
  - Polymorphism
summary: "A C++ program demonstrating polymorphism and inheritance through geometric shape calculations for area, surface area, and volume."
---

<img class="img-fluid" src="../img/shapes-header.png">

The Geometric Shape Calculator is a C++ program that demonstrates object-oriented programming concepts including polymorphism, inheritance, and abstract classes. The program calculates area, surface area, and volume for seven different geometric shapes.

The program features an abstract Shape base class with concrete derived classes for Circle, Sphere, Cylinder, Square, Cube, Triangle, and Tetrahedron. Users can select a shape from a menu, input dimensions, and receive calculated results. The implementation uses virtual functions to achieve runtime polymorphism.

Built with C++ using inheritance hierarchies where 3D shapes derive from their 2D counterparts (Sphere from Circle, Cube from Square, Tetrahedron from Triangle), demonstrating code reuse and the "is-a" relationship in object-oriented design.

## Code
```cpp
#include <iostream>
#include <cmath>

#define NUM 7
#define MY_PI 3.14

using namespace std;

class Shape {
  public:
    virtual const char* name() const = 0;
    virtual void printDetails() const = 0;
    virtual void inputData() = 0;
    virtual double area() const = 0;
    virtual double volume() const {
      return 0.0;
    }     
};   

class Circle : public Shape {
  public:
    Circle (double radiusParam = 1) {
      radius = radiusParam;
    }
    
    const char* name() const {
      return "Circle";
    }
  
    void printDetails() const {
      cout << "The " << name() << "'s area = " << area() << endl;
    } 
    
    void inputData() {
      cout << "Enter the " << name() << "'s radius: ";
      cin >> radius;
    }
    
    double area() const {
      return MY_PI * radius * radius;
    }
   
  protected:    
    double radius;
};

// Additional classes...
```
*Full source code available upon request.*
