---
aliases:
tags:
- CPP/Class/Constructor
- CPP/Class/Inheritance
- CPP/Expressions/OperatorOverloading
- CPP/Library/string_view/string_view
---
**[[C++inheritance|BACK]]**

---
>[!recite|clean no-i] Inheritance across multiple files

**main.cpp**
```cpp
#include <iostream>
#include "player.h"

int main(int argc, char **argv) {
    Player p1("Basketball");
    
    p1.set_firstName("Rhiz");
    p1.set_lastName("Caballero");

    std::cout << "player: " << p1 << std::endl;

    return 0;
}
```
>[!column|no-t]
>>[!INFO|clean no-i] **person.h**
>> ```cpp
>> #ifndef PERSON_H
>> #define PERSON_H
>> 
>> #include <iostream>
>> #include <string>
>> 
>> class Person
>> {
>>     friend std::ostream &operator<<(std::ostream &out, const Person &person);
>> 
>> public:
>>     Person();
>>     Person(std::string &firstName_param, std::string &lastName_param);
>>     ~Person();
>> 
>>     // Getters
>>     std::string get_firstName() const { return firstName; }
>>     std::string get_lastName() const { return lastName; }
>> 
>>     void set_firstName(std::string_view fn) { firstName = fn; }
>>     void set_lastName(std::string_view ln) { lastName = ln; }
>> 
>> private:
>>     std::string firstName{"Keane"};
>>     std::string lastName{"Inting"};
>> };
>> 
>> #endif // PERSON_H
>> ```
>
>>[!INFO|clean no-i] **person.cpp**
>> ```cpp
>> #include "person.h"
>> 
>> Person::Person() {}
>> 
>> Person::Person(std::string &firstName_param, std::string &lastName_param)
>>     : firstName(firstName_param), lastName(lastName_param) {}
>> 
>> std::ostream &operator<<(std::ostream &out, const Person &person)
>> {
>>     out << "Person [" << person.firstName << " " << person.lastName << "]";
>>     return out;
>> }
>> 
>> Person::~Person() {}>> 
>> ```

>[!column|no-t]
>>[!INFO|clean no-i] **player.h**
>> ```cpp
>> #ifndef PLAYER_H
>> #define PLAYER_H
>> 
>> #include <string>
>> #include <iostream>
>> #include <string_view>
>> #include "person.h"
>> 
>> class Player : public Person
>> {
>>     friend std::ostream &operator<<(std::ostream &out, const Player &player);
>> 
>> public:
>>     Player() = default;
>>     Player(std::string_view game_param); // reference or string_view
>> 
>> private:
>>     std::string m_game{"None"};
>> };
>> 
>> #endif // PLAYER_H
>> ```
>
>>[!INFO|clean no-i] **player.cpp**
>> ```cpp
>> #include "person.h"
>> #include "player.h"
>> 
>> Player::Player(std::string_view game_param) : m_game(game_param)
>> {
>>     // firstName = "John"; // PRIVATE MEMBERS COMPILER ERROR!
>>     // lastName = "Snow";
>> }
>> 
>> std::ostream &operator<<(std::ostream &out, const Player &player)
>> {
>>     out << "Player: [game " << player.m_game
>>         << " names: " << player.get_firstName()
>>         << " " << player.get_lastName() << "]";
>> 
>>     return out;
>> }
>> ```