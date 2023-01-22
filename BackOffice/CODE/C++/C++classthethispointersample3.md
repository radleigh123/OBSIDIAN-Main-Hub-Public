>[!recite|clean no-i] Chained calls using [[C++pointers|pointers]]
```cpp
#include <iostream>
#include <string_view>

class myClass {
public:
    myClass() = default;
    myClass(std::string_view name_param, std::string_view sex_param, int age_param);
    ~myClass(); // defining destructor

    void print_info() {
        std::cout << "Name(" << this << "): " << name
                  << " Sex: " << sex
                  << " Age: " << *ptr_age << std::endl;
    }

    /*
    // Using references
    myClass &setName(std::string_view name) {
        this->name = name;
        return *this; // dereference and return
    }
    myClass &setSex(std::string_view sex) {
        this->sex = sex;
        return *this;
    }
    myClass &setAge(int age) {
        *(this)->ptr_age = age;
        return *this;
    }
    */

    // Using pointers
    myClass *setName(std::string_view name) {
        this->name = name;
        return this;
    }
    myClass *setSex(std::string_view sex) {
        this->sex = sex;
        return this;
    }
    myClass *setAge(int age) {
        *(this)->ptr_age = age;
        return this;
    }

private:
    std::string name, sex;
    int *ptr_age{nullptr};
};

myClass::myClass(std::string_view name_param, std::string_view sex_param, int age_param) {
    name = name_param;
    sex = sex_param;
    ptr_age = new int;
    *ptr_age = age_param;

    std::cout << "myClass constructor called value: " << name << " at " << this << std::endl;
}

myClass::~myClass() {
    delete ptr_age;
    std::cout << "myClass destructor called value: " << name << " at " << this << std::endl;
}

int main(int argc, char **argv) {
    myClass func1("Fluffy", "Gay", 22); // constructor called

    func1.print_info();

    // for reference
    // func1.setName("Rhiz").setSex("Female").setAge(20);
    func1.setName("Rhiz")->setSex("Female")->setAge(20);

    func1.print_info();

    std::cout << "Done" << std::endl; // destructor called
    return 0;
}
```