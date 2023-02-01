**Refactor the code** If possible, refactor the code to remove the need for accessing the private data members. This may involve redesigning the class hierarchy, or moving functionality to a different class.
```cpp
class baseClass {
public:
    int private_member;
    int public_member;
};

class derivedClass : public baseClass {
    void doSomething() {
        public_member = private_member + 1;
    }
};
```
<br>

**Use the getter and setter methods** Instead of directly accessing the private data members, use public "getter" and "setter" methods to read and write the data. This is also known as the "property pattern" and it allows to read and write the private member variable, by providing public methods to access them.
```cpp
class baseClass {
private:
    int private_member{150};

public:
    int public_member;
    
    int get_private_member() const { return private_member; }
    void set_private_member(int value) { private_member = value; }
};

class derivedClass : public baseClass {
public:
    void doSomething() { public_member = get_private_member() + 1; }
};
```