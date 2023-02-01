---
aliases:
tags:
- CPP/Lecture
- CPP/Polymorphism
- CPP/virtual
- CPP/FlowControl/rangefor
- CPP/Arrays
---
**[[C++|HOME [C++]]]**

---
## Polymorphism: Dynamic binding w/ virtual functions
>[!INFO|alt-co]+ Using arrays for collections
> ```cpp
> Base *base_collection[]{&base, &derived1, &derived2};
> 
> for(Base *s_ptr : base_collection) {
> 	s_ptr->functionName();
> }
> ```

**e.g.**
```cpp
#include <iostream>
using namespace std;

class Shape
{
protected:
    int width;
    int height;

public:
    Shape(int w, int h)
    {
        width = w;
        height = h;
    }

    virtual int area()
    {
        cout << "sha(" << width << ", " << height << ") - ";
        cout << "Parent class area: ";
        return (width * height);
    }
};

class Rectangle : public Shape
{
public:
    Rectangle(int w, int h) : Shape(w, h) {}

    int area()
    {
        cout << "rec(" << width << ", " << height << ") - ";
        cout << "Rectangle class area: ";
        return (width * height);
    }
};

class Triangle : public Shape
{
public:
    Triangle(int w, int h) : Shape(w, h) {}

    int area()
    {
        cout << "tri(" << width << ", " << height << ") - ";
        cout << "Triangle class area: ";
        return (width * height / 2);
    }
};

int main()
{
    Shape sha(10, 3);
    Rectangle rec(10, 7);
    Triangle tri(10, 5);

    Shape *shape;
    shape = &sha;
    cout << shape->area() << endl;

    shape = &rec;
    cout << shape->area() << endl;

    shape = &tri;
    cout << shape->area() << endl;

    return 0;
}
```