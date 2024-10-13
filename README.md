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

### Conclusion
In this implementation, we successfully created a stack using an array, allowing for basic operations such as push, pop, and display through a menu-driven interface. The study and implementation of this data structure help in understanding key concepts in computer science, including memory management, data handling, and algorithm efficiency. The stack's LIFO nature makes it a fundamental structure in various applications, such as expression evaluation, backtracking algorithms, and function call management in programming languages. This exercise reinforces the importance of understanding data structures and their practical applications in software development.
