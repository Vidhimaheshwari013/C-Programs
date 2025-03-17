# Program 4

#include <iostream>
#include <string>  // For strlen()
using namespace std;

// Function to display ASCII values
void displayASCII(string str) {
    cout << "ASCII values:\n";
    for (char c : str) {
        cout << c << " -> " << int(c) << endl;
    }
}

// Function to concatenate two strings (without built-in functions)
void concatenateStrings(char str1[], char str2[]) {
    int i = 0, j = 0;
    while (str1[i] != '\0') {
        i++;
    }
    while (str2[j] != '\0') {
        str1[i] = str2[j];
        i++;
        j++;
    }
    str1[i] = '\0';
}

// Function to compare two strings
bool compareStrings(char str1[], char str2[]) {
    int i = 0;
    while (str1[i] != '\0' && str2[i] != '\0') {
        if (str1[i] != str2[i]) {
            return false;
        }
        i++;
    }
    return str1[i] == str2[i]; // Ensure both end at the same position
}

// Function to find string length using pointers
int stringLength(char* str) {
    int len = 0;
    while (*str != '\0') {
        len++;
        str++;
    }
    return len;
}

// Convert lowercase to uppercase
void toUppercase(char str[]) {
    int i = 0;
    while (str[i] != '\0') {
        if (str[i] >= 'a' && str[i] <= 'z') {
            str[i] -= 32;
        }
        i++;
    }
}

// Reverse string
void reverseString(char str[]) {
    int len = stringLength(str);
    for (int i = 0; i < len / 2; i++) {
        swap(str[i], str[len - i - 1]);
    }
}

int main() {
    char str1[100], str2[100];

    cout << "Enter first string: ";
    cin >> str1;
    cout << "Enter second string: ";
    cin >> str2;

    displayASCII(str1);

    // Concatenation
    concatenateStrings(str1, str2);
    cout << "Concatenated String: " << str1 << endl;

    // Comparison
    cout << "Strings are " << (compareStrings(str1, str2) ? "equal" : "not equal") << endl;

    // String length
    cout << "Length of first string: " << stringLength(str1) << endl;

    // Convert to uppercase
    toUppercase(str1);
    cout << "Uppercase String: " << str1 << endl;

    // Reverse string
    reverseString(str1);
    cout << "Reversed String: " << str1 << endl;

    return 0;
}
![image](https://github.com/user-attachments/assets/d846523f-f6c6-45c9-b3bc-47738de297ec)
![image](https://github.com/user-attachments/assets/7c013718-5bda-4ce6-98c7-f366c7d62123)
![image](https://github.com/user-attachments/assets/05f742b3-d7ee-4115-8aac-a3c4c7bb58fc)
![image](https://github.com/user-attachments/assets/5fa14acb-1221-41b8-8ce4-dc82c298f238)
# output

![image](https://github.com/user-attachments/assets/83d7628d-9281-4cf1-a84e-5727424bcf37)

