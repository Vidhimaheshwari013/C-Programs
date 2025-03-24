# Program 11
#include <iostream>
#include <stdexcept>

using namespace std;

class MatrixException : public exception {
public:
    const char* what() const noexcept override {
        return "Matrix dimensions are incompatible!";
    }
};

void checkCompatibility(int rows1, int cols1, int rows2, int cols2) {
    if (cols1 != rows2)
        throw MatrixException();
}

int main() {
    try {
        checkCompatibility(2, 6, 4, 2); // This will throw an exception
    } catch (const MatrixException& e) {
        cout << "Error: " << e.what() << endl;
    }
    return 0;
}
![image](https://github.com/user-attachments/assets/d4e0e1dc-b974-4f21-9aac-383fcfff2e88)
# OUTPUT
![image](https://github.com/user-attachments/assets/08bbff44-2f29-4463-9ae9-e26c8371e567)
