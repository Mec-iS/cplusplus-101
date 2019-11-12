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
