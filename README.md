## EgoLang - 
>  **Version: 2.7.9 (Update, March, 29th, 2025)**

![Logoprimary](https://egolang.neocities.org/1743296644840.png)


# Ego Language Documentation

## Overview

> Ego is a strongly-typed programming language with explicit visibility and mutability controls. It compiles to Python bytecode and provides a structured approach to programming with clear rules about variable access and modification.

##


> Ego includes a small set of standard packages, most of which were created to fix language errors, adjust logic, and more.

All packages are compiled and located in the directory:

``/std_packpages``

The available packages are:

**pkg_dataconfig.ego**  
A simple package for handling syntax and data (private, public, etc.).

**How to import it?**

1. Place the file in the same directory as the compiler.
2. Import the package using the following command:

```python
from pkg_dataconfig import *
```

3. Call the function:

```python
pkg_dataconfig();
```

That's it! This package handles some errors in the compiler, mainly when translating explicit data and other details.

**Source code available in:**  
pkg_dataconfig_nocompiled.ego

---

**Sizeof_pkg**  
A package designed for string configuration and memory storage limitation. Place it in your compiler environment. The library file name is:

**sizeof_pkg.ego**

**How to import it?**

1. Import the package with the following command:

```python
from sizeof_pkg import *
```

2. Create the `pkg` object:

```python
pkg = variable_name;
```

3. Then, pass the variable as a default parameter in the language:

```python
public mutable str variable_name = "MY_TEXT";
```

If your variable exceeds 100 memory values, it will be reformatted to hold only the first 10 characters.

**Source code available in:**  
pkg_sizeof_str.EgoJIT




## Basic Syntax

### Comments

```
// This is a single-line comment

/* This is a
   multi-line comment */
```

### Variables

Variables in Ego must be declared with visibility, mutability, type, and name:

```
visibility mutability type name = value;
```

For example:
```
public mutable int counter = 0;
private immutable string name = "Ego";
protected const bool isEnabled = true;
```

#### Visibility Modifiers
- `public`: Accessible everywhere
- `private`: Limited to current scope
- `protected`: Limited to current scope and child scopes

#### Mutability Modifiers
- `mutable`: Can be changed after declaration
- `immutable`: Cannot be changed after declaration
- `const`: Cannot be changed (similar to immutable)

#### Data Types
- `int`: Integer values
- `float`: Floating-point values
- `string`: Text values
- `bool`: Boolean values (true/false)
- `list`: List of values
- `dict`: Dictionary/map of key-value pairs

### Control Structures

#### If Statements

```
if (condition) {
    // code to execute if condition is true
} else {
    // code to execute if condition is false
}
```

#### Loops

For loops:
```
for (initialization; condition; update) {
    // code to execute in loop
}
```

While loops:
```
while (condition) {
    // code to execute while condition is true
}
```

### Functions

Functions are declared with visibility, the `function` keyword, name, parameters, and body:

```
visibility function name(parameters) {
    // function body
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

## Examples

### Basic Variable Usage

```
public mutable int x = 10;
public immutable string greeting = "Hello";
print(x);
print(greeting);
```

### Using Conditions

```
public mutable int age = 18;

if (age >= 18) {
    print("Adult");
} else {
    print("Minor");
}
```

### Loop Example

```
public mutable int i = 0;
while (i < 5) {
    print(i);
    i = i + 1;
}
```

```
for (public mutable int j = 0; j < 5; j = j + 1) {
    print(j);
}
```

### Function Example

```
public function add(int a, int b) {
    return a + b;
}

public mutable int result = add(5, 3);
print(result);
```

## Error Handling

> The Ego compiler will generate errors for:

1. Attempting to modify an immutable variable
2. Using undefined variables
3. Invalid visibility or mutability modifiers
4. Invalid data types
5. Syntax errors in control structures or function declarations

Error messages will be included as comments in the generated Python code.

## Compilation Process

> The EgoJITCompiler processes Ego code in these steps:
1. Clean the source code (remove comments, normalize whitespace)
2. Split code into logical blocks
3. Translate each block into equivalent Python code
4. Track variables and their properties in scopes
5. Compile the generated Python code to bytecode

## Language Limitations

- No support for classes or object-oriented programming
- Limited data type operations
- No built-in exception handling
- Limited standard library

## Using the Compiler

1. Go to the `src/Ego_compiler` file and scroll to the end of the code.


2. Inside the ``sample_code`` instance, write your code.

Example:
```
sample_code = """

public mutable int x = 10;
print(x);

"""
```

3. In the function:

```compiler.compile(sample_code, 'output.ego')```

Set the output file name by replacing ``'output.ego'`` with the name you want for the compiled file.

Example:
```
compiler.compile(sample_code, 'my_file.ego')
```
##
>![](https://uxwing.com/wp-content/themes/uxwing/download/communication-chat-call/faqs-icon.png)
## Runtime Environment

> ⚠️ The compiled Ego programs run in Python's runtime environment, but maintain Ego's variable access and mutability rules through the generated code.
##
> Technologies that were used to develop the beta version (1.0 **beta**).

> ![Python](https://img.shields.io/badge/Python-14354C?style=flat-square&logo=python&logoColor=white) 
![OpenAI](https://img.shields.io/badge/OpenAI-412991?style=flat-square&logo=openai&logoColor=white) 
![Claude AI](https://img.shields.io/badge/Claude_AI-3E5E8A?style=flat-square&logo=anthropic&logoColor=white)
##

