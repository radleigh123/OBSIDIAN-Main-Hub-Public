>[!recite|clean no-i] Class base access specifier across multiple files

**main.cpp**
```cpp
#include <iostream>
#include "person.h"
#include "player.h"

int main(int argc, char **argv) {
    Person p1("Keane Radleigh", 21, "Deca Homes");
    std::cout << "p1\n"
              << p1 << std::endl;

    std::cout << "---------------------" << std::endl;

    Player p2;
    p2.m_fullName = "Mariah Paulynn";
    
    // will only print name, since constructor didn't match
    std::cout << "p2\n" << p2 << std::endl;

    return 0;
}
```

>[!column|no-i ttl-c] **Base class**
>>[!INFO|clean no-t]
>> **person.h**
>> ```cpp
>> #ifndef PERSON_H
>> #define PERSON_H
>> 
>> #include <string>
>> #include <string_view>
>> 
>> class Person
>> {
>>     friend std::ostream &operator<<(std::ostream &out, const Person &person);
>> 
>> public:
>>     Person() = default;
>>     Person(const std::string_view fullName, int age, const std::string address);
>>     ~Person();
>> 
>>     // Getters
>>     std::string get_fullName() const { return m_fullName; }
>>     int get_age() const { return m_age; }
>>     std::string get_address() const { return m_address; }
>> 
>> public:
>>     std::string m_fullName{"None"};
>> 
>> protected:
>>     int m_age{0};
>> 
>> private:
>>     std::string m_address{"None"};
>> };
>> 
>> #endif // PERSON_H>> 
>> ```
>
>>[!INFO|clean no-t]
>> **person.cpp**
>> ```cpp
>> #include <iostream>
>> #include <string_view>
>> #include "person.h"
>> 
>> Person::Person(const std::string_view fullName, int age, const std::string address) : m_fullName{fullName}, m_age{age}, m_address{address} {}
>> 
>> std::ostream &operator<<(std::ostream &out, const Person &person)
>> {
>>     out << "Person [Full name: " << person.get_fullName()
>>         << ", Age: " << person.get_age()
>>         << ", Address: " << person.get_address() << "]";
>>     return out;
>> }
>> 
>> Person::~Person() {}
>> ```

>[!column|no-i ttl-c] **PUBLIC inheritance class**
>>[!INFO|clean no-t]
>> **player.h**
>> ```cpp
>> #ifndef PLAYER_H
>> #define PLAYER_H
>> 
>> #include "person.h"
>> 
>> // Player will do public inheritance from Person
>> class Player : public Person
>> {
>>     friend std::ostream &operator<<(std::ostream &out, const Person &person);
>> 
>> public:
>>     Player();
>>     ~Player();
>> 
>>     // See the access we have to inherited members from Person
>>     void play()
>>     {
>>         m_fullName = "Rhiz Caballero"; // OK public data member
>>         m_age = 20;                    // OK protected data member
>>         // m_address = "Talisay";      // ERROR! Accessing a private data member
>>     }
>> 
>> private:
>>     int m_careerYear{}, healthFactor{};
>>     double m_salary{};
>> };
>> 
>> #endif // PLAYER_H
>> ```
>
>>[!INFO|clean no-t]
>> **player.cpp**
>> ```cpp
>> #include <iostream>
>> #include "person.h"
>> #include "player.h"
>> 
>> Player::Player() {}
>> 
>> std::ostream &operator<<(std::ostream &out, const Player &player)
>> {
>>     out << "Player [Full name: " << player.get_fullName()
>>         << ", Age: " << player.get_age()
>>         << ", Address: " << player.get_address() << "]";
>>     return out;
>> }
>> 
>> Player::~Player() {}
>> ```

>[!column|no-i ttl-c] **PROTECTED inheritance class**
>>[!INFO|clean no-t]
>> **nurse.h**
>> ```cpp
>> #ifndef NURSE_H
>> #define NURSE_H
>> 
>> #include "person.h"
>> 
>> // Nurse will do protected inheritance
>> class Nurse : protected Person
>> {
>>     friend std::ostream &operator<<(std::ostream &out, const Nurse &operand>> );
>> 
>> public:
>>     Nurse();
>>     ~Nurse();
>> 
>>     void nurseFunc1()
>>     {
>>         m_fullName = "Zero Two";
>>         m_age = 19;
>>         // m_address = "Space" // still private on the base class
>>     }
>> 
>> private:
>>     int nurseDataMember1{};
>> };
>> 
>> #endif // NURSE_H
>> ```
>
>>[!INFO|clean no-t]
>> **nurse.cpp**
>> ```cpp
>> #include "person.h"
>> #include "nurse.h"
>> #include <iostream>
>> 
>> Nurse::Nurse() {}
>> 
>> std::ostream &operator<<(std::ostream &out, const Nurse &operand)
>> {
>>     out << "Nurse [Full name: " << operand.get_fullName()
>>         << ", Age: " << operand.get_age()
>>         << ", Address: " << operand.get_address()
>>         << ", nurseDataMember1: " << operand.nurseDataMember1 << "]";
>>     return out;
>> }
>> 
>> Nurse::~Nurse() {}
>> ```

>[!column|no-i ttl-c] **PRIVATE inheritance class**
>>[!INFO|clean no-t]
>> **engineer.h**
>> ```cpp
>> #ifndef ENGINEER_H
>> #define ENGINEER_H
>> 
>> #include "person.h"
>> 
>> // Engineer is doing private inheritance
>> class Engineer : private Person
>> {
>>     friend std::ostream &operator<<(std::ostream &out, const Engineer &eng);
>> 
>> public:
>>     Engineer();
>>     ~Engineer();
>> 
>>     void engineerFunc1()
>>     {
>>         m_fullName = "Natsu Dragneel";
>>         m_age = 14;
>>         // m_address = "Fairy Tail" // private
>>     }
>> 
>> private:
>>     int engineerDataMember1{};
>> };
>> 
>> #endif // ENGINEER_H
>> ```
>
>>[!INFO|clean no-t]
>> **engineer.cpp**
>> ```cpp
>> #include <iostream>
>> #include "person.h"
>> #include "engineer.h"
>> 
>> Engineer::Engineer() {}
>> 
>> std::ostream &operator<<(std::ostream &out, const Engineer &eng)
>> {
>>     out << "Engineer [Full name: " << eng.get_fullName()
>>         << ", Age: " << eng.get_age()
>>         << ", Adress: " << eng.get_address()
>>         << ", engineerDataMember1: " << eng.engineerDataMember1>>  << "]";
>> 
>>     return out;
>> }
>> 
>> Engineer::~Engineer() {}
>> ```