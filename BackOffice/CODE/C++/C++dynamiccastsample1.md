---
aliases:
tags:
- CPP/Polymorphism
- CPP/Class/Inheritance
- CPP/Conversion/dynamic_cast
- CPP/Pointers
- CPP/References
---
**[[C++dynamiccast|BACK]]**

---
## Simple example with pointers/references
```cpp
#include <iostream>
#include <string>
#include <string_view>

class Base {
public:
	Base() = default;
	Base(std::string_view description)
		: m_description(description) {}

	virtual ~Base() { std::cout << "Base destructor called" << std::endl; }

	virtual void breathe() const {
		std::cout << "Base::breathe called for : " << m_description << std::endl;
	}

protected:
	std::string m_description;
};

class Derived1 : public Base {
public:
	Derived1() = default;
	Derived1(std::string_view fur_style, std::string_view description)
		: Base(description), m_fur_style(fur_style) {}

	virtual ~Derived1() { std::cout << "Derived1 destructor called" << std::endl; }

	virtual void run() const {
		std::cout << "Derived1 " << m_description << " is running" << std::endl;
	}
	void do_some_derived1_thingy() {
		std::cout << "Doing some derived1 thingy..." << std::endl;
	}
	std::string m_fur_style;
};

class Derived2 : public Derived1 {
public:
	Derived2() = default;
	Derived2(std::string_view fur_style, std::string_view description)
		: Derived1(fur_style, description) {}

	virtual ~Derived2() { std::cout << "Derived2 destructor called" << std::endl; }

	virtual void bark() const {
		std::cout << "Derived2::bark called : Woof!" << std::endl;
	}

	void do_some_derived2_thingy() {
		std::cout << "Doing some derived2 thingy...,speed : " << m_speed << std::endl;
	}

private:
	double m_speed{};
};

// --------------------------------------------------------------

void do_something_with_base_ptr(Base *base)
{
	std::cout << "In function taking base pointer..." << std::endl;
	Derived1 *derived1_ptr = dynamic_cast<Derived1 *>(base);

	if (derived1_ptr)
	{
		derived1_ptr->do_some_derived1_thingy();
	}
	else
	{
		std::cout << "Couldn't cast to Derived1 pointer,Sorry." << std::endl;
	}
}

void do_something_with_base_ref(Base &base) {
	std::cout << "In function taking base reference..." << std::endl;
	Derived1 *derived1_ptr_1{dynamic_cast<Derived1 *>(&base)};
	if (derived1_ptr_1) {
		derived1_ptr_1->do_some_derived1_thingy();
	} else {
		std::cout << "Couldn't cast to Derived1 reference,Sorry." << std::endl;
	}
}

// --------------------------------------------------------------

int main() {
	// Base class pointer
	Base *base_ptr = new Derived1("stripes", "derived1");
	// base_ptr->do_some_derived1_thingy(); ERROR! Has no member named do_some_derived1_thingy

	// check before calling stuff on the returned pointer
	Derived1 *derived1_ptr = dynamic_cast<Derived1 *>(base_ptr);
	if (derived1_ptr) {
		derived1_ptr->do_some_derived1_thingy();
	} else {
		std::cout << "Can't convert" << std::endl;
	}

	std::cout << "-------------------" << std::endl;

	// Transformation downstream for references

	// Base class references
	Derived1 derived12("stripes", "derived12");
	Base &base_ref = derived12;
	// base_ref.do_some_derived1_thingy(); ERROR! calling non-virtual method

	/*
	Derived2 &derived_ref = dynamic_cast<Derived2 &>(base_ref);
	derived_ref.do_some_derived1_thingy();
	*/

	// Doing proper checks w/ references
	Derived2 *derived1_ptr1 = dynamic_cast<Derived2 *>(&base_ref);
	if (derived1_ptr1) {
		derived1_ptr1->do_some_derived2_thingy();
	} else {
		std::cout << "Couldn't cast to Derived2" << std::endl;
	}

	std::cout << "-------------------" << std::endl;

	do_something_with_base_ptr(base_ptr);
	do_something_with_base_ref(base_ref);

	delete base_ptr;
	return 0;
}
```