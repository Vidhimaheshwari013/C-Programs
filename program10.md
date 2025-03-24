# program 10

     #include <iostream>
     #include <cmath>
     using namespace std;

     class Triangle {
     public:
         // Area with base & height
         double area(double base, double height) {
             return 0.5 * base * height;
         }

         // Area with 3 sides (Heron's formula)
         double area(double a, double b, double c) {
             double s = (a + b + c) / 2;
             return sqrt(s * (s - a) * (s - b) * (s - c));
         }
     };

     int main() {
         Triangle t;
         cout << "Area (Base, Height): " << t.area(5, 10) << endl;
         cout << "Area (Three Sides): " << t.area(3, 4, 5) << endl;
         return 0;
     }
![image](https://github.com/user-attachments/assets/6515cd03-5504-4791-bfdd-ba2c7fcd0098)
# output
![image](https://github.com/user-attachments/assets/858d2d1a-c83e-4305-ac10-ca436d18700a)

