# Toolkit Document – S.A & Volume Calculator (C Language)

## 1️. Title & Objective
**Project Title:** Getting Started with C – Surface Area & Volume Calculator  
**Objective:**  
To learn the basics of the C programming language by creating a simple program that calculates the area of a circle, the surface area of a sphere, and its volume.  
This toolkit will guide beginners through setup, coding, compiling, and testing steps.

---

## 2️. Quick Summary of the Technology
**C** is a powerful general-purpose programming language developed in the 1970s by *Dennis Ritchie*.  
It’s widely used for:
- Operating systems (e.g., Linux kernel)
- Embedded systems
- Performance-critical applications

C teaches how computers manage memory, data types, and logic at a low level.  
It uses a **compiler** to translate code into machine language for execution.

**Real-world example:**  
The *Git version control system* and the *Linux operating system* are both written in C.

---

## 3️. System Requirements

| Requirement | Description |
|--------------|-------------|
| **Operating System** | Windows / Linux / macOS |
| **Compiler** | GCC (GNU Compiler Collection) |
| **Text Editor / IDE** | Visual Studio Code, Code::Blocks, or any text editor |
| **Libraries Used** | `stdio.h` and `math.h` |

---

## 4️. Installation & Setup Instructions

### For Windows
1. Download and install **MinGW** from [https://www.mingw-w64.org](https://www.mingw-w64.org).  
2. Add `C:\MinGW\bin` to your PATH environment variable.  
3. Open Command Prompt and verify installation:
   ```bash
   gcc --version

## 5. Create a working folder and save your file as sphere_calc.c.

### For Linux / macOS

-Open Terminal.
-Install GCC (if not installed):
sudo apt install build-essential     # Ubuntu/Debian

brew install gcc                     # macOS
-Save your program as sphere_calc.c in any folder.

-Navigate to the folder in the terminal
## 6. Minimal working example
### Source code

#include <stdio.h>
#include <math.h>

int main() {
    // SAMPLE PROJECT TO: calculate the surface area and volume of a sphere

    double radius = 0.0;
    double area = 0.0;
    double surfacearea = 0.0;
    double volume = 0.0;
    const double PI = 3.14159;

    printf("Enter the radius: ");
    scanf("%lf", &radius);

    area = PI * pow(radius, 2);
    surfacearea = 4 * PI * pow(radius, 2);
    volume = (4.0 / 3.0) * PI * pow(radius, 3);

    printf("Area: %.2lf\n", area);
    printf("Surface Area: %.2lf\n", surfacearea);
    printf("Volume: %.2lf\n", volume);

    return 0;
}
### How to compile and run
gcc sphere_calc.c -o sphere_calc -lm

./sphere_calc

### Example Output
Enter the radius: 5

Area: 78.54

Surface Area: 314.16

Volume: 523.60

## 7. AI Prompt Journal
| Prompt Used                                                     | AI Response Summary                                             | Reflection                                                |
| --------------------------------------------------------------- | --------------------------------------------------------------- | --------------------------------------------------------- |
| “Explain how to write and compile a C program using GCC.”       | Gave setup steps, `gcc` commands, and structure of `main()`     | Helped me understand the compilation process clearly      |
| “How can I calculate surface area and volume of a sphere in C?” | Provided mathematical formulas and sample implementation        | Guided me in writing the correct mathematical expressions |
| “What are common C errors for beginners?”                       | Listed missing semicolons, wrong data types, missing `#include` | Helped me debug syntax errors                             |
| “Why do I need `-lm` when compiling?”                           | Explained linking with math library for `pow()`                 | Helped fix “undefined reference to pow” error             |


## 8. Common issues and fixes
| Issue                          | Cause                                   | Fix                                      |
| ------------------------------ | --------------------------------------- | ---------------------------------------- |
| `'gcc' is not recognized`      | GCC not installed or PATH not set       | Install MinGW and add to PATH            |
| `undefined reference to 'pow'` | Math library not linked                 | Add `-lm` flag when compiling            |
| Wrong output (e.g., 0)         | Missing input or wrong format specifier | Use `%lf` for `double` in `scanf()`      |
| Program closes instantly       | Running via double-click                | Run program from terminal or IDE console |

## 9. References

Learn-C.org

GeeksforGeeks – C Language Guide

DevDocs.io C Documentation

GNU GCC Documentation

## 10. Future Improvements / To-Do List

 Add user input validation (check if radius > 0)

 Include options for other shapes (cube, cylinder, cone)

 Implement a menu-driven interface

 Add error handling for invalid input

 Format output neatly with more descriptive text

 Create version 2.0 with GUI (using C & GTK or C++)

## Summary & Reflection

This project was a great introduction to C programming and mathematical operations using math.h.
### Through this toolkit, I learned:

How to compile and run a C program manually.

How to use pow() and constants like PI.

How to troubleshoot common syntax and linking errors.

Creating this project helped me understand not just how C works, but why it’s so powerful for system-level logic and performance programming.

## License

This project is released under the MIT License.
You’re free to use, modify, and share it as long as you credit the author.

Author: John Njoroge
