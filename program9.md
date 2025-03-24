# Program 9
     #include <iostream>
     using namespace std;

     class Person {
     protected:
         string name;
         int age;
     public:
         void input() {
             cout << "Enter name and age: ";
             cin >> name >> age;
         }
         void display() {
             cout << "Name: " << name << ", Age: " << age << endl;
         }
     };

     class Student : public Person {
         string course;
     public:
         void input() {
             Person::input();
             cout << "Enter course: ";
             cin >> course;
         }
         void display() {
             Person::display();
             cout << "Course: " << course << endl;
         }
     };

     class Employee : public Person {
         int salary;
     public:
         void input() {
             Person::input();
             cout << "Enter salary: ";
             cin >> salary;
         }
         void display() {
             Person::display();
             cout << "Salary: " << salary << endl;
         }
     };

     int main() {
         Student s;
         Employee e;

         cout << "Enter student details:\n";
         s.input();

         cout << "Enter employee details:\n";
         e.input();

         cout << "\nStudent Details:\n";
         s.display();

         cout << "\nEmployee Details:\n";
         e.display();

         return 0;
     }

![image](https://github.com/user-attachments/assets/99c22dd3-fef1-4826-b409-91b8a22b2c6f)

![image](https://github.com/user-attachments/assets/35636887-ce4f-4b7c-9559-ecede7a464de)

![image](https://github.com/user-attachments/assets/0ce338ea-bb2f-4736-aab5-a85493688e4d)

# OUTPUT
![image](https://github.com/user-attachments/assets/e9c3cdf3-3279-4eb6-8ed1-3b2805411433)
