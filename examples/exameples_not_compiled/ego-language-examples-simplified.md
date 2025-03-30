# Ego Language - Basic Examples

## 1. Variable Declaration and Types

### Complete Example
```
// Demonstrate all variable types with different visibilities and mutabilities

// Integer examples
public mutable int counter = 0;
private immutable int maxRetries = 5;
protected const int userId = 12345;

// Float examples
public mutable float price = 19.99;
private immutable float pi = 3.14159;
protected const float taxRate = 0.08;

// String examples
public mutable string message = "Hello, Ego!";
private immutable string appName = "EgoApp";
protected const string version = "1.0.0";

// Boolean examples
public mutable bool isActive = true;
private immutable bool isRequired = false;
protected const bool isProduction = true;

// List example
public mutable list numbers = [1, 2, 3, 4, 5];

// Dictionary example
public mutable dict userInfo = {"name": "John", "age": 30};

// Printing variables
print(counter);
print(price);
print(message);
print(isActive);
print(numbers);
print(userInfo);

// Modifying mutable variables
counter = counter + 1;
price = price * 1.1;
message = message + " Welcome!";
isActive = false;
numbers = [10, 20, 30];
userInfo = {"name": "Jane", "age": 25};

// Print modified values
print(counter);
print(price);
print(message);
print(isActive);
print(numbers);
print(userInfo);
```

## 2. Conditional Statements

### Complete Example
```
// Demonstrate if-else statements with different conditions

public mutable int score = 85;
public mutable string grade = "";

// Simple if-else
if (score >= 90) {
    grade = "A";
} else {
    grade = "B or below";
}
print(grade);

// Multiple conditions
if (score >= 90) {
    grade = "A";
} else if (score >= 80) {
    grade = "B";
} else if (score >= 70) {
    grade = "C";
} else if (score >= 60) {
    grade = "D";
} else {
    grade = "F";
}
print(grade);

// Nested if statements
public mutable bool isHonorsStudent = true;

if (score >= 80) {
    if (isHonorsStudent) {
        grade = grade + "+";
    }
}
print(grade);

// Logical operators in conditions
public mutable int attendance = 95;

if (score >= 80 && attendance >= 90) {
    print("Excellent student!");
} else if (score >= 80 || attendance >= 90) {
    print("Good student!");
} else {
    print("Needs improvement");
}
```

## 3. Loops

### Complete Example
```
// Demonstrate different types of loops

// While loop
public mutable int i = 0;
while (i < 5) {
    print(i);
    i = i + 1;
}

// For loop
for (public mutable int j = 0; j < 5; j = j + 1) {
    print(j);
}

// Nested loops
for (public mutable int x = 1; x <= 3; x = x + 1) {
    for (public mutable int y = 1; y <= 3; y = y + 1) {
        print(x * y);
    }
}

// Loop with conditional break
public mutable int k = 0;
while (k < 10) {
    if (k == 5) {
        print("Breaking at 5");
        k = 10; // Simulating a break
    } else {
        print(k);
        k = k + 1;
    }
}

// Loop with continue
for (public mutable int m = 0; m < 10; m = m + 1) {
    if (m % 2 == 0) {
        // Skip even numbers (simulating continue)
    } else {
        print(m); // Print only odd numbers
    }
}
```
