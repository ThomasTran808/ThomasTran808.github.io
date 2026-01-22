---
layout: project
type: project
image: img/shapes-square.png
title: "Geometric Shape Calculator"
date: 2025-01-20
published: true
labels:
  - C++
  - Object-Oriented Programming
  - Polymorphism
summary: "A C++ program demonstrating polymorphism and inheritance through geometric shape calculations for area, surface area, and volume."
---

<img class="img-fluid" src="../img/shapes-header.png">

This project is a C++ program that calculates geometric properties for seven different shapes including circles, spheres, cylinders, squares, cubes, triangles, and tetrahedrons. The program uses an abstract base class and derived classes to demonstrate object-oriented programming principles. Users interact with a menu system to select shapes, input dimensions, and receive calculated results for area, surface area, and volume.

I developed this project independently as part of my computer science coursework. I designed the class hierarchy, implemented all seven shape classes with their respective calculation methods, and created the menu-driven interface. I was responsible for implementing virtual functions, inheritance relationships, and ensuring accurate mathematical calculations for each shape type.

This project deepened my understanding of polymorphism and how virtual functions enable runtime behavior selection in C++. I learned how to design effective class hierarchies where 3D shapes inherit from their 2D counterparts, promoting code reuse. The experience also reinforced the importance of abstract classes in defining interfaces and the practical applications of the "is-a" relationship in object-oriented design.

## Code Sample
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
    
    double area() const {
      return MY_PI * radius * radius;
    }
   
  protected:    
    double radius;
};

// Additional classes: Sphere, Cylinder, Square, Cube, Triangle, Tetrahedron...
```

*Full source code available upon request.*
