---
aliases:
tags:
- CPP/Lecture
- CPP/Class/Inheritance
- CPP/Polymorphism
- CPP/virtual/destructors
---
**[[C++|HOME [C++]]]**

---
## Inheritance and polymorphism at different levels
**e.g.**
```cpp
#include <iostream>
#include <string>
#include <string_view>

class Base {
public:
    Base() = default;
    Base(std::string_view description)
        : m_description(description) {}

    virtual ~Base() {}

    virtual void breathe() const {
        std::cout << "Base::breathe called for : " << m_description << std::endl;
    }

protected:
    std::string m_description;
};

class Bird : public Base {
public:
    Bird() = default;
    Bird(std::string_view wing_color, std::string_view description)
        : Base(description), m_wing_color(wing_color) {}

    virtual ~Bird() {}

    virtual void fly() const {
        std::cout << "Bird::fly() called for bird : " << m_description << std::endl;
    }

private:
    std::string m_wing_color;
};

class Pigeon : public Bird {
public:
    Pigeon() = default;
    Pigeon(std::string_view wing_color, std::string_view description)
        : Bird(wing_color, description) {}
    virtual ~Pigeon() {}

    virtual void coo() const {
        std::cout << "Pigeon::coo called for pigeon : " << m_description << std::endl;
    }

    virtual void breathe() const {
        std::cout << "Pigeon::breathe called for : " << m_description << std::endl;
    }

    virtual void fly() const override {
        std::cout << "Pigeon::fly() called for bird : " << m_description << std::endl;
    }
};

class Crow : public Bird {
public:
    Crow() = default;
    Crow(std::string_view wing_color, std::string_view description)
        : Bird(wing_color, description) {}
    virtual ~Crow() {}

    virtual void cow() const {
        std::cout << "Crow::cow called fro crow : " << m_description << std::endl;
    }

    virtual void breathe() const {
        std::cout << "Crow::breathe called for : " << m_description << std::endl;
    }

    virtual void fly() const override {
        std::cout << "Crow::fly() called for bird : " << m_description << std::endl;
    }
};

class Feline : public Base {
public:
    Feline() = default;
    Feline(std::string_view fur_style, std::string_view description)
        : Base(description), m_fur_style(fur_style) {}
    virtual ~Feline() {}

    virtual void run() const {
        std::cout << "Feline " << m_description << " is running" << std::endl;
    }
    std::string m_fur_style;
};

class Cat : public Feline {
public:
    Cat() = default;
    Cat(std::string_view fur_style, std::string_view description)
        : Feline(fur_style, description) {}
    virtual ~Cat() {}

    virtual void miaw() const {
        std::cout << "Cat::miaw() called for cat " << m_description << std::endl;
    }

    virtual void breathe() const {
        std::cout << "Cat::breathe called for : " << m_description << std::endl;
    }

    virtual void run() const override {
        std::cout << "Cat " << m_description << " is running" << std::endl;
    }
};

class Dog : public Feline {
public:
    Dog() = default;
    Dog(std::string_view fur_style, std::string_view description)
        : Feline(fur_style, description) {}
    virtual ~Dog() {}

    virtual void bark() const {
        std::cout << "Dog::bark called : Woof!" << std::endl;
    }

    virtual void breathe() const override {
        std::cout << "Dog::breathe called for : " << m_description << std::endl;
    }

    virtual void run() const override {
        std::cout << "Dog " << m_description << " is running" << std::endl;
    }
};

int main() {
    // Base polymorphism
    Dog d1("dark grey", "d1");
    Cat ca1("black stripes", "ca1");
    Pigeon p1("white", "p1");
    Crow cr1("black", "cr1");

    Base *base[]{&d1, &ca1, &p1, &cr1};
    for (const auto &i : base) i->breathe();

    std::cout << "-------------------------" << std::endl;

    // Feline polymorphism
    Dog d2("dark grey", "d2");
    Cat ca2("black stripes", "ca2");
    // Putting pigeon in feline will result in compiler error
    // Pigeon p2("white", "p2");

    Feline *feline[]{&d2, &ca2};
    for (const auto &i : feline) i->run();

    std::cout << "-------------------------" << std::endl;

    // Bird polymorphism
    Pigeon p3("white", "p3");
    Crow c3("black", "c3");

    Bird *bird[]{&p3, &c3};
    for (const auto &i : bird) i->fly();

    return 0;
}
```