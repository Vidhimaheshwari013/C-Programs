
# Program 1

    include <iostream>
    include <cmath>  // For pow()
    using namespace std;
    double seriesSum(int n) {
   
    double sum = 0;
    for (int i = 1; i <= n; i++) {
        double term = 1.0 / pow(i, i);
        if (i % 2 == 0) {
            sum -= term;  // Alternate terms are negative
        } else {
            sum += term;
        }
    }
    return sum;
    }

    int main() {
  
    int n;
    cout << "Enter the number of terms: ";
    cin >> n;

    cout << "Sum of series: " << seriesSum(n) << endl;
    return 0;
    }

![image](https://github.com/user-attachments/assets/4886cda5-2e9d-4f13-b7e5-ab56f4fe9dbe)

![image](https://github.com/user-attachments/assets/0b8ede8d-d2f4-4240-b480-1186f6410f90)
