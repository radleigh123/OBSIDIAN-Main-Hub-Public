---
aliases:
tags:
- CPP/Expressions/OperatorOverloading/operator<<
---
**[[C++operatoroverloading|BACK]]**

---
>[!recite|clean no-i] ### `operator<<`
is a stream insertion operator, which is used to write the output to the output stream.

```cpp
friend ostream &operator<<(ostream& os, const Person& p);\n
friend istream &operator>>(istream& is, Person& p);

ostream& operator<<(ostream& os, const Person& p) {
    os << p.name << " " << p.age;
    return os;
}

istream &operator>>(istream &is, Person &p) {
	is >> p.name >> p.age;
	return is;
}
```