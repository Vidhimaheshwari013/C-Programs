# program 5

    include <iostream>
    include <vector>

    using namespace std;

    vector<int> mergeArrays(vector<int>& arr1, vector<int>& arr2) {
         vector<int> merged;
         int i = 0, j = 0;

         while (i < arr1.size() && j < arr2.size()) {
             if (arr1[i] < arr2[j])
                merged.push_back(arr1[i++]);
             else
                merged.push_back(arr2[j++]);
         }

        while (i < arr1.size()) merged.push_back(arr1[i++]);
        while (j < arr2.size()) merged.push_back(arr2[j++]);

        return merged;
    }

    int main() {
        vector<int> arr1 = {1, 3, 5, 7};
        vector<int> arr2 = {2, 4, 6, 8};

        vector<int> merged = mergeArrays(arr1, arr2);

        cout << "Merged sorted array: ";
        for (int num : merged) 
        cout << num << " ";

        return 0;
    }

![image](https://github.com/user-attachments/assets/f24c90b9-417f-4990-b500-b2664cecf3f4)
![image](https://github.com/user-attachments/assets/f40409bc-bea0-4984-ab1f-09b15c56f6b7)
# outpur
![image](https://github.com/user-attachments/assets/0ff8c9a1-374d-4790-862d-cf4178e9bf6d)
