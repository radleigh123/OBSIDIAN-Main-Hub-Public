---
aliases:
tags:
- CPP/Class/Inheritance
- CPP/Polymorphism
- CPP/Pointers/unique_ptr
- CPP/Pointers/shared_ptr
- CPP/virtual/pure
- CPP/virtual/destructors
- CPP/Expressions/OperatorOverloading/operator<<
---
**[[C++polymorphismabstractinterfaces|BACK]]**

---
## Complex sample 1
**stream_insertable.h**
```cpp
#ifndef STREAM_INSERTABLE_H
#define STREAM_INSERTABLE_H
#include <iostream>

class StreamInsertable {
    friend std::ostream &operator<<(std::ostream &out, const StreamInsertable &operand) {
        operand.stream_insert(out);
        return out;
    }

public:
    virtual void stream_insert(std::ostream &out) const = 0;
};

#endif // STREAM_INSERTABLE_H
```

**main.cpp**
```cpp
#include <iostream>
#include <memory>
#include <string>
#include <string_view>
#include "stream_insertable.h"

class Point : public StreamInsertable {
public:
    Point() = default;
    Point(double x, double y)
        : m_x(x), m_y(y) {}

    virtual void stream_insert(std::ostream &out) const override {
        out << "Point [x: " << m_x << ",y: " << m_y << "]";
    }

private:
    double m_x;
    double m_y;
};

class Animal : public StreamInsertable {
public:
    Animal() = default;
    Animal(const std::string &description)
        : m_description(description) {}

    virtual ~Animal() {}

    virtual void breathe() const {
        std::cout << "Animal::breathe called for : " << m_description << std::endl;
    }

    // Stream insertable interface
    virtual void stream_insert(std::ostream &out) const override {
        out << "Animal [description : " << m_description << "]";
    }

protected:
    std::string m_description;
};

class Feline : public Animal {
public:
    Feline() = default;
    Feline(const std::string &fur_style, const std::string &description)
        : Animal(description), m_fur_style(fur_style) {}

    virtual ~Feline() {}

    virtual void run() const {
        std::cout << "Feline " << m_description << " is running" << std::endl;
    }

    // Stream insertable interface
    virtual void stream_insert(std::ostream &out) const override {
        out << "Feline [description : " << m_description << ", fur_style : " << m_fur_style << "]";
    }
    std::string m_fur_style;
};

class Cat : public Feline {
public:
    Cat() = default;
    Cat(const std::string &fur_style, const std::string &description)
        : Feline(fur_style, description) {}

    virtual ~Cat() {}

    virtual void miaw() const {
        std::cout << "Cat::miaw() called for cat " << m_description << std::endl;
    }

    virtual void stream_insert(std::ostream &out) const override {
        out << "Cat [description : " << m_description << ", fur_style : " << m_fur_style << "]";
    }
};

class Dog : public Feline {
public:
    Dog() = default;
    Dog(const std::string &fur_style, const std::string &description)
        : Feline(fur_style, description) {}

    virtual ~Dog() {}

    virtual void bark() const {
        std::cout << "Dog::bark called : Woof!" << std::endl;
    }

    virtual void stream_insert(std::ostream &out) const override {
        out << "Dog [description : " << m_description << ", fur_style : " << m_fur_style << "]";
    }
};

class Bird : public Animal {
public:
    Bird() = default;
    Bird(const std::string &wing_color, const std::string &description)
        : Animal(description), m_wing_color(wing_color) {}

    virtual ~Bird() {}

    virtual void fly() const {
        std::cout << "Bird::fly() called for bird : " << m_description << std::endl;
    }

    virtual void stream_insert(std::ostream &out) const override {
        out << "Bird [description : " << m_description << ", wing_color : " << m_wing_color << "]";
    }

protected:
    std::string m_wing_color;
};

class Pigeon : public Bird {
public:
    Pigeon() = default;
    Pigeon(const std::string &wing_color, const std::string &description)
        : Bird(wing_color, description) {}

    virtual ~Pigeon() {}

    virtual void coo() const {
        std::cout << "Pigeon::coo called for pigeon : " << m_description << std::endl;
    }

    virtual void stream_insert(std::ostream &out) const override {
        out << "Pigeon [description : " << m_description << ", wing_color : " << m_wing_color << "]";
    }
};

class Crow : public Bird {
public:
    Crow() = default;
    Crow(const std::string &wing_color, const std::string &description)
        : Bird(wing_color, description) {}

    virtual ~Crow() {}

    virtual void cow() const {
        std::cout << "Crow::cow called fro crow : " << m_description << std::endl;
    }

    virtual void stream_insert(std::ostream &out) const override {
        out << "Crow [description : " << m_description << ", wing_color : " << m_wing_color << "]";
    }
};

int main() {
    Point f1(10, 20);
    std::cout << "f1: " << f1 << std::endl; // what the compiler does: operator<<(std::cout, f1);

    std::cout << "--------------------" << std::endl;

    std::unique_ptr<Animal> animal0 = std::make_unique<Dog>("stripes", "dog1");
    std::cout << *animal0 << std::endl;

    std::unique_ptr<Animal> animal1 = std::make_unique<Bird>("white", "bird1");
    std::cout << *animal1 << std::endl;

    std::cout << "--------------------" << std::endl;

    // Can even put animals in an array and print them polymorphically
    std::shared_ptr<Animal> animals[]{
        std::make_shared<Dog>("Stripes", "dog2"),
        std::make_shared<Cat>("Black stripes", "cat2"),
        std::make_shared<Crow>("Black wings", "crow2"),
        std::make_shared<Pigeon>("White wings", "pigeon2")};

    std::cout << "Printing out animals array" << std::endl;
    for (const auto &a : animals) { std::cout << *a << std::endl; }

    return 0;
}
```