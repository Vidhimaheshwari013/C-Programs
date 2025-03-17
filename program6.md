# Program 6 

#include <iostream>
#include <vector>

using namespace std;

// Recursive binary search
int binarySearchRecursive(vector<int>& arr, int left, int right, int key) {
    if (left > right) return -1;
    int mid = left + (right - left) / 2;

    if (arr[mid] == key) return mid;
    if (arr[mid] > key) return binarySearchRecursive(arr, left, mid - 1, key);
    return binarySearchRecursive(arr, mid + 1, right, key);
}

// Iterative binary search
int binarySearchIterative(vector<int>& arr, int key) {
    int left = 0, right = arr.size() - 1;

    while (left <= right) {
        int mid = left + (right - left) / 2;
        if (arr[mid] == key) return mid;
        if (arr[mid] > key) right = mid - 1;
        else left = mid + 1;
    }
    return -1;
}

int main() {
    vector<int> arr = {1, 3, 5, 7, 9, 11};
    int key = 7;

    // Recursive search
    int indexRec = binarySearchRecursive(arr, 0, arr.size() - 1, key);
    cout << "Recursive Binary Search: " 
         << (indexRec != -1 ? "Found at index " + to_string(indexRec) : "Not found") 
         << endl;

    // Iterative search
    int indexIter = binarySearchIterative(arr, key);
    cout << "Iterative Binary Search: " 
         << (indexIter != -1 ? "Found at index " + to_string(indexIter) : "Not found") 
         << endl;

    return 0;
}
![image](https://github.com/user-attachments/assets/55834a9c-9e27-4000-b054-c15c911475fe)
![image](https://github.com/user-attachments/assets/f44ba695-9162-4293-96ce-237aa24e6ce0)

# output
![image](https://github.com/user-attachments/assets/b2b41950-5dc9-44cb-84e5-ed8937e6c857)

