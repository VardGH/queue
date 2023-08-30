# Queue Adapter

This repository contains a C++ queue adapter class implemented using a vector as the underlying data structure.

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- - [Usage](#usage)
  - [Installation](#installation)
  - [Example](#example)

## Introduction

The Queue Adapter is a C++ class that provides an interface for working with queues. It is implemented using the Standard Template Library (STL) `std::vector` as the underlying data structure. The class offers basic queue operations such as push, pop, top, size, and empty.

## Features

- Intuitive and easy-to-use queue interface.
- Support for copy construction, copy assignment, move construction, and move assignment.
- Proper encapsulation and namespace usage.
- Efficient storage and retrieval of elements using `std::vector`.

## Usage

### Installation

To utilize the Queue Adapter class in your project, follow these steps:

1. Clone this repository to your local machine.
2. Include the `queue.hpp` header file in your C++ project.
3. You can then employ the `adapter::queue<T>` class in your code.

### Example

```cpp
#include "queue.hpp"
#include <iostream>

int main() {
    adapter::queue<int> myQueue;

    myQueue.push(10);
    myQueue.push(20);
    myQueue.push(30);

    std::cout << "Front element: " << myQueue.top() << std::endl;
    myQueue.pop();
    std::cout << "Front element after pop: " << myQueue.top() << std::endl;

    std::cout << "Queue size: " << myQueue.size() << std::endl;
    std::cout << "Is queue empty? " << (myQueue.empty() ? "Yes" : "No") << std::endl;

    return 0;
}
```