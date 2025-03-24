# program 7

 #include <iostream>

     using namespace std;

     // Recursive GCD
     int gcdRecursive(int a, int b) {
         return (b == 0) ? a : gcdRecursive(b, a % b);
     }

     // Non-recursive GCD
     int gcdIterative(int a, int b) {
         while (b != 0) {
             int temp = b;
             b = a % b;
             a = temp;
         }
         return a;
     }

     int main() {
         int a, b;
         cout << "Enter two numbers: ";
         cin >> a >> b;

         cout << "GCD (Recursive): " << gcdRecursive(a, b) << endl;
         cout << "GCD (Iterative): " << gcdIterative(a, b) << endl;

         return 0;
     }
![image](https://github.com/user-attachments/assets/cfcc1f49-eb94-44b5-bbc5-64e3be3a4f3f)
![image](https://github.com/user-attachments/assets/919faa65-fcc6-4615-b9b2-3c2b20d3d444)
# OUTPUT
![image](https://github.com/user-attachments/assets/a7440b82-5d2a-4fb2-b758-cd0ed0def1da)







