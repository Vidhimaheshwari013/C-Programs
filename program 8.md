# Program 8

     #include <iostream>
     using namespace std;

     class Matrix {
         int mat[3][3];

     public:
         void input() {
             cout << "Enter matrix (3x3):\n";
             for (int i = 0; i < 3; i++)
                 for (int j = 0; j < 3; j++)
                     cin >> mat[i][j];
         }

         void display() {
             for (int i = 0; i < 3; i++) {
                 for (int j = 0; j < 3; j++)
                     cout << mat[i][j] << " ";
                 cout << endl;
             }
         }

         Matrix operator+(Matrix m) {
             Matrix res;
             for (int i = 0; i < 3; i++)
                 for (int j = 0; j < 3; j++)
                     res.mat[i][j] = mat[i][j] + m.mat[i][j];
             return res;
        }

         Matrix operator*(Matrix m) {
             Matrix res;
             for (int i = 0; i < 3; i++)
                 for (int j = 0; j < 3; j++)
                     for (int k = 0; k < 3; k++)
                    res.mat[i][j] += mat[i][k] * m.mat[k][j];
             return res;
         }

         Matrix transpose() {
             Matrix res;
             for (int i = 0; i < 3; i++)
                 for (int j = 0; j < 3; j++)
                     res.mat[i][j] = mat[j][i];
             return res;
         }
     };

     int main() {
         Matrix A, B, C;
         int choice;

         A.input();
         B.input();

        do {
             cout << "\nMenu:\n1. Sum\n2. Product\n3. Transpose\n4. Exit\nEnter choice: ";
             cin >> choice;

             switch (choice) {
                 case 1:
                     C = A + B;
                     C.display();
                     break;
                 case 2:
                     C = A * B;
                     C.display();
                     break;
                 case 3:
                     C = A.transpose();
                     C.display();
                     break;
                 case 4:
                     cout << "Exiting...\n";
                     break;
                 default:
                     cout << "Invalid choice!";
             }
         } while (choice != 4);

         return 0;
     }

![image](https://github.com/user-attachments/assets/fc62be21-43a1-4fe2-9c56-ef24355b9c6b)
![image](https://github.com/user-attachments/assets/4f432c63-47eb-44c5-88e0-dc2e0c4d39cc)
![image](https://github.com/user-attachments/assets/94e60101-b4bb-42f0-abb1-f5813e353f37)

![image](https://github.com/user-attachments/assets/034aa290-a337-4495-800d-834e1e927da9)

# OUTPUT


![image](https://github.com/user-attachments/assets/15ac244e-e1e6-484d-94a5-a7d271a65649)

![image](https://github.com/user-attachments/assets/64a76632-c66a-490e-878f-25d3efca3081)

![image](https://github.com/user-attachments/assets/0641a2ba-cf54-4465-973a-298d3706b2d4)
