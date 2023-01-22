>[!recite|clean no-i] Basic sample `protected` and `private` class

```cpp
// base class
class baseClass {
  protected:
    int protected_member;  // protected member
  private:
    int private_member;  // private member
  public:
    int public_member;  // public member

    void set_private_member(int value) { private_member = value; }
    int get_private_member() { return private_member; }
};

// derived class using private inheritance
class derivedClass_private : private baseClass {
  public:
    // derived class can access the public and protected members
    // through the public and protected member functions of the base class
    void set_private_member(int value) { baseClass::set_private_member(value); }
    int get_private_member() { return baseClass::get_private_member(); }
};

// derived class using protected inheritance
class derivedClass_protected : protected baseClass {
  public:
    // derived class can directly access the protected members
    // of the base class
    void set_protected_member(int value) { protected_member = value; }
    int get_protected_member() { return protected_member; }
};

int main() {
    derivedClass_private dp;
    // dp.public_member = 0;  // this will cause a compile error
    // dp.private_member = 0;  // this will cause a compile error
    dp.set_private_member(5);
    // dp.get_private_member();  // return 5
    
    derivedClass_protected dt;
    // dt.public_member = 0;  // this will cause a compile error
    // dt.private_member = 0;  // this will cause a compile error
    dt.set_protected_member(10);
    // dt.get_protected_member();  // return 10
    return 0;
}
```