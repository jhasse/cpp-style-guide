# C++ Style Guide

Style guide for C++

## File encoding

UTF-8, Unix file endings.

## Indentation

Tabs for indentation, spaces for alignment.

## Naming

CamelCase for Types, camelCase for names.

```cpp
class Example {
public:
  void fooBar(int firstVar
              int secondVar) {
    for (int i = 0; i < 10; ++i) {
      std::cout << i << std::endl;
    }
  }
};
```

## Includes

Local includes before system ones:

```cpp
#include "thisfile.hpp"

#include "a.hpp"
#include "b.hpp"

#include <iostream>
```
