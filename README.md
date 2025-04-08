# EgoLang

![EgoLang Logo](ego.png)

A strongly-typed programming language with explicit control over visibility and mutability

[![EgoLang](https://img.shields.io/badge/EgoLang-%E2%9A%96%20Powered-FFD700?style=flat&logo=expensify&logoColor=00274D&labelColor=0057B7&color=00A4E0&borderRadius=50)](https://github.com/isamytanaka/EgoLang)
[![Version](https://img.shields.io/badge/Version-2.9.0-FF4500?style=flat&logo=v&logoColor=white&labelColor=FF7F50&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang)
[![License](https://img.shields.io/badge/License-MIT-9370DB?style=flat&logo=license&logoColor=white&labelColor=8A2BE2&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang/blob/main/LICENSE)
[![Python](https://img.shields.io/badge/Built_With-Python-4B8BBE?style=flat&logo=python&logoColor=white&labelColor=306998&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://www.python.org/)
[![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-brightgreen?style=flat&logo=github&logoColor=white&labelColor=3CB371&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang/pulls)
[![Documentation](https://img.shields.io/badge/Docs-Latest-FF8C00?style=flat&logo=read-the-docs&logoColor=white&labelColor=FF4500&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang/README.md)

<br>

[![Stars](https://img.shields.io/github/stars/isamytanaka/EgoLang?style=flat&logo=github&logoColor=white&label=Stars&color=FFD700&labelColor=FFA500&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang/stargazers)
[![Forks](https://img.shields.io/github/forks/isamytanaka/EgoLang?style=flat&logo=git&logoColor=white&label=Forks&color=32CD32&labelColor=228B22&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang/network/members)
[![Issues](https://img.shields.io/github/issues/isamytanaka/EgoLang?style=flat&logo=github&logoColor=white&label=Issues&color=FF6347&labelColor=FF4500&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang/issues)
[![Downloads](https://img.shields.io/github/downloads/isamytanaka/EgoLang/total?style=flat&logo=github&logoColor=white&label=Downloads&color=6A5ACD&labelColor=483D8B&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang/releases)
[![Created](https://img.shields.io/badge/Created-Mar%202025-9932CC?style=flat&logo=github&logoColor=white&labelColor=8B008B&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang)
[![Creator](https://img.shields.io/badge/Creator-isamytanaka-1E90FF?style=flat&logo=github&logoColor=white&labelColor=4169E1&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka)

## Table of Contents

- [Introduction](#introduction)
- [Key Features](#key-features)
- [Installation & Running](#installation--running)
- [Getting Started](#getting-started)
- [Language Fundamentals](#language-fundamentals)
  - [Storage Types](#storage-types)
  - [Lifecycle Modifiers](#lifecycle-modifiers)
  - [Data Qualifiers](#data-qualifiers)
  - [Symbol Binding and Transformation](#symbol-binding-and-transformation)
  - [Control Structures](#control-structures)
  - [Procedures](#procedures)
  - [Blocks](#blocks)
  - [Comments](#comments)
- [Examples](#examples)
- [Changelog](#changelog)
- [Contributing](#contributing)
- [License](#license)

## Introduction

**EgoLang** is a unique programming language that brings explicit control over symbol visibility, mutability, and lifecycle directly into the language syntax. By making these properties first-class citizens of the language, EgoLang helps developers write more maintainable code with fewer side effects and better memory management.

EgoLang translates to Python code, focusing on providing stronger guarantees about symbol visibility and mutability than traditional languages.

> **"Write once, understand forever."** — EgoLang Philosophy

## Key Features

🔒 **Explicit Control** - Every symbol declaration clearly defines its storage type, lifecycle, and data type

🔄 **Controlled Mutability** - Granular control over whether and how variables can change

🧩 **Domain Management** - Hierarchical scoping through domain blocks

⚡ **Python Interoperability** - Seamlessly compiles to Python

🛡️ **Strong Typing** - Type safety through qualifier system

🔎 **Clean Syntax** - Elegant, readable code with clear boundaries

## Installation & Running

**Note: Currently, EgoLang does not support installation via pip or command-line execution.**

To run EgoLang code, you need to:

1. Clone the repository
2. Open the compiler file at `src/compiler.py`
3. Locate the `sample_code` variable in the file
4. Replace its content with your EgoLang code
5. Run the compiler directly with Python:

```bash
python src/compiler.py
```

This will compile and execute your EgoLang code.

## Getting Started

Your first EgoLang program (place this in the `sample_code` variable):

```
-- hello_world.ego

persistent enduring textual greeting <- "Hello, EgoLang World!".

transient procedure sayHello[] {
    emit[greeting].
}

sayHello[].
```

## Language Fundamentals

EgoLang introduces three core concepts that make it unique:

### Storage Types

Storage types define how a symbol is stored in memory:

| Storage Type | Description |
|--------------|-------------|
| `transient`  | Temporary, local storage that exists only during execution scope |
| `persistent` | Stored in a way that persists between executions |
| `volatile`   | May change from external factors, no guarantees on value consistency |

### Lifecycle Modifiers

Lifecycle modifiers control how long a symbol exists and whether it can be modified:

| Lifecycle   | Description |
|-------------|-------------|
| `ephemeral` | Short-lived and mutable |
| `enduring`  | Long-lived and mutable |
| `permanent` | Long-lived and immutable after initialization |

### Data Qualifiers

Data qualifiers define what type of data a symbol can hold:

| Qualifier   | Description | Python Equivalent |
|-------------|-------------|-------------------|
| `numeric`   | Numbers     | `int`, `float`    |
| `logical`   | Boolean     | `bool`            |
| `textual`   | Strings     | `str`             |
| `composite` | Collections | `list`, `dict`, `tuple` |
| `abstract`  | Any type    | Any Python object |

### Symbol Binding and Transformation

Symbols are declared with their full specifications:

```
storage lifecycle qualifier identifier <- value.
```

For example:

```
transient ephemeral numeric counter <- 0.
volatile enduring composite data <- [1, 2, 3].
persistent permanent textual APP_NAME <- "EgoLang IDE".
```

Transformations (value changes) use the arrow operator:

```
counter <- counter + 1.
```

### Control Structures

**Branches (Conditionals)**:

```
when [condition] {
    // code if condition is true
} otherwise {
    // code if condition is false
}
```

**Iterations**:

```
// Traditional loop
iterate [initialization; condition; update] {
    // code
}

// For-each loop
iterate [element over collection] {
    // code
}

// While loop
while [condition] {
    // code
}
```

### Procedures

Procedures are EgoLang's functions:

```
transient procedure calculateArea[numeric width, numeric height]: numeric {
    transient ephemeral numeric area <- width * height.
    yield area.
}
```

Invoking a procedure:

```
transient ephemeral numeric result <- calculateArea[5, 10].
```

### Blocks

Blocks create scoped domains:

```
block Calculator {
    transient permanent numeric PI <- 3.14159.
    
    transient procedure circleArea[numeric radius]: numeric {
        transient ephemeral numeric area <- PI * radius * radius.
        yield area.
    }
}
```

### Comments

```
-- This is a single line comment

/- 
   This is a 
   multi-line comment
-/
```

## Examples

### Example 1: Temperature Converter

```
block TemperatureConverter {
    transient procedure celsiusToFahrenheit[numeric celsius]: numeric {
        transient ephemeral numeric fahrenheit <- (celsius * 9/5) + 32.
        yield fahrenheit.
    }
    
    transient procedure fahrenheitToCelsius[numeric fahrenheit]: numeric {
        transient ephemeral numeric celsius <- (fahrenheit - 32) * 5/9.
        yield celsius.
    }
}

transient ephemeral numeric tempC <- 25.
transient ephemeral numeric tempF <- TemperatureConverter.celsiusToFahrenheit[tempC].

emit["Temperature in Fahrenheit:", tempF].
```

### Example 2: Simple Todo List

```
persistent enduring composite todos <- [].

transient procedure addTodo[textual item] {
    todos <- todos + [item].
}

transient procedure displayTodos[] {
    emit["Todo List:"].
    
    when [length[todos] == 0] {
        emit["  No items in the list."].
    } otherwise {
        iterate [item over todos] {
            emit["  -", item].
        }
    }
}

addTodo["Learn EgoLang"].
addTodo["Write a program"].
addTodo["Share with friends"].

displayTodos[].
```

## Changelog

### EgoLang 2.9.0 (Current Version)

**Major Changes:**

1. **Removed Functional Programming Features:**
   - Functional programming paradigm has been removed due to critical bugs during Python conversion
   - Function as first-class values caused significant stability issues

2. **Removed Object-Oriented Programming Features:**
   - Object-oriented programming constructs have been removed
   - The translation to Python was unstable and introduced difficult-to-trace errors

3. **Enhanced Focus on Security and Control:**
   - Language now prioritizes code safety and predictability
   - More restrictive but more robust compiler
   - Improved handling to prevent ambiguity and vulnerabilities
   - Intentionally more rigid design for better security guarantees

The language has been simplified to focus on its core strengths of explicit control over visibility, mutability, and lifecycle management.

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

This project is licensed under the MIT License - see the LICENSE file for details.

---

Made with ❤️ by [Isamy Tanaka](https://github.com/isamytanaka)

[![Follow on GitHub](https://img.shields.io/github/followers/isamytanaka?style=flat&logo=github&logoColor=white&label=Follow&color=1E90FF&labelColor=4169E1&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka)
