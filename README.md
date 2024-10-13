# Experiment-18
### Aim
The aim of this project is to study and implement a stack data structure using arrays. This involves understanding the fundamental operations of a stack—namely push, pop, and display—and creating a simple menu-driven interface to interact with the stack.

### Theory
A **stack** is a linear data structure that follows the Last In, First Out (LIFO) principle. This means that the last element added to the stack is the first one to be removed. The primary operations for a stack are:

1. **Push**: Add an element to the top of the stack.
2. **Pop**: Remove the top element from the stack.
3. **Display**: Show all elements in the stack.

In this implementation, we utilize an array to store the stack elements. A top index will keep track of the current position in the stack, allowing efficient access to the last pushed element. We also handle situations like stack overflow (when trying to push to a full stack) and stack underflow (when trying to pop from an empty stack).
1)

### Algorithm for Stack Implementation Using STL in C++

1. **Include Necessary Libraries:**
   - Include `<iostream>` for input and output operations.
   - Include `<stack>` for stack operations.

2. **Define the Main Function:**
   - Start the `main` function.

3. **Create a Stack:**
   - Declare a stack `st` of integers.

4. **Push Elements onto the Stack:**
   - Use `st.push(30)` to add the element 30 to the stack.
   - Use `st.push(20)` to add the element 20 to the stack.
   - Use `st.push(10)` to add the element 10 to the stack.

5. **Access and Print the Top Element:**
   - Use `st.top()` to retrieve the top element of the stack (which should be 10).
   - Print the message "Top element of the stack: " followed by the value retrieved from `st.top()`.

6. **End the Program:**
   - Return 0 to indicate successful execution of the program.
```cpp
#include <iostream>
#include <stack>
using namespace std;

int main() {
    stack<int> st;

    // Push elements onto the stack
    st.push(30);
    st.push(20);
    st.push(10);

    // Print the top element of the stack
    cout << "Top element of the stack: " << st.top() << endl;

    return 0;
}
```

2. ### Algorithm for Stack Implementation Using Dynamic Array

1. **Define the Stack Class:**
   - Declare the `Stack` class with public members:
     - `int capacity` to hold the maximum size of the stack.
     - `int top` to track the index of the top element.
     - `int* arr` to dynamically allocate memory for stack elements.

2. **Constructor:**
   - Initialize the stack with a specified capacity.
   - Allocate memory for `arr` with the given capacity.
   - Set `top` to -1 to indicate that the stack is initially empty.

3. **Destructor:**
   - Deallocate memory used by `arr` when the stack object is destroyed.

4. **Push Method:**
   - Check if the stack is full (`top < capacity - 1`).
   - If not full, increment `top` and add the element at `arr[top]`.
   - If full, print "Stack Overflow".

5. **Pop Method:**
   - Check if the stack is empty (`top >= 0`).
   - If not empty, decrement `top`.
   - If empty, print "Stack Underflow".

6. **Peek Method:**
   - Check if the stack is empty (`top >= 0`).
   - If not empty, return the element at `arr[top]`.
   - If empty, return -1 to indicate the stack is empty.

7. **Main Function:**
   - Create an instance of `Stack` with a capacity of 5.
   - Push three integers (23, 24, 25) onto the stack.
   - Call the `peek` method to print the top element.
   - Call the `pop` method to remove the top element.
   - Call the `peek` method again to print the new top element.



```cpp
#include <iostream>
using namespace std;

class Stack {
public:
    int capacity;
    int top;
    int* arr;

    // Constructor to initialize stack
    Stack(int capacity) {
        this->capacity = capacity;
        arr = new int[capacity];
        top = -1; // Stack is initially empty
    }

    // Destructor to free memory
    ~Stack() {
        delete[] arr; // Deallocate memory
    }

    // Push method to add element to the stack
    void push(int element) {
        if (top < capacity - 1) { // Check if stack is not full
            top++;
            arr[top] = element;
        } else {
            cout << "Stack Overflow" << endl;
        }
    }

    // Pop method to remove the top element from the stack
    void pop() {
        if (top >= 0) {
            top--;
        } else {
            cout << "Stack Underflow" << endl;
        }
    }

    // Peek method to get the top element of the stack
    int peek() {
        if (top >= 0) {
            return arr[top];
        } else {
            return -1; // Indicate that the stack is empty
        }
    }
};

int main() {
    Stack st(5);
    st.push(23);
    st.push(24);
    st.push(25);

    cout << st.peek() << endl; // Output: 25
    st.pop();
    cout << st.peek() << endl; // Output: 24

    return 0;
}
```

### Conclusion
In this implementation, we successfully created a stack using an array, allowing for basic operations such as push, pop, and display through a menu-driven interface. The study and implementation of this data structure help in understanding key concepts in computer science, including memory management, data handling, and algorithm efficiency. The stack's LIFO nature makes it a fundamental structure in various applications, such as expression evaluation, backtracking algorithms, and function call management in programming languages. This exercise reinforces the importance of understanding data structures and their practical applications in software development.
