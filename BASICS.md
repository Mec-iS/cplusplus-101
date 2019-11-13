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

### accumulate vector's element
```c++
    return std::accumulate(v.begin(), v.end(), 0);
```
