---
aliases:
tags:
- CPP/Lecture
- CPP/Polymorphism
- CPP/Arrays
---
**[[C++|HOME [C++]]]**

---
## Polymorphic objects stored in collections
>[!FAIL|alt-co] Instead of using raw data
> ```cpp
> Base base1[] {circle1, oval1, circle2, oval2};
> ```

>[!column|no-t flex]
>>[!INFO|clean no-i ttl-c collapse] Use raw pointers
>> ```cpp
>> Base *base1[]{&circle1, &oval1, &circle1, &oval2};
>> 
>> for (Base *ptr : base1) {
>> 	std::cout << "Inside array, sizeof(*ptr): " << sizeof(*ptr) << std::endl;
>> 	ptr->draw();
>> }
>> ```
>
>>[!INFO|clean no-i ttl-c collapse] Use smart pointers
>> ```cpp
>> std::shared_ptr<Base> base1[]{std::make_shared<Circle>(12.2, "Circle1"), std::make_shared<Oval>(10.25, 20.33, "Oval1")};
>> for (auto &i : base1) {
>> 	i->draw();
>> }
>> ```