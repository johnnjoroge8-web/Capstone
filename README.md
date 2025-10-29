#  S.A & Volume Calculator  
*A beginner-friendly C program for calculating the surface area and volume of a sphere.*

## Description
**S.A & Volume Calculator** is a simple C-based console application that allows users to calculate:
- The **area of a circle** based on a given radius.  
- The **surface area** of a sphere.  
- The **volume** of a sphere.
This program prompts the user for a radius (double) and prints:
- Area (πr²)
- Surface Area (4πr²)
- Volume (4/3 πr³)

Uses math functions from math.h.

## Requirements
- A C compiler installed and available in PATH (e.g., GCC via MinGW-w64 or MSVC Build Tools on Windows).
- C standard library and math library (math.h). For GCC, link math with -lm if needed.

## Build (Windows, GCC)
1. Open a terminal in the project folder (where sampproj.c is located).
2. Compile:
   gcc sampproj.c -o sampproj.exe -lm
3. Run:
   .\sampproj.exe

(If using MSVC, use the Visual Studio Developer Command Prompt and compile with cl.)

## Notes
- The program uses a constant PI = 3.14159; replace with M_PI from math.h for greater precision if available.
- Ensure the compiler can find and link the math library; GCC often requires -lm.
- Validate input in production code (current program assumes valid numeric input).

## To clone this repository or download the project file:

git clone https://github.com/johnnjoroge8-web/Capstone.git
cd Capstone


### To compile the program:

gcc sampproj.c -o calculator -lm


### To run the program:

calculator

## For Linux / macOS

Open a terminal.

Install GCC (if not installed):

sudo apt install build-essential       # Ubuntu/Debian
brew install gcc                       # macOS


Navigate to the project directory:

cd Capstone


### To compile the code:

gcc sampproj.c -o calculator -lm


### To run the executable:

./calculator

## Usage
Run the executable and enter a numeric radius when prompted.

Enter the radius:


You then enter any numeric value, for example:

Enter the radius: 5


Expected Output:

Area: 78.54
Surface Area: 314.16
Volume: 523.60

## Features Overview

### Calculates:

The area of a circle (πr²)

The surface area of a sphere (4πr²)

The volume of a sphere ((4/3)πr³)

### Simple and interactive command-line interface
### Beginner-friendly and well-commented code
### Works across Windows, macOS, and Linux

## Configuration Options

Currently, the project does not require any external configuration.

However, you can modify the following variables in the code for customization:

const double PI = 3.14159;  // You can adjust precision here
Or extend the program to compute other geometric properties.

## Code Structure Overview
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


## Key Points:

- Uses pow() from math.h for exponentiation.
- Takes radius input from the user.
- Calculates and prints results with formatted precision (%.2lf).

## Troubleshooting
### Problems		
- gcc: command not found
- undefined reference to 'pow'
- The program closes instantly after running
- Wrong output values

### Possible Causes
- GCC not installed or not added to PATH
- Missing math library flag
- Running via double-click instead of the terminal
- Incorrect input (non-numeric or negative

### Solution
- Install GCC and verify with gcc --version
- Add -lm when compiling: gcc sampproj.c -o calculator -lm
- Run the program from the Command Prompt or Terminal
- Ensure you input positive numeric values for radius

## Contributing Guidelines
Contributions are welcome! Here’s how you can help:
### Fork this repository.

### Create a new branch:
git checkout -b feature-name

### Commit your changes:

git commit -m "Added new feature"

### Push to your branch:

git push origin feature-name

### Open a Pull Request and describe what you’ve improved.

## Possible improvements:
Add input validation for radius.

Extend the program to calculate other shapes (e.g., cube, cylinder).

Add a menu-driven interface?

## License

This project is open-source under the MIT License.

You’re free to use, modify, and distribute it as long as proper credit is given.

## Author
### John Njoroge




