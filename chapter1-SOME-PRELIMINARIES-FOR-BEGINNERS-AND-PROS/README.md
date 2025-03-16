To get started with gdb and its TUI (Text User Interface) mode, let's write a simple C++ program that we can debug. I'll also guide you step-by-step on how to use gdb in TUI mode to debug it.

Here's the code:

```cpp
#include <iostream>
using namespace std;

int add(int a, int b) {
    return a + b;
}

int subtract(int a, int b) {
    return a - b;
}

int main() {
    int x = 10;
    int y = 5;

    int sum = add(x, y);
    int difference = subtract(x, y);

    cout << "Sum: " << sum << endl;
    cout << "Difference: " << difference << endl;

    return 0;
}
```

### Instructions to Debug with gdb in TUI Mode:

1. **Save the Program**  
   Save the code to a file, e.g., `example.cpp`.

2. **Compile the Code with Debug Symbols**  
   Use the `-g` flag to include debugging symbols during compilation:
   ```bash
   g++ -g -o example example.cpp
   ```

3. **Start gdb in TUI Mode**  
   Run gdb with the `--tui` flag:
   ```bash
   gdb --tui example
   ```

4. **Set a Breakpoint**  
   Inside gdb, set a breakpoint at a specific line or function. For example, set a breakpoint in the `add` function:
   ```bash
   break add
   ```

5. **Run the Program**  
   Start the program in gdb:
   ```bash
   run
   ```

6. **Inspect the Execution**  
   When the breakpoint is hit, inspect variables using commands like `print`:
   ```bash
   print a
   print b
   ```

7. **Step Through the Code**  
   Use commands to step through the code:
   - `next` (execute the next line)
   - `step` (step into a function)

8. **Exit the Debugger**  
   To quit gdb, type:
   ```bash
   quit
   ```

While in TUI mode, you'll see a split-screen interface where the source code is displayed alongside the gdb console. This mode makes it easier to follow the execution flow visually.

