# Basics

## Basic chunks

### print elements of a vector
```c++
...
    vector<int> v_1{0, 1, 2};
    for (auto const& c : v_1) {
      std::cout << c << '\n';
    }
...
```

### create 2D containers (vectors of vectors)
```c++
...
    vector<vector<int>> v {{1,2}, {3,4}};
...
```

### vector access fails silently
Exception handling should be explicit?
```c++
int main() {
    vector<int> a = {0, 1, 2, 3, 4};
    // Add some code here to access and print elements of a.
    cout << a[0];
    cout << a[10];
    cout << "\n";
}
```
This prints `00`.

### iterate over containers
```c++
    vector<int> a {1, 2, 3, 4, 5};
    for (int i: a) {
        cout << i << "\n";
    }
```

### accumulate vector's elements
```c++
    return std::accumulate(v.begin(), v.end(), 0);
```

### open a file into a stream (buffer)
```c++
#include <fstream>
#include <iostream>
#include <string>

int main() {
    std::ifstream my_file;
    my_file.open("files/1.board");
    if (my_file.is_open()) {
        std::cout << "The file stream has been created!" << "\n";
        std::string line;
        while (getline(my_file, line)) {
            std::cout << line << "\n";
        }
    }
}
```

### process a string into a stream
```c++
#include <iostream>
#include <sstream>
#include <string>

using std::istringstream;
using std::string;
using std::cout;

int main() 
{
    string a("1 2 3");

    istringstream my_stream(a);

    int n;
    
    // Testing to see if the stream was successful and printing results.
    while (my_stream) {
        my_stream >> n;
        if (my_stream) {
            cout << "That stream was successful: " << n << "\n";
        }
        else {
            cout << "That stream was NOT successful!" << "\n";            
        }
    }
}
```

### use enums in switch
```c++
enum class BoardEnum {kEmpty, kObstacle};

string CellString(BoardEnum state) {
  string s;
  switch (state) {
    case BoardEnum::kObstacle : s = "⛰️   ";
    default: s = "0   ";  
  }
  return s;
}
```

### addresses and pointers
`&` and `*` operations provide different functionalities depending if they are left or right to the assigment:
```c++
// define a variable
int a = 5;

// create a reference (alias)
auto &b = a;  // b reference to the value of a

// handle the address
auto addr = &a;  // addr is the memory address

// A pointer to a is declared and initialized to the address of a.
int* pointer_to_a = &a;  // int* is the type of a pointer

// retrieve the value of a pointer
cout << *pointer_to_a  // print the value
```

### print variable types
```c++
in a = 5;
cout << typeid(a).name();
```



