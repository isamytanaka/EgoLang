# EgoLang Documentation

![EgoLang Logo](https://egolang.neocities.org/imagem_convertida.png)

**Version: 2.7.9 (March 2025)**

## Table of Contents
- [Introduction](#introduction)
- [Main Features](#main-features)
- [Basic Syntax](#basic-syntax)
  - [Comments](#comments)
  - [Variables](#variables)
  - [Control Structures](#control-structures)
  - [Functions](#functions)
- [Practical Examples](#practical-examples)
  - [Variable Usage](#variable-usage)
  - [Conditional Logic](#conditional-logic)
  - [Loops](#loops)
  - [Functions](#functions-1)
  - [Complex Examples](#complex-examples)
- [Error Handling](#error-handling)
- [Compilation Process](#compilation-process)
- [Language Limitations](#language-limitations)
- [Using the Compiler](#using-the-compiler)

## Introduction

EgoLang is a strongly-typed programming language specifically engineered to provide developers with precise control over variable visibility and mutability. By enforcing explicit declarations and strict typing, EgoLang creates a coding environment where data integrity and access patterns are clear, making your programs more reliable, maintainable, and secure.

The philosophy behind EgoLang emphasizes clarity and explicit intent in every line of code. Each variable or function declaration clearly communicates its scope, modifiability, and data expectations, which eliminates many of the ambiguities and potential bugs found in less strict languages.

## Main Features

### Visibility Control
EgoLang enforces explicit visibility declarations for all variables and functions, creating clear boundaries between different parts of your code. This leads to more maintainable codebases, especially in larger projects where data access control becomes crucial.

### Explicit Mutability
Every variable in EgoLang includes a clear declaration of whether it can be modified after initialization. This prevents unexpected changes to critical values and makes code behavior more predictable across the entire application.

### Strong Typing
The language's strict type system ensures that values are used consistently throughout your code. Type incompatibilities are caught at compile time rather than causing runtime failures, significantly reducing the potential for bugs.

### Error Detection
EgoLang's compiler performs comprehensive static analysis to identify potential issues before execution. Error messages are clear and actionable, helping developers quickly resolve problems in their code.

### JIT Compilation
The language uses Just-In-Time compilation to transform EgoLang code into optimized Python bytecode, providing good performance while maintaining strong safety guarantees.

### Clear Structure
The syntax is designed to be explicit and consistent, which improves readability and makes code maintenance simpler. Every element of the language follows predictable patterns that are easy to understand.

## Basic Syntax

### Comments

EgoLang supports both single-line and multi-line comments to help document your code:

```
// This is a single-line comment

/* This is a
   multi-line comment
   that spans multiple lines */
```

### Variables

Variables in EgoLang follow a strict declaration pattern that includes visibility, mutability, type, and name:

```
visibility mutability type name = value;
```

For example:

```
public mutable int counter = 0;
private immutable string name = "EgoLang";
protected const bool isEnabled = true;
```

#### Visibility Modifiers

- `public`: Accessible from anywhere in the program
- `private`: Limited to the current scope, not accessible from outside
- `protected`: Accessible in the current scope and any child scopes

#### Mutability Modifiers

- `mutable`: The variable's value can be changed after declaration
- `immutable`: The variable's value cannot be changed after declaration
- `const`: Cannot be changed (effectively the same as immutable)

#### Data Types

- `int`: Integer values (whole numbers)
- `float`: Floating-point values (decimal numbers)
- `string`: Text values enclosed in quotes
- `bool`: Boolean values (true/false)
- `list`: Ordered collection of values
- `dict`: Key-value pairs (associative array)

### Control Structures

#### Conditionals (if-else)

```
if (condition) {
    // Code executed when condition is true
} else if (anotherCondition) {
    // Code executed when anotherCondition is true
} else {
    // Code executed when all conditions are false
}
```

#### Loops

For Loops:
```
for (initialization; condition; update) {
    // Code executed repeatedly while condition is true
}
```

While Loops:
```
while (condition) {
    // Code executed repeatedly while condition is true
}
```

### Functions

Functions are declared with visibility, the `function` keyword, name, parameters, and body:

```
visibility function name(type param1, type param2, ...) {
    // Function body
    return value;
}
```

For example:

```
public function calculateArea(int width, int height) {
    public mutable int area = width * height;
    return area;
}
```

### Printing Values

```
print(value);
```

## Practical Examples

### Variable Usage

Basic variable declaration and manipulation:

```
// Declaring different types of variables
public mutable int counter = 10;
private immutable string message = "Hello, EgoLang!";
protected const float PI = 3.14159;

// Manipulating mutable variables
counter = counter + 5;
print(counter);  // Outputs: 15

// Using variables together
public mutable string result = message + " Counter: " + counter;
print(result);  // Outputs: Hello, EgoLang! Counter: 15
```

### Conditional Logic

Making decisions with if statements:

```
public mutable int temperature = 22;
public mutable string weather = "sunny";

if (temperature > 25) {
    if (weather == "sunny") {
        print("It's hot and sunny!");
    } else {
        print("It's hot but not sunny.");
    }
} else if (temperature < 15) {
    print("It's cold outside.");
} else {
    print("The temperature is pleasant.");
}

// Combining conditions
if (temperature > 20 && weather == "sunny") {
    print("Perfect day for a picnic!");
}
```

### Loops

Working with different types of loops:

```
// While loop that counts from 1 to 5
public mutable int counter = 1;
while (counter <= 5) {
    print("Count: " + counter);
    counter = counter + 1;
}

// For loop that iterates through numbers
for (public mutable int i = 0; i < 5; i = i + 1) {
    print("Iteration: " + i);
}

// Loop with conditional break
public mutable int sum = 0;
for (public mutable int i = 1; i <= 100; i = i + 1) {
    sum = sum + i;
    if (sum > 500) {
        print("Sum exceeded 500 at i = " + i);
        break;
    }
}
```

### Functions

Defining and using functions:

```
// Function to check if a number is prime
public function isPrime(int num) {
    if (num <= 1) {
        return false;
    }
    if (num <= 3) {
        return true;
    }
    if (num % 2 == 0 || num % 3 == 0) {
        return false;
    }
    
    public mutable int i = 5;
    while (i * i <= num) {
        if (num % i == 0 || num % (i + 2) == 0) {
            return false;
        }
        i = i + 6;
    }
    
    return true;
}

// Using the function
public mutable int testNumber = 17;
if (isPrime(testNumber)) {
    print(testNumber + " is a prime number.");
} else {
    print(testNumber + " is not a prime number.");
}
```

### Complex Examples

Calculating Fibonacci numbers:

```
public function fibonacci(int n) {
    if (n <= 0) {
        return 0;
    }
    if (n == 1 || n == 2) {
        return 1;
    }
    
    public mutable int a = 1;
    public mutable int b = 1;
    public mutable int result = 0;
    
    for (public mutable int i = 3; i <= n; i = i + 1) {
        result = a + b;
        a = b;
        b = result;
    }
    
    return result;
}

// Print the first 10 Fibonacci numbers
for (public mutable int i = 1; i <= 10; i = i + 1) {
    print("Fibonacci(" + i + ") = " + fibonacci(i));
}
```

Temperature converter:

```
public function celsiusToFahrenheit(float celsius) {
    return (celsius * 9/5) + 32;
}

public function fahrenheitToCelsius(float fahrenheit) {
    return (fahrenheit - 32) * 5/9;
}

// Converting temperatures
public mutable float tempC = 25.0;
public mutable float tempF = celsiusToFahrenheit(tempC);
print(tempC + "°C is equal to " + tempF + "°F");

public mutable float originalF = 98.6;
public mutable float convertedC = fahrenheitToCelsius(originalF);
print(originalF + "°F is equal to " + convertedC + "°C");
```

## Error Handling

The EgoLang compiler performs thorough static analysis to catch potential issues before runtime. It will generate errors for:

1. **Mutability violations**: Attempts to modify immutable or const variables
   ```
   public immutable int counter = 5;
   counter = 10;  // Error: Cannot modify immutable variable 'counter'
   ```

2. **Visibility violations**: Accessing variables outside their declared scope
   ```
   private function helper() {
       private mutable int internalValue = 42;
       return internalValue;
   }
   public mutable int result = internalValue;  // Error: 'internalValue' is not accessible in this scope
   ```

3. **Type errors**: Operations with incompatible types
   ```
   public mutable int number = 10;
   public mutable string text = "Count: ";
   public mutable int result = text + number;  // Error: Cannot add string and int directly
   ```

4. **Syntax errors**: Malformed code structures
   ```
   if temperature > 30 {  // Error: Missing parentheses around condition
       print("It's hot!");
   }
   ```

5. **Undefined references**: Using variables or functions that don't exist
   ```
   print(undefinedVariable);  // Error: 'undefinedVariable' is not defined
   ```

Error messages include the line number and a clear explanation of the issue, making it easier to locate and fix problems in your code.

## Compilation Process

The EgoJITCompiler processes EgoLang code through several phases:

1. **Lexical Analysis**: Cleans the source code by removing comments and normalizing whitespace
2. **Parsing**: Divides the code into logical blocks and validates the syntax
3. **Semantic Analysis**: Checks for type compatibility and visibility/mutability rules
4. **Code Generation**: Translates each validated block to equivalent Python code
5. **Scope Management**: Tracks variables and their properties in different scopes
6. **Bytecode Compilation**: Compiles the generated Python code to optimized bytecode
7. **Execution**: Runs the bytecode in the Python virtual machine

> **⚠️ Note:** Compiled EgoLang programs run in the Python runtime environment, but the compiler ensures that all EgoLang's variable access and mutability rules are maintained throughout execution.

## Language Limitations

While EgoLang provides strong guarantees for code safety and clarity, it currently has some limitations:

- **No object-oriented features**: EgoLang doesn't support classes or inheritance
- **Limited standard library**: The language provides only basic built-in functions
- **No exception handling**: There's no built-in mechanism for structured error handling at runtime
- **Limited data structures**: Complex data structures beyond basic lists and dictionaries are not natively supported
- **No concurrency model**: EgoLang doesn't provide built-in support for threading or parallel execution

## Using the Compiler

To compile and run EgoLang code:

1. Navigate to the `src/Ego_compiler` file in your installation
2. Find the `sample_code` variable at the end of the file
3. Replace its content with your EgoLang code:

```python
sample_code = """
public mutable int x = 10;
public function double(int value) {
    return value * 2;
}
print(double(x));
"""
```

4. Specify your desired output filename in the compile function:

```python
compiler.compile(sample_code, 'my_program.ego')
```

5. Run the compiler to generate and execute your code

The compiler will process your code, report any errors it finds, and generate Python bytecode that maintains all of EgoLang's safety guarantees.
