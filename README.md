# EgoLang

<div align="center">

![EgoLang Logo](ego.png)

A programming language with explicit control over context and mutability

[![EgoLang](https://img.shields.io/badge/EgoLang-%E2%9A%96%20Powered-FFD700?style=flat&logo=expensify&logoColor=00274D&labelColor=0057B7&color=00A4E0&borderRadius=50)](https://github.com/isamytanaka/EgoLang)
[![Version](https://img.shields.io/badge/Version-2.10.1-FF4500?style=flat&logo=v&logoColor=white&labelColor=FF7F50&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang)
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

<br>

[![Release Date](https://img.shields.io/badge/Latest_Release-April_2025-E91E63?style=flat&logo=github&logoColor=white&labelColor=C2185B&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang/releases)
[![Code Size](https://img.shields.io/github/languages/code-size/isamytanaka/EgoLang?style=flat&logo=github&logoColor=white&label=Code%20Size&color=00BCD4&labelColor=0097A7&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang)
[![Repo Size](https://img.shields.io/github/repo-size/isamytanaka/EgoLang?style=flat&logo=github&logoColor=white&label=Repo%20Size&color=009688&labelColor=00796B&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang)
[![Lines of Code](https://img.shields.io/tokei/lines/github/isamytanaka/EgoLang?style=flat&logo=github&logoColor=white&label=Lines&color=CDDC39&labelColor=AFB42B&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang)
[![Test Coverage](https://img.shields.io/badge/Test_Coverage-92%25-4CAF50?style=flat&logo=pytest&logoColor=white&labelColor=388E3C&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang/actions)
[![Build Status](https://img.shields.io/github/workflow/status/isamytanaka/EgoLang/CI?style=flat&logo=github-actions&logoColor=white&label=Build&color=03A9F4&labelColor=0288D1&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka/EgoLang/actions)

</div>

## 📚 Table of Contents

- [Overview](#-overview)
- [Quick Start Guide](#-quick-start-guide)
- [Key Features](#-key-features)
- [Installation Instructions](#-installation-instructions)
- [Language Basics](#-language-basics)
- [Advanced Topics](#-advanced-topics)
- [Version History](#-version-history)
- [Troubleshooting](#-troubleshooting)
- [Contributing](#-contributing)
- [License](#-license)

## 🔍 Overview

EgoLang is a programming language designed with a focus on code clarity, data integrity, and explicit intent. The language has evolved significantly in version 2.10.1, shifting from the strongly-typed paradigm toward a more context-aware approach with simplified syntax while retaining explicit declarations for variable mutability.

The core philosophy of EgoLang centers around making code behavior more intuitive and accessible, while still maintaining predictability and eliminating ambiguities that often lead to bugs in less strict languages. Every declaration clearly communicates the intended mutability and context, reducing cognitive load during code review and maintenance.

## 🚀 Quick Start Guide

Want to try EgoLang right away? Here's a simple "Hello World" program to get you started:

1. Create a file named `hello.ego` with the following content:

```
fluid greeting is "Hello, EgoLang World!".
say(greeting).
```

That's it! You've just written and executed your first EgoLang program.

## ✨ Key Features

| Feature | Description |
|---------|-------------|
| **Context-Aware Syntax** | Variables are declared within their intended context ("fluid" or "rigid") |
| **Simplified Declaration** | Clean, intuitive syntax with period-terminated statements |
| **Explicit Mutability** | Variables must be declared as either `fluid` (mutable) or `rigid` (immutable) |
| **Python Bytecode Compilation** | Compiles to optimized Python bytecode for good performance |
| **Comprehensive Error Detection** | Thorough static analysis catches potential issues before execution |
| **Natural Language Control Flow** | Control structures that read more like natural language |

## 📥 Installation Instructions

### Prerequisites

- Python 3.8 or higher
- 64-bit operating system

### Step-by-Step Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/isamytanaka/EgoLang.git
   cd EgoLang/src
   ```

2. **Install required dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

## 📖 Language Basics

### Variable Declaration

In EgoLang, all variables must be declared with explicit mutability:

- **Fluid** variables can be changed after declaration:
  ```
  fluid counter is 10.
  counter becomes counter + 1.  // Now counter is 11
  ```

- **Rigid** variables cannot be changed after declaration:
  ```
  rigid PI is 3.14159.
  // PI becomes 3.14.  // This would cause an error!
  ```

### Basic Operations

#### Arithmetic

```
fluid a is 5.
fluid b is 10.
fluid sum is a + b.
fluid product is a * b.
fluid quotient is b / a.
fluid difference is b - a.
```

#### String Manipulation

```
fluid greeting is "Hello".
fluid name is "EgoLang".
fluid message is greeting + ", " + name + "!".
say(message).  // Outputs: Hello, EgoLang!
```

#### Boolean Logic

```
fluid is_enabled is True.
fluid is_valid is False.

when (is_enabled and not is_valid) {
    say("Enabled but not valid").
}.
```

### Control Structures

#### Conditionals

```
fluid temperature is 22.

when (temperature > 30) {
    say("It's hot!").
} otherwise {
    say("It's not hot.").
}.
```

#### Counting Loop

```
fluid count is 1.
rigid max is 5.

when (count <= max) {
    say("Count:", count).
    count becomes count + 1.
}.
```

### Functions

EgoLang uses the `execute` keyword to call functions:

```
// Get input from user
fluid name is execute input_value with ("Enter your name: ").
say("Hello,", name).

// Convert string to number
fluid number_text is "42".
fluid actual_number is execute to_number with (number_text).
say(actual_number + 8).  // Outputs: 50
```

## 🔧 Advanced Topics

### Type Conversion

EgoLang provides built-in functions for type conversion:

```
fluid text is "123.45".
fluid number is execute to_number with (text).       // Convert to integer
fluid decimal is execute to_decimal with (text).     // Convert to float
fluid string_again is execute to_text with (decimal). // Convert back to string
```

### Nested Conditionals

```
fluid age is 25.
fluid has_license is True.

when (age >= 18) {
    when (has_license) {
        say("Can drive").
    } otherwise {
        say("Cannot drive, no license").
    }.
} otherwise {
    say("Too young to drive").
}.
```

### Working with Lists (Upcoming Feature)

```
// Note: Array support is coming in the next update
fluid names is ["Alice", "Bob", "Charlie"].
fluid count is execute length with (names).
say("There are", count, "names in the list").
```

## 📝 Complete Example Program

Here's a more comprehensive example showing various EgoLang features:

```
// Temperature converter program
fluid celsius is execute input_value with ("Enter temperature in Celsius: ").
fluid celsius_num is execute to_number with (celsius).

// Convert to Fahrenheit
fluid fahrenheit is (celsius_num * 9/5) + 32.

// Display results
say("Temperature conversion:").
say(celsius, "°C =", fahrenheit, "°F").

// Provide weather description
when (celsius_num <= 0) {
    say("It's freezing!").
} otherwise {
    when (celsius_num < 20) {
        say("It's cool.").
    } otherwise {
        when (celsius_num < 30) {
            say("It's warm.").
        } otherwise {
            say("It's hot!").
        }.
    }.
}.

say("Program complete.").
```

### Using the API in Python

```python
from ego_compiler import EgoCompiler

# Create compiler instance
compiler = EgoCompiler()

# EgoLang code
code = """
fluid greeting is "Hello, programmatic EgoLang!".
say(greeting).
"""

# Compile to a .ego file
compiler.compile(code, 'my_program.ego')

# To run, use:
# python -m my_program
```

### Debug Mode

Enable debug mode for additional checks and more detailed error messages:

```python
compiler = EgoCompiler(debug=True)
```

## 📜 Version History

### Accurate Release Timeline

| Version | Release Date | Key Features & Changes |
|---------|--------------|--------------|
| **2.10.1** | April 2025 | • First stable release in the 2.10.x series<br>• Bug fixes in statement parsing<br>• Improved error reporting<br>• Enhanced compiler stability<br>• Fixed issues with nested blocks<br>• Optimized bytecode generation |
| **2.9.0** | March 2025 | • Public release (later discontinued)<br>• Experimental syntax changes<br>• Critical security issues in Python transpilation<br>• Runtime performance problems |
| **2.8.0** | March 2025 | • Python integration with `@py:` directive<br>• OOP support with classes and inheritance<br>• Iterator-style for loops<br>• Return type annotations<br>• Logical operators<br>• Improved error reporting |
| **2.7.9** | March 2025 | • Initial public release<br>• Strong typing system<br>• Visibility and mutability control<br>• JIT compilation to Python bytecode |

### Development Path Clarification

After releasing version 2.9.0, which had significant issues, development returned to the stable 2.8.0 codebase. Version 2.10.0 was developed internally but never publicly released. Instead, version 2.10.1 was released as the new stable version, incorporating lessons learned from the problematic 2.9.0 release.

## ❓ Troubleshooting

### Common Errors and Solutions

| Error | Possible Cause | Solution |
|-------|---------------|----------|
| `Cannot redeclare rigid variable` | Attempting to modify a rigid variable | Either use a fluid variable or create a new variable with a different name |
| `Variable has not been declared` | Using a variable before declaring it | Declare the variable with `fluid` or `rigid` before using it |
| `Invalid when statement syntax` | Incorrect conditional structure | Ensure your when statements have proper parentheses and braces |
| `Invalid say statement` | Wrong format for output | Check that your say statement has proper parentheses |
| `Compilation failed` | Syntax error in EgoLang code | Check your code for missing periods or incorrect syntax |

### FAQ

**Q: Why am I getting bytecode compilation errors?**
A: Ensure you have Python 3.8+ installed and that your EgoLang syntax is correct.

**Q: Can I mix EgoLang with regular Python code?**
A: Direct Python integration was available in 2.8 but was removed in 2.10.1. You can call Python functions through the standard library interface.

**Q: Where are comments in EgoLang?**
A: Use `//` for single-line comments. Multi-line comments will be added in a future update.

**Q: My program compiles but doesn't run correctly. What should I do?**
A: Try enabling debug mode in the compiler to get more detailed error information.

## 👥 Contributing

Contributions to EgoLang are welcome! Here's how you can contribute:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Contribution Guidelines

- Include tests for new features
- Update documentation for any changes
- Follow the existing code style
- Add examples for new functionality

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](https://github.com/isamytanaka/EgoLang/blob/main/LICENSE) file for details.

---

<div align="center">

Made with ❤️ by [Isamy Tanaka](https://github.com/isamytanaka)

[![Follow on GitHub](https://img.shields.io/github/followers/isamytanaka?style=flat&logo=github&logoColor=white&label=Follow&color=1E90FF&labelColor=4169E1&fontFamily=Verdana&fontWeight=bold&borderRadius=20)](https://github.com/isamytanaka)

</div>
