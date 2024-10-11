# EXP-20


#### Aim 
To study and implement sorting algorithm C++. 

#### Software 
Visual Studio Code 

#### Theory 
<ul>
    Sorting algorithms are used to rearrange elements of a list in a specific order, typically either ascending or descending. Below, I'll explain a few common sorting algorithms in C++.

1. Bubble Sort
Bubble Sort repeatedly compares adjacent elements and swaps them if they are in the wrong order. This process is repeated until the list is sorted.

2. Selection Sort
Selection Sort finds the minimum element from the unsorted part of the list and swaps it with the first unsorted element. It repeats this process until the list is sorted.

3. Insertion Sort
Insertion Sort builds the sorted list one item at a time by repeatedly taking one unsorted item and inserting it into the correct position within the sorted part of the list.

</li>
</ul>

#### Code 

(A) <br> 
```cpp
//RIDDHI LOKHANDE
//23070123107
//EXP 20 A
//ENTCB2
#include<iostream>
using namespace std;

void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

void s_sort(int *a, int elements) {
    int n = 0;
    int *b;

    while (n < elements) {
        b = a + 1;
        for (int i = 0; i < (elements - 1) - n; i++) {
            if (*a > *b) {
                swap(a, b);
            }
            b++;
        }
        n++;
        a++;
    }
}

int main() {
    int no_el;
    cout << "How many elements in your array?" << endl;
    cin >> no_el;
    int arr[no_el];

    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cin >> arr[i];
    }

    s_sort(arr, no_el);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    return 0;
}
```

#### Output 
(A) <br> 
![image](https://github.com/user-attachments/assets/c69a7acf-feea-484d-9e50-9d6b7b776f50)

 


(B) <br> 
```cpp
//RIDDHI LOKHANDE
//23070123107
//EXP 20 B
//ENTC B2
#include<iostream>
using namespace std;

void swap(int *a, int *b) {
    int temp;
    temp = *a;
    *a = *b;
    *b = temp;
}

void bubbleSort(int *a, int elements) {
    int n = 0;
    int *b;

    while (n < elements) {
        b = a + 1;
        for (int i = 0; i < (elements - 1) - n; i++) {
            if (*a > *b) {
                swap(a, b);
            }
            b++;
        }
        n++;
        a++;
    }
}

int main() {
    int no_el;
    cout << "How many elements in your array?" << endl;
    cin >> no_el;

    int arr[no_el];
    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cin >> arr[i];
    }

    bubbleSort(arr, no_el);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < no_el; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;

    return 0;
} 
```

#### Output 
(B) <br> 
![image](https://github.com/user-attachments/assets/61c520ae-b64c-43da-bba3-19031a4c81f5)

(B) <br> 
```cpp
//RIDDHI LOKHANDE
//23070123107
//EXP 20 C
//ENTC B2
#include<iostream>
using namespace std;

void insertionSort(int arr[], int n) {
    for (int i = 1; i < n; i++) {
        int key = arr[i];
        int j = i - 1;

        // Move elements of arr[0..i-1], that are greater than key, to one position ahead of their current position
        while (j >= 0 && arr[j] > key) {
            arr[j + 1] = arr[j];
            j = j - 1;
        }
        arr[j + 1] = key;
    }
}

int main() {
    int n;
    cout << "How many elements in your array?" << endl;
    cin >> n;
    
    int arr[n];
    cout << "Enter the elements of the array: " << endl;
    for (int i = 0; i < n; i++) {
        cin >> arr[i];
    }

    insertionSort(arr, n);

    cout << "Sorted array: " << endl;
    for (int i = 0; i < n; i++) {
        cout << arr[i] << " ";
    }
    cout << endl;
    
    return 0;
}
```

#### Output 
(B) <br> 
![image](https://github.com/user-attachments/assets/b2755e3a-e9c8-4f35-b9f7-2c8c87ab334d)




#### Conclusion 
I learnt the study and implement sorting algorithm C++.
