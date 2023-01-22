>[!recite|clean no-i] Using [[C++classconstructorssetters&getters|getters & setters]]
```cpp
#include <iostream>
#include <string_view>

class myClass {
public:
    myClass() = default;
    myClass(std::string_view name_param, std::string_view sex_param, int age_param);
    ~myClass(); // defining destructor

    void print_info()
    {
        std::cout << "Name(" << this << "): " << name
                  << " Sex: " << sex
                  << " Age: " << *ptr_age << std::endl;
    }

    // Setters
    void setName(std::string_view name) { this->name = name; }
    void setSex(std::string_view sex) { this->sex = sex; }
    void setAge(int age) { *(this)->ptr_age = age; }

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
    func1.setName("Mufasa");
    func1.setSex("Trans");
    func1.setAge(88);
    func1.print_info();

    std::cout << "Done" << std::endl; // destructor called
    return 0;
}
```