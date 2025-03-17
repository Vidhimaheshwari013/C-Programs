# Program-3 

#include <iostream>
#include <string>
#include <map>
using namespace std;

void countOccurrences(string str) {
    map<char, int> freq;

    for (char c : str) {
        if (isalpha(c)) {  // Consider only alphabets
            freq[tolower(c)]++;
        }
    }

    cout << "Character Frequency Table:\n";
    for (auto pair : freq) {
        cout << pair.first << " -> " << pair.second << endl;
    }
}

int main() {
    string input;
    cout << "Enter a string: ";
    getline(cin, input);

    countOccurrences(input);

    return 0;
}

![image](https://github.com/user-attachments/assets/67b82c08-5aa6-423c-85be-1cbdc45254b3)
![image](https://github.com/user-attachments/assets/c3cc685b-e9fe-45f6-b367-908b0c54bf55)

output

![image](https://github.com/user-attachments/assets/0877f61e-7f66-488a-bc6e-570908afe85e)
