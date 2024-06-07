#include <iostream>
#include <string> // Use the string header for std::string
using namespace std;

class person {
private:
    string name;
    string address;
    int age;
    long int citzno;

public:
    // Constructor with an initialization list
    person(string n, int a, string addr, long int c)
        : name(n), age(a), address(addr), citzno(c) {}

    void display() {
        cout << "Name: " << name << endl;
        cout << "Address: " << address << endl;
        cout << "Age: " << age << endl;
        cout << "Citizenship no: " << citzno << endl;
    }
};

int main() {
    string name;
    string address;
    int age;
    long int citzno;

    cout << "Enter the name" << endl;
    getline(cin, name); // Use getline for string input
    cout << "Enter the address" << endl;
    getline(cin, address); // Use getline for string input
    cout << "Enter the age" << endl;
    cin >> age;
    cin.ignore(); // Ignore the newline character left in the input stream

    if (age > 16) {
        cout << "Enter the citizenship number" << endl;
        cin >> citzno;
        person p(name, age, address, citzno);
        p.display();
    } else {
        person p(name, age, address, 0);
        p.display();
    }
    return 0;
}
