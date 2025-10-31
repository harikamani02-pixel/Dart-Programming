# Dart Programming Language 

## Dart Modules
1. [Introduction and Basics](#1-introduction-and-basics)
2. [Conditions and Loops](#2-conditions-and-loops)
3. [Functions in Dart](#3-functions-in-dart)
4. [Collections in Dart](#4-collections-in-dart)
5. [File Handling in Dart](#5-file-handling-in-dart)
6. [OOP in Dart](#6-oop-in-dart)
7. [Null Safety In Dart](#7-Null-Safety-In-Dart)


## 1. Introduction and Basics
Dart is a programming language developed by Google. It is mainly used for building mobile apps (Android & iOS), web apps, desktop apps, and especially Flutter applications. Dart is object-oriented, easy to learn, and supports both ahead-of-time (AOT) and just-in-time (JIT) compilation, making it fast and efficient for UI development.


### 10 Examples of Dart Basics

#### Example 1: Print Hello World
```dart
void main() {
  print('Hello, World!');
}
```

**Output:**
```
Hello, World!
```
### Example 2:Variables 
```dart
void main() {
  int age = 23;
  String name = "Manikanta";
  print("My name is $name and I am $age years old.");
}
```

**Output:**
```
My name is Manikanta and I am 23 years old.
```
### Example 3: Arithmetic Operations
```dart
void main() {
  int a = 10, b = 3;
  print(a + b);
  print(a - b);
  print(a * b);
  print(a / b);
}
```

**Output:**
```
13
7
30
3.3333333333333335
```

### Example 4: If-Else
```dart
void main() {
  int number = 7;
  if (number % 2 == 0) {
    print("Even number");
  } else {
    print("Odd number");
  }
}
```
**output:**
```
Odd number
```

### Example 5: For Loop
```dart
void main() {
  for (int i = 1; i <= 5; i++) {
    print(i);
  }
}
```
**output:**
```
1
2
3
4
5
```

### Example 6: While Loop
```dart
void main() {
  int i = 1;
  while (i <= 3) {
    print("Hello $i");
    i++;
  }
}
```
**output:**
```
Hello 1
Hello 2
Hello 3
```

### Example 7: Function Example
```dart
void main() {
  print(add(5, 3));
}

int add(int a, int b) {
  return a + b;
}
```
**output:**
```
8
```

### Example 8: List Example
```dart
void main() {
  List<String> fruits = ["Apple", "Banana", "Mango"];
  print(fruits);
}
```
**output:**
```
[Apple, Banana, Mango]
```

### Example 9: Map Example
```dart
void main() {
  Map<String, String> student = {"name": "Alice", "age": "20"};
  print(student["name"]);
}
```
**output:**
```
Alice
```

### Example 10: Class and Object
```dart
class Person {
  String name = "Sam";
  int age = 22;

  void display() {
    print("Name: $name, Age: $age");
  }
}

void main() {
  Person p = Person();
  p.display();
}
```
**output:**
```
Name: Sam, Age: 22
```

## 2. Conditions and Loops

### Overview
Conditions and loops are fundamental concepts in programming used to control the flow of a program.

### 10 Examples of Conditions and Loops

#### Example 1: Basic If-Else Statement
```dart
void main() {
  int age = 18;
  
  if (age >= 18) {
    print('You are an adult.');
  } else {
    print('You are a minor.');
  }
}
```

**Output:**
```
You are an adult.
```

#### Example 2: If-Else If-Else Chain
```dart
void main() {
  int score = 85;
  
  if (score >= 90) {
    print('Grade: A');
  } else if (score >= 80) {
    print('Grade: B');
  } else if (score >= 70) {
    print('Grade: C');
  } else if (score >= 60) {
    print('Grade: D');
  } else {
    print('Grade: F');
  }
}
```

**Output:**
```
Grade: B
```

#### Example 3: Ternary Operator
```dart
void main() {
  int temperature = 25;
  
  // Using ternary operator
  String weather = temperature > 20 ? 'Hot' : 'Cold';
  print('Weather: $weather');
  
  // Nested ternary
  String season = temperature > 30 ? 'Summer' : 
                  temperature > 20 ? 'Spring' : 
                  temperature > 10 ? 'Autumn' : 'Winter';
  print('Season: $season');
}
```

**Output:**
```
Weather: Hot
Season: Spring
```

#### Example 4: Switch Statement
```dart
void main() {
  String day = 'Monday';
  
  switch (day) {
    case 'Monday':
      print('Start of work week');
      break;
    case 'Tuesday':
    case 'Wednesday':
    case 'Thursday':
      print('Mid week');
      break;
    case 'Friday':
      print('TGIF!');
      break;
    case 'Saturday':
    case 'Sunday':
      print('Weekend!');
      break;
    default:
      print('Invalid day');
  }
}
```

**Output:**
```
Start of work week
```

#### Example 5: Switch Expression (Dart 3.0+)
```dart
void main() {
  String day = 'Friday';
  
  String message = switch (day) {
    'Monday' => 'Start of work week',
    'Tuesday' || 'Wednesday' || 'Thursday' => 'Mid week',
    'Friday' => 'TGIF!',
    'Saturday' || 'Sunday' => 'Weekend!',
    _ => 'Invalid day'
  };
  
  print(message);
}
```

**Output:**
```
TGIF!
```

#### Example 6: For Loop
```dart
void main() {
  // Basic for loop
  print('Numbers 1 to 5:');
  for (int i = 1; i <= 5; i++) {
    print(i);
  }
  
  // For loop with step
  print('\nEven numbers 0 to 10:');
  for (int i = 0; i <= 10; i += 2) {
    print(i);
  }
  
  // Reverse for loop
  print('\nCountdown from 5:');
  for (int i = 5; i >= 1; i--) {
    print(i);
  }
}
```

**Output:**
```
Numbers 1 to 5:
1
2
3
4
5

Even numbers 0 to 10:
0
2
4
6
8
10

Countdown from 5:
5
4
3
2
1
```

#### Example 7: For-In Loop
```dart
void main() {
  List<String> fruits = ['apple', 'banana', 'orange', 'grape'];
  
  // For-in loop with list
  print('Fruits:');
  for (String fruit in fruits) {
    print(fruit);
  }
  
  // For-in loop with string
  String word = 'Dart';
  print('\nLetters in "Dart":');
  for (String letter in word.split('')) {
    print(letter);
  }
  
  // For-in loop with range
  print('\nNumbers 1 to 5:');
  for (int number in List.generate(5, (index) => index + 1)) {
    print(number);
  }
}
```

**Output:**
```
Fruits:
apple
banana
orange
grape

Letters in "Dart":
D
a
r
t

Numbers 1 to 5:
1
2
3
4
5
```

#### Example 8: While Loop
```dart
void main() {
  int count = 0;
  
  // Basic while loop
  print('While loop - counting to 5:');
  while (count < 5) {
    print(count);
    count++;
  }
  
  // While loop with condition
  int number = 10;
  print('\nHalving 10 until it reaches 1:');
  while (number > 1) {
    print(number);
    number ~/= 2; // Integer division
  }
  print(number); // Print the final 1
}
```

**Output:**
```
While loop - counting to 5:
0
1
2
3
4

Halving 10 until it reaches 1:
10
5
2
1
```

#### Example 9: Do-While Loop
```dart
void main() {
  int count = 0;
  
  // Do-while loop (executes at least once)
  print('Do-while loop:');
  do {
    print('Count: $count');
    count++;
  } while (count < 3);
  
  // Do-while with false condition (still executes once)
  print('\nDo-while with false condition:');
  do {
    print('This will print once');
  } while (false);
}
```

**Output:**
```
Do-while loop:
Count: 0
Count: 1
Count: 2

Do-while with false condition:
This will print once
```

#### Example 10: Break and Continue
```dart
void main() {
  // Break example - exit loop early
  print('Numbers 1 to 10, stopping at 5:');
  for (int i = 1; i <= 10; i++) {
    if (i == 6) {
      break; // Exit the loop
    }
    print(i);
  }
  
  // Continue example - skip current iteration
  print('\nEven numbers 1 to 10:');
  for (int i = 1; i <= 10; i++) {
    if (i % 2 != 0) {
      continue; // Skip odd numbers
    }
    print(i);
  }
  
  // Nested loops with labels
  print('\nNested loops with break:');
  outerLoop: for (int i = 1; i <= 3; i++) {
    for (int j = 1; j <= 3; j++) {
      if (i == 2 && j == 2) {
        break outerLoop; // Break outer loop
      }
      print('i: $i, j: $j');
    }
  }
}
```

**Output:**
```
Numbers 1 to 10, stopping at 5:
1
2
3
4
5

Even numbers 1 to 10:
2
4
6
8
10

Nested loops with break:
i: 1, j: 1
i: 1, j: 2
i: 1, j: 3
i: 2, j: 1
```
## 3. Functions in Dart

### Overview
Functions in Dart are blocks of code that perform a specific task. You write a function once, and you can use (call) it multiple times in your program. Functions help you organize code, reduce repetition, and improve readability.

### Why We Use Functions
- **Reuse Code**
- **Break complex problems into small parts**
- **Improve code structure**
- **Make debugging easier**


### 10 Examples of Functions in Dart

#### Example 1: Basic Function
```dart
// Function declaration
void greet() {
  print('Hello, World!');
}

// Function with parameters
void greetPerson(String name) {
  print('Hello, $name!');
}

// Function with return value
int add(int a, int b) {
  return a + b;
}

void main() {
  greet();
  greetPerson('Alice');
  int result = add(5, 3);
  print('Sum: $result');
}
```

**Output:**
```
Hello, World!
Hello, Alice!
Sum: 8
```

#### Example 2: Function with Optional Parameters
```dart
// Optional positional parameters
void greetWithOptional(String name, [String? title, int? age]) {
  String message = 'Hello, $name';
  if (title != null) message += ' $title';
  if (age != null) message += ' (age: $age)';
  print(message);
}

// Optional named parameters
void createUser({required String name, String? email, int? age}) {
  print('User: $name');
  if (email != null) print('Email: $email');
  if (age != null) print('Age: $age');
}

void main() {
  greetWithOptional('John');
  greetWithOptional('Jane', 'Dr.');
  greetWithOptional('Bob', 'Mr.', 30);
  
  createUser(name: 'Alice');
  createUser(name: 'Bob', email: 'bob@example.com');
  createUser(name: 'Charlie', email: 'charlie@example.com', age: 25);
}
```

**Output:**
```
Hello, John
Hello, Jane Dr.
Hello, Bob Mr. (age: 30)
User: Alice
User: Bob
Email: bob@example.com
User: Charlie
Email: charlie@example.com
Age: 25
```

#### Example 3: Function with Default Values
```dart
// Default values for optional parameters
void greetWithDefaults(String name, [String title = 'Mr./Ms.', int age = 0]) {
  print('Hello, $title $name');
  if (age > 0) print('Age: $age');
}

// Default values for named parameters
void createProfile({required String name, String role = 'User', bool isActive = true}) {
  print('Name: $name');
  print('Role: $role');
  print('Active: $isActive');
}

void main() {
  greetWithDefaults('Alice');
  greetWithDefaults('Bob', 'Dr.', 30);
  
  createProfile(name: 'John');
  createProfile(name: 'Jane', role: 'Admin');
  createProfile(name: 'Charlie', role: 'Moderator', isActive: false);
}
```

**Output:**
```
Hello, Mr./Ms. Alice
Hello, Dr. Bob
Age: 30
Name: John
Role: User
Active: true
Name: Jane
Role: Admin
Active: true
Name: Charlie
Role: Moderator
Active: false
```

#### Example 4: Arrow Functions (Single Expression)
```dart
// Arrow function syntax
int multiply(int a, int b) => a * b;

// Arrow function with conditional
String getGrade(int score) => score >= 90 ? 'A' : 
                             score >= 80 ? 'B' : 
                             score >= 70 ? 'C' : 'F';

// Arrow function with null safety
String? getName(Map<String, dynamic> data) => data['name'] as String?;

void main() {
  print('Product: ${multiply(4, 5)}');
  print('Grade: ${getGrade(85)}');
  
  Map<String, dynamic> user = {'name': 'Alice', 'age': 25};
  print('Name: ${getName(user)}');
}
```

**Output:**
```
Product: 20
Grade: B
Name: Alice
```

#### Example 5: Anonymous Functions
```dart
void main() {
  // Anonymous function assigned to variable
  var greet = (String name) {
    print('Hello, $name!');
  };
  
  greet('Alice');
  
  // Anonymous function as parameter
  List<String> names = ['Alice', 'Bob', 'Charlie'];
  names.forEach((name) {
    print('Greeting $name');
  });
  
  // Anonymous function with return value
  var square = (int x) => x * x;
  print('Square of 5: ${square(5)}');
}
```

**Output:**
```
Hello, Alice!
Greeting Alice
Greeting Bob
Greeting Charlie
Square of 5: 25
```

#### Example 6: Higher-Order Functions
```dart
// Function that takes another function as parameter
void processNumbers(List<int> numbers, Function(int) processor) {
  for (int number in numbers) {
    processor(number);
  }
}

// Function that returns a function
Function createMultiplier(int factor) {
  return (int number) => number * factor;
}

// Function that takes and returns functions
Function compose(Function f, Function g) {
  return (x) => f(g(x));
}

void main() {
  List<int> numbers = [1, 2, 3, 4, 5];
  
  // Using processNumbers with anonymous function
  processNumbers(numbers, (n) => print('Number: $n'));
  
  // Using processNumbers with arrow function
  processNumbers(numbers, (n) => print('Square: ${n * n}'));
  
  // Using createMultiplier
  var doubleIt = createMultiplier(2);
  var tripleIt = createMultiplier(3);
  
  print('Double 5: ${doubleIt(5)}');
  print('Triple 5: ${tripleIt(5)}');
  
  // Using compose
  var addOne = (int x) => x + 1;
  var multiplyByTwo = (int x) => x * 2;
  var addOneThenDouble = compose(multiplyByTwo, addOne);
  
  print('Add 1 then double 3: ${addOneThenDouble(3)}');
}
```

**Output:**
```
Number: 1
Number: 2
Number: 3
Number: 4
Number: 5
Square: 1
Square: 4
Square: 9
Square: 16
Square: 25
Double 5: 10
Triple 5: 15
Add 1 then double 3: 8
```

#### Example 7: Recursive Functions
```dart
// Recursive function to calculate factorial
int factorial(int n) {
  if (n <= 1) {
    return 1;
  }
  return n * factorial(n - 1);
}

// Recursive function to calculate Fibonacci
int fibonacci(int n) {
  if (n <= 1) {
    return n;
  }
  return fibonacci(n - 1) + fibonacci(n - 2);
}

// Recursive function to reverse a string
String reverseString(String str) {
  if (str.isEmpty) {
    return str;
  }
  return str[str.length - 1] + reverseString(str.substring(0, str.length - 1));
}

void main() {
  print('Factorial of 5: ${factorial(5)}');
  print('Fibonacci sequence:');
  for (int i = 0; i < 10; i++) {
    print('F($i) = ${fibonacci(i)}');
  }
  print('Reverse of "Dart": ${reverseString("Dart")}');
}
```

**Output:**
```
Factorial of 5: 120
Fibonacci sequence:
F(0) = 0
F(1) = 1
F(2) = 1
F(3) = 2
F(4) = 3
F(5) = 5
F(6) = 8
F(7) = 13
F(8) = 21
F(9) = 34
Reverse of "Dart": traD
```

#### Example 8: Function Overloading (Using Optional Parameters)
```dart
// Dart doesn't support traditional overloading, but we can use optional parameters
class Calculator {
  // Single method with optional parameters
  int add(int a, [int? b, int? c]) {
    int result = a;
    if (b != null) result += b;
    if (c != null) result += c;
    return result;
  }
  
  // Alternative using named parameters
  double calculate({required String operation, required List<double> numbers}) {
    switch (operation) {
      case 'sum':
        return numbers.fold(0.0, (sum, num) => sum + num);
      case 'product':
        return numbers.fold(1.0, (product, num) => product * num);
      case 'average':
        return numbers.fold(0.0, (sum, num) => sum + num) / numbers.length;
      default:
        throw ArgumentError('Unknown operation: $operation');
    }
  }
}

void main() {
  Calculator calc = Calculator();
  
  print('Add 5: ${calc.add(5)}');
  print('Add 5 + 3: ${calc.add(5, 3)}');
  print('Add 5 + 3 + 2: ${calc.add(5, 3, 2)}');
  
  print('Sum: ${calc.calculate(operation: 'sum', numbers: [1, 2, 3, 4, 5])}');
  print('Product: ${calc.calculate(operation: 'product', numbers: [1, 2, 3, 4])}');
  print('Average: ${calc.calculate(operation: 'average', numbers: [1, 2, 3, 4, 5])}');
}
```

**Output:**
```
Add 5: 5
Add 5 + 3: 8
Add 5 + 3 + 2: 10
Sum: 15.0
Product: 24.0
Average: 3.0
```

#### Example 9: Function as First-Class Citizens
```dart
void main() {
  // Functions can be assigned to variables
  Function operation = add;
  print('5 + 3 = ${operation(5, 3)}');
  
  // Functions can be passed as arguments
  int result = calculate(10, 20, multiply);
  print('10 * 20 = $result');
  
  // Functions can be returned from functions
  Function getOperation(String op) {
    switch (op) {
      case 'add':
        return add;
      case 'subtract':
        return subtract;
      case 'multiply':
        return multiply;
      case 'divide':
        return divide;
      default:
        return add;
    }
  }
  
  Function op = getOperation('multiply');
  print('7 * 8 = ${op(7, 8)}');
  
  // Functions can be stored in collections
  List<Function> operations = [add, subtract, multiply, divide];
  List<String> opNames = ['Add', 'Subtract', 'Multiply', 'Divide'];
  
  for (int i = 0; i < operations.length; i++) {
    print('${opNames[i]}: ${operations[i](10, 5)}');
  }
}

int add(int a, int b) => a + b;
int subtract(int a, int b) => a - b;
int multiply(int a, int b) => a * b;
double divide(int a, int b) => a / b;

int calculate(int a, int b, Function operation) {
  return operation(a, b);
}
```

**Output:**
```
5 + 3 = 8
10 * 20 = 200
7 * 8 = 56
Add: 15
Subtract: 5
Multiply: 50
Divide: 2.0
```

#### Example 10: Async Functions
```dart
import 'dart:async';

// Future-returning function
Future<String> fetchData() async {
  // Simulate network delay
  await Future.delayed(Duration(seconds: 2));
  return 'Data fetched successfully!';
}

// Stream-returning function
Stream<int> countStream() async* {
  for (int i = 1; i <= 5; i++) {
    await Future.delayed(Duration(seconds: 1));
    yield i;
  }
}

// Function that handles async operations
Future<void> processData() async {
  try {
    print('Starting data fetch...');
    String data = await fetchData();
    print(data);
    
    print('Starting count stream...');
    await for (int count in countStream()) {
      print('Count: $count');
    }
  } catch (e) {
    print('Error: $e');
  }
}

void main() async {
  await processData();
  print('All operations completed!');
}
```

**Output:**
```
Starting data fetch...
Data fetched successfully!
Starting count stream...
Count: 1
Count: 2
Count: 3
Count: 4
Count: 5
All operations completed!
```
## 4. Collections in Dart

### Overview
Collections in Dart are data structures that hold multiple values. Dart provides several built-in collection types: List, Set, Map, and Queue.

 - **List – Ordered collection of items**
 - **Set – Unordered collection of unique items**
 - **Map – Collection of key-value pairs**

### 10 Examples of Collections in Dart

#### Example 1: List Basics
```dart
void main() {
  // Creating lists
  List<int> numbers = [1, 2, 3, 4, 5];
  List<String> fruits = ['apple', 'banana', 'orange'];
  var mixed = [1, 'hello', 3.14, true]; // List<dynamic>
  
  // Accessing elements
  print('First number: ${numbers[0]}');
  print('Last fruit: ${fruits[fruits.length - 1]}');
  
  // Modifying lists
  numbers.add(6);
  numbers.insert(0, 0);
  numbers.remove(3);
  
  print('Numbers: $numbers');
  print('Fruits: $fruits');
  print('Mixed: $mixed');
}
```

**Output:**
```
First number: 1
Last fruit: orange
Numbers: [0, 1, 2, 4, 5, 6]
Fruits: [apple, banana, orange]
Mixed: [1, hello, 3.14, true]
```

#### Example 2: List Methods and Operations
```dart
void main() {
  List<int> numbers = [3, 1, 4, 1, 5, 9, 2, 6];
  
  // Basic operations
  print('Length: ${numbers.length}');
  print('Is empty: ${numbers.isEmpty}');
  print('Is not empty: ${numbers.isNotEmpty}');
  print('First element: ${numbers.first}');
  print('Last element: ${numbers.last}');
  
  // Searching
  print('Contains 5: ${numbers.contains(5)}');
  print('Index of 4: ${numbers.indexOf(4)}');
  print('Last index of 1: ${numbers.lastIndexOf(1)}');
  
  // Sorting
  List<int> sorted = List.from(numbers);
  sorted.sort();
  print('Sorted: $sorted');
  
  // Reversing
  List<int> reversed = List.from(numbers);
  reversed.reversed.toList();
  print('Reversed: ${reversed.reversed.toList()}');
  
  // Filtering
  List<int> evenNumbers = numbers.where((n) => n % 2 == 0).toList();
  print('Even numbers: $evenNumbers');
}
```

**Output:**
```
Length: 8
Is empty: false
Is not empty: true
First element: 3
Last element: 6
Contains 5: true
Index of 4: 2
Last index of 1: 3
Sorted: [1, 1, 2, 3, 4, 5, 6, 9]
Reversed: [6, 2, 9, 5, 1, 4, 1, 3]
Even numbers: [4, 2, 6]
```

#### Example 3: Set Basics
```dart
void main() {
  // Creating sets
  Set<String> colors = {'red', 'green', 'blue'};
  Set<int> numbers = {1, 2, 3, 4, 5};
  var emptySet = <String>{}; // Empty set
  
  // Adding elements
  colors.add('yellow');
  colors.addAll(['purple', 'orange']);
  
  // Removing elements
  colors.remove('red');
  colors.removeAll(['green', 'blue']);
  
  print('Colors: $colors');
  print('Numbers: $numbers');
  
  // Set operations
  Set<int> set1 = {1, 2, 3, 4, 5};
  Set<int> set2 = {4, 5, 6, 7, 8};
  
  print('Union: ${set1.union(set2)}');
  print('Intersection: ${set1.intersection(set2)}');
  print('Difference: ${set1.difference(set2)}');
  print('Contains all: ${set1.containsAll([1, 2, 3])}');
}
```

**Output:**
```
Colors: {yellow, purple, orange}
Numbers: {1, 2, 3, 4, 5}
Union: {1, 2, 3, 4, 5, 6, 7, 8}
Intersection: {4, 5}
Difference: {1, 2, 3}
Contains all: true
```

#### Example 4: Map Basics
```dart
void main() {
  // Creating maps
  Map<String, int> ages = {
    'Alice': 25,
    'Bob': 30,
    'Charlie': 35
  };
  
  Map<String, String> capitals = Map();
  capitals['USA'] = 'Washington D.C.';
  capitals['France'] = 'Paris';
  capitals['Japan'] = 'Tokyo';
  
  // Accessing values
  print('Alice\'s age: ${ages['Alice']}');
  print('Capital of France: ${capitals['France']}');
  
  // Modifying maps
  ages['David'] = 28;
  ages['Alice'] = 26; // Update existing
  ages.remove('Bob');
  
  print('Ages: $ages');
  print('Capitals: $capitals');
  
  // Map properties
  print('Number of people: ${ages.length}');
  print('Keys: ${ages.keys}');
  print('Values: ${ages.values}');
  print('Is empty: ${ages.isEmpty}');
}
```

**Output:**
```
Alice's age: 25
Capital of France: Paris
Ages: {Alice: 26, Charlie: 35, David: 28}
Capitals: {USA: Washington D.C., France: Paris, Japan: Tokyo}
Number of people: 3
Keys: (Alice, Charlie, David)
Values: (26, 35, 28)
Is empty: false
```

#### Example 5: Map Methods and Operations
```dart
void main() {
  Map<String, int> scores = {
    'Alice': 95,
    'Bob': 87,
    'Charlie': 92,
    'David': 78
  };
  
  // Iterating through maps
  print('All scores:');
  scores.forEach((name, score) {
    print('$name: $score');
  });
  
  // Using entries
  print('\nHigh scorers:');
  scores.entries.where((entry) => entry.value >= 90).forEach((entry) {
    print('${entry.key}: ${entry.value}');
  });
  
  // Map transformations
  Map<String, String> grades = scores.map((name, score) {
    String grade = score >= 90 ? 'A' : 
                   score >= 80 ? 'B' : 
                   score >= 70 ? 'C' : 'F';
    return MapEntry(name, grade);
  });
  
  print('\nGrades: $grades');
  
  // Checking conditions
  bool allPassed = scores.values.every((score) => score >= 60);
  bool anyExcellent = scores.values.any((score) => score >= 95);
  
  print('All passed: $allPassed');
  print('Any excellent: $anyExcellent');
}
```

**Output:**
```
All scores:
Alice: 95
Bob: 87
Charlie: 92
David: 78

High scorers:
Alice: 95
Charlie: 92

Grades: {Alice: A, Bob: B, Charlie: A, David: C}
All passed: true
Any excellent: true
```

#### Example 6: Collection Iteration Methods
```dart
void main() {
  List<int> numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
  
  // forEach
  print('Numbers:');
  numbers.forEach((n) => print(n));
  
  // map
  List<int> squares = numbers.map((n) => n * n).toList();
  print('Squares: $squares');
  
  // where (filter)
  List<int> evens = numbers.where((n) => n % 2 == 0).toList();
  print('Even numbers: $evens');
  
  // reduce
  int sum = numbers.reduce((a, b) => a + b);
  print('Sum: $sum');
  
  // fold
  int product = numbers.fold(1, (a, b) => a * b);
  print('Product: $product');
  
  // any
  bool hasEven = numbers.any((n) => n % 2 == 0);
  print('Has even numbers: $hasEven');
  
  // every
  bool allPositive = numbers.every((n) => n > 0);
  print('All positive: $allPositive');
  
  // take and skip
  List<int> firstThree = numbers.take(3).toList();
  List<int> skipFirstThree = numbers.skip(3).toList();
  print('First three: $firstThree');
  print('Skip first three: $skipFirstThree');
}
```

**Output:**
```
Numbers:
1
2
3
4
5
6
7
8
9
10
Squares: [1, 4, 9, 16, 25, 36, 49, 64, 81, 100]
Even numbers: [2, 4, 6, 8, 10]
Sum: 55
Product: 3628800
Has even numbers: true
All positive: true
First three: [1, 2, 3]
Skip first three: [4, 5, 6, 7, 8, 9, 10]
```

#### Example 7: List Comprehensions and Generators
```dart
void main() {
  // Generating lists
  List<int> numbers = List.generate(10, (index) => index + 1);
  print('Generated numbers: $numbers');
  
  // List comprehension-like operations
  List<int> squares = List.generate(5, (i) => (i + 1) * (i + 1));
  print('Squares: $squares');
  
  // Conditional generation
  List<int> evenNumbers = List.generate(10, (i) => (i + 1) * 2);
  print('Even numbers: $evenNumbers');
  
  // Using where and map together
  List<String> words = ['hello', 'world', 'dart', 'flutter', 'programming'];
  List<String> longWords = words
      .where((word) => word.length > 4)
      .map((word) => word.toUpperCase())
      .toList();
  print('Long words: $longWords');
  
  // Nested lists
  List<List<int>> matrix = List.generate(3, (i) => List.generate(3, (j) => i * 3 + j + 1));
  print('Matrix: $matrix');
}
```

**Output:**
```
Generated numbers: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
Squares: [1, 4, 9, 16, 25]
Even numbers: [2, 4, 6, 8, 10, 12, 14, 16, 18, 20]
Long words: [HELLO, WORLD, FLUTTER, PROGRAMMING]
Matrix: [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
```

#### Example 8: Queue Operations
```dart
import 'dart:collection';

void main() {
  // Creating queues
  Queue<String> queue = Queue<String>();
  Queue<int> numbers = Queue.from([1, 2, 3, 4, 5]);
  
  // Adding elements
  queue.add('first');
  queue.add('second');
  queue.addLast('third');
  queue.addFirst('zero');
  
  print('Queue: $queue');
  
  // Removing elements
  String first = queue.removeFirst();
  String last = queue.removeLast();
  
  print('Removed first: $first');
  print('Removed last: $last');
  print('Queue after removal: $queue');
  
  // Queue properties
  print('Length: ${queue.length}');
  print('Is empty: ${queue.isEmpty}');
  print('First element: ${queue.first}');
  print('Last element: ${queue.last}');
  
  // Iterating
  print('Queue elements:');
  for (String item in queue) {
    print(item);
  }
}
```

**Output:**
```
Queue: {zero, first, second, third}
Removed first: zero
Removed last: third
Queue after removal: {first, second}
Length: 2
Is empty: false
First element: first
Last element: second
Queue elements:
first
second
```

#### Example 9: Custom Collection Classes
```dart
class Stack<T> {
  List<T> _items = [];
  
  void push(T item) {
    _items.add(item);
  }
  
  T? pop() {
    if (_items.isEmpty) return null;
    return _items.removeLast();
  }
  
  T? peek() {
    if (_items.isEmpty) return null;
    return _items.last;
  }
  
  bool get isEmpty => _items.isEmpty;
  int get length => _items.length;
  
  @override
  String toString() => _items.toString();
}

class Queue<T> {
  List<T> _items = [];
  
  void enqueue(T item) {
    _items.add(item);
  }
  
  T? dequeue() {
    if (_items.isEmpty) return null;
    return _items.removeAt(0);
  }
  
  T? front() {
    if (_items.isEmpty) return null;
    return _items.first;
  }
  
  bool get isEmpty => _items.isEmpty;
  int get length => _items.length;
  
  @override
  String toString() => _items.toString();
}

void main() {
  // Using custom Stack
  Stack<int> stack = Stack<int>();
  stack.push(1);
  stack.push(2);
  stack.push(3);
  
  print('Stack: $stack');
  print('Peek: ${stack.peek()}');
  print('Pop: ${stack.pop()}');
  print('Stack after pop: $stack');
  
  // Using custom Queue
  Queue<String> queue = Queue<String>();
  queue.enqueue('first');
  queue.enqueue('second');
  queue.enqueue('third');
  
  print('\nQueue: $queue');
  print('Front: ${queue.front()}');
  print('Dequeue: ${queue.dequeue()}');
  print('Queue after dequeue: $queue');
}
```

**Output:**
```
Stack: [1, 2, 3]
Peek: 3
Pop: 3
Stack after pop: [1, 2]

Queue: [first, second, third]
Front: first
Dequeue: first
Queue after dequeue: [second, third]
```

#### Example 10: Advanced Collection Operations
```dart
void main() {
  List<Map<String, dynamic>> students = [
    {'name': 'Alice', 'age': 20, 'grade': 'A'},
    {'name': 'Bob', 'age': 22, 'grade': 'B'},
    {'name': 'Charlie', 'age': 19, 'grade': 'A'},
    {'name': 'David', 'age': 21, 'grade': 'C'},
    {'name': 'Eve', 'age': 20, 'grade': 'B'},
  ];
  
  // Grouping
  Map<String, List<Map<String, dynamic>>> groupedByGrade = {};
  for (var student in students) {
    String grade = student['grade'];
    groupedByGrade.putIfAbsent(grade, () => []).add(student);
  }
  
  print('Grouped by grade: $groupedByGrade');
  
  // Sorting
  students.sort((a, b) => a['age'].compareTo(b['age']));
  print('\nSorted by age: $students');
  
  // Filtering and mapping
  List<String> honorStudents = students
      .where((student) => student['grade'] == 'A')
      .map((student) => student['name'])
      .toList();
  
  print('\nHonor students: $honorStudents');
  
  // Aggregation
  double averageAge = students
      .map((student) => student['age'] as int)
      .reduce((a, b) => a + b) / students.length;
  
  print('\nAverage age: ${averageAge.toStringAsFixed(1)}');
  
  // Finding
  Map<String, dynamic>? oldestStudent = students
      .reduce((a, b) => a['age'] > b['age'] ? a : b);
  
  print('Oldest student: $oldestStudent');
  
  // Partitioning
  List<List<Map<String, dynamic>>> partitioned = students
      .fold([[], []], (acc, student) {
        if (student['age'] >= 20) {
          acc[0].add(student);
        } else {
          acc[1].add(student);
        }
        return acc;
      });
  
  print('\nAdults (20+): ${partitioned[0]}');
  print('Minors (<20): ${partitioned[1]}');
}
```

**Output:**
```
Grouped by grade: {A: [{name: Alice, age: 20, grade: A}, {name: Charlie, age: 19, grade: A}], B: [{name: Bob, age: 22, grade: B}, {name: Eve, age: 20, grade: B}], C: [{name: David, age: 21, grade: C}]}

Sorted by age: [{name: Charlie, age: 19, grade: A}, {name: Alice, age: 20, grade: A}, {name: Eve, age: 20, grade: B}, {name: David, age: 21, grade: C}, {name: Bob, age: 22, grade: B}]

Honor students: [Alice, Charlie]

Average age: 20.4

Oldest student: {name: Bob, age: 22, grade: B}

Adults (20+): [{name: Alice, age: 20, grade: A}, {name: Bob, age: 22, grade: B}, {name: David, age: 21, grade: C}, {name: Eve, age: 20, grade: B}]
Minors (<20): [{name: Charlie, age: 19, grade: A}]
```

---

## 5. File Handling in Dart

### Overview
File handling in Dart allows you to read from and write to files on the local filesystem. Dart provides the `dart:io` library for file operations, which includes classes like `File`, `Directory`, and `FileSystemEntity`.

### Key Concepts
- **File**: Represents a file on the filesystem
- **Directory**: Represents a directory on the filesystem
- **FileSystemEntity**: Base class for both files and directories
- **Path operations**: Working with file and directory paths
- **Asynchronous operations**: Most file operations are asynchronous

### 10 Examples of File Handling in Dart

#### Example 1: Basic File Reading
```dart
import 'dart:io';

void main() async {
  try {
    // Create a file object
    File file = File('example.txt');
    
    // Check if file exists
    if (await file.exists()) {
      // Read file contents
      String contents = await file.readAsString();
      print('File contents:');
      print(contents);
    } else {
      print('File does not exist');
    }
  } catch (e) {
    print('Error reading file: $e');
  }
}
```

**Output:**
```
File contents:
Hello, World!
This is a sample text file.
```

#### Example 2: File Writing
```dart
import 'dart:io';

void main() async {
  try {
    // Create a file object
    File file = File('output.txt');
    
    // Write content to file
    await file.writeAsString('Hello from Dart!\nThis is a new file.');
    print('File written successfully');
    
    // Read back to verify
    String contents = await file.readAsString();
    print('File contents:');
    print(contents);
  } catch (e) {
    print('Error writing file: $e');
  }
}
```

**Output:**
```
File written successfully
File contents:
Hello from Dart!
This is a new file.
```

#### Example 3: Reading File Line by Line
```dart
import 'dart:io';

void main() async {
  try {
    File file = File('data.txt');
    
    if (await file.exists()) {
      // Read file as lines
      List<String> lines = await file.readAsLines();
      
      print('File has ${lines.length} lines:');
      for (int i = 0; i < lines.length; i++) {
        print('Line ${i + 1}: ${lines[i]}');
      }
    } else {
      print('File does not exist');
    }
  } catch (e) {
    print('Error: $e');
  }
}
```

**Output:**
```
File has 3 lines:
Line 1: First line
Line 2: Second line
Line 3: Third line
```

#### Example 4: Appending to File
```dart
import 'dart:io';

void main() async {
  try {
    File file = File('log.txt');
    
    // Append content to file
    await file.writeAsString('New log entry: ${DateTime.now()}\n', mode: FileMode.append);
    print('Log entry added');
    
    // Read all content
    String contents = await file.readAsString();
    print('All log entries:');
    print(contents);
  } catch (e) {
    print('Error: $e');
  }
}
```

**Output:**
```
Log entry added
All log entries:
Previous log entry: 2024-01-01 10:00:00
New log entry: 2024-01-01 10:30:00
```

#### Example 5: Working with Directories
```dart
import 'dart:io';

void main() async {
  try {
    // Create directory
    Directory dir = Directory('test_folder');
    if (!await dir.exists()) {
      await dir.create();
      print('Directory created: ${dir.path}');
    }
    
    // List directory contents
    List<FileSystemEntity> contents = await dir.list().toList();
    print('Directory contents:');
    for (var item in contents) {
      print('- ${item.path}');
    }
    
    // Get directory info
    print('Directory path: ${dir.path}');
    print('Directory absolute path: ${dir.absolute.path}');
  } catch (e) {
    print('Error: $e');
  }
}
```

**Output:**
```
Directory created: test_folder
Directory contents:
- test_folder\file1.txt
- test_folder\file2.txt
Directory path: test_folder
Directory absolute path: C:\Users\Admin\Desktop\Error Fix\test_folder
```

#### Example 6: File Copying and Moving
```dart
import 'dart:io';

void main() async {
  try {
    File sourceFile = File('source.txt');
    File destinationFile = File('destination.txt');
    
    // Create source file with content
    await sourceFile.writeAsString('This is the source file content');
    
    // Copy file
    await sourceFile.copy(destinationFile.path);
    print('File copied successfully');
    
    // Verify copy
    String copiedContent = await destinationFile.readAsString();
    print('Copied file content: $copiedContent');
    
    // Move file (rename)
    File movedFile = File('moved.txt');
    await destinationFile.rename(movedFile.path);
    print('File moved to: ${movedFile.path}');
  } catch (e) {
    print('Error: $e');
  }
}
```

**Output:**
```
File copied successfully
Copied file content: This is the source file content
File moved to: moved.txt
```

#### Example 7: File Properties and Metadata
```dart
import 'dart:io';

void main() async {
  try {
    File file = File('example.txt');
    
    if (await file.exists()) {
      // Get file properties
      FileStat stat = await file.stat();
      
      print('File properties:');
      print('Path: ${file.path}');
      print('Size: ${stat.size} bytes');
      print('Type: ${stat.type}');
      print('Modified: ${stat.modified}');
      print('Accessed: ${stat.accessed}');
      print('Changed: ${stat.changed}');
      print('Mode: ${stat.mode}');
    } else {
      print('File does not exist');
    }
  } catch (e) {
    print('Error: $e');
  }
}
```

**Output:**
```
File properties:
Path: example.txt
Size: 25 bytes
Type: FileSystemEntityType.file
Modified: 2024-01-01 10:30:00.000
Accessed: 2024-01-01 10:30:00.000
Changed: 2024-01-01 10:30:00.000
Mode: 33206
```

#### Example 8: Binary File Operations
```dart
import 'dart:io';
import 'dart:typed_data';

void main() async {
  try {
    File file = File('binary_data.bin');
    
    // Write binary data
    List<int> data = [72, 101, 108, 108, 111]; // "Hello" in ASCII
    await file.writeAsBytes(data);
    print('Binary data written');
    
    // Read binary data
    Uint8List bytes = await file.readAsBytes();
    print('Read bytes: $bytes');
    
    // Convert to string
    String text = String.fromCharCodes(bytes);
    print('As text: $text');
  } catch (e) {
    print('Error: $e');
  }
}
```

**Output:**
```
Binary data written
Read bytes: [72, 101, 108, 108, 111]
As text: Hello
```

#### Example 9: File Stream Operations
```dart
import 'dart:io';
import 'dart:convert';

void main() async {
  try {
    File file = File('large_file.txt');
    
    // Write large content
    String content = 'Line ${DateTime.now().millisecondsSinceEpoch}\n' * 1000;
    await file.writeAsString(content);
    print('Large file created');
    
    // Read file using stream
    Stream<List<int>> inputStream = file.openRead();
    Stream<String> lines = inputStream
        .transform(utf8.decoder)
        .transform(LineSplitter());
    
    int lineCount = 0;
    await for (String line in lines) {
      lineCount++;
      if (lineCount <= 5) {
        print('Line $lineCount: $line');
      }
    }
    print('Total lines: $lineCount');
  } catch (e) {
    print('Error: $e');
  }
}
```

**Output:**
```
Large file created
Line 1: Line 1704067200000
Line 2: Line 1704067200000
Line 3: Line 1704067200000
Line 4: Line 1704067200000
Line 5: Line 1704067200000
Total lines: 1000
```

#### Example 10: Error Handling and File Cleanup
```dart
import 'dart:io';

void main() async {
  File? tempFile;
  Directory? tempDir;
  
  try {
    // Create temporary directory
    tempDir = await Directory.systemTemp.createTemp('dart_temp_');
    print('Temporary directory created: ${tempDir.path}');
    
    // Create temporary file
    tempFile = File('${tempDir.path}/temp_file.txt');
    await tempFile.writeAsString('Temporary file content');
    print('Temporary file created');
    
    // Simulate some work
    await Future.delayed(Duration(seconds: 1));
    
    // Read the file
    String content = await tempFile.readAsString();
    print('File content: $content');
    
  } catch (e) {
    print('Error occurred: $e');
  } finally {
    // Cleanup: delete temporary files and directories
    try {
      if (tempFile != null && await tempFile.exists()) {
        await tempFile.delete();
        print('Temporary file deleted');
      }
      
      if (tempDir != null && await tempDir.exists()) {
        await tempDir.delete(recursive: true);
        print('Temporary directory deleted');
      }
    } catch (e) {
      print('Error during cleanup: $e');
    }
  }
}
```

**Output:**
```
Temporary directory created: C:\Users\Admin\AppData\Local\Temp\dart_temp_12345
Temporary file created
File content: Temporary file content
Temporary file deleted
Temporary directory deleted
```

---

## 6. OOP in Dart

### Overview
Object-Oriented Programming (OOP) in Dart is built around classes and objects. Dart supports all major OOP concepts including encapsulation, inheritance, polymorphism, and abstraction.

### Key Concepts
- **Class**: Blueprint for creating objects
- **Object**: Instance of a class
- **Constructor**: Special method for initializing objects
- **Inheritance**: Creating new classes based on existing ones
- **Polymorphism**: Same interface, different implementations
- **Encapsulation**: Hiding internal implementation details
- **Abstract Classes**: Classes that cannot be instantiated
- **Interfaces**: Contracts that classes must implement

### 10 Examples of OOP in Dart

#### Example 1: Basic Class and Object
```dart
class Person {
  String name;
  int age;
  
  // Constructor
  Person(this.name, this.age);
  
  // Method
  void introduce() {
    print('Hi, I am $name and I am $age years old.');
  }
  
  // Getter
  String get info => 'Name: $name, Age: $age';
  
  // Setter
  set setAge(int newAge) {
    if (newAge > 0) {
      age = newAge;
    }
  }
}

void main() {
  // Creating objects
  Person person1 = Person('Alice', 25);
  Person person2 = Person('Bob', 30);
  
  // Using methods
  person1.introduce();
  person2.introduce();
  
  // Using getters and setters
  print(person1.info);
  person1.setAge = 26;
  print('After age change: ${person1.info}');
}
```

**Output:**
```
Hi, I am Alice and I am 25 years old.
Hi, I am Bob and I am 30 years old.
Name: Alice, Age: 25
After age change: Name: Alice, Age: 26
```

#### Example 2: Constructor Variations
```dart
class Rectangle {
  double width;
  double height;
  
  // Default constructor
  Rectangle(this.width, this.height);
  
  // Named constructor
  Rectangle.square(double side) : width = side, height = side;
  
  // Named constructor with default values
  Rectangle.unit() : width = 1.0, height = 1.0;
  
  // Factory constructor
  factory Rectangle.fromDimensions(double w, double h) {
    return Rectangle(w, h);
  }
  
  // Method
  double get area => width * height;
  double get perimeter => 2 * (width + height);
}

void main() {
  // Using different constructors
  Rectangle rect1 = Rectangle(5.0, 3.0);
  Rectangle square = Rectangle.square(4.0);
  Rectangle unit = Rectangle.unit();
  Rectangle factory = Rectangle.fromDimensions(6.0, 2.0);
  
  print('Rectangle 1 - Area: ${rect1.area}, Perimeter: ${rect1.perimeter}');
  print('Square - Area: ${square.area}, Perimeter: ${square.perimeter}');
  print('Unit - Area: ${unit.area}, Perimeter: ${unit.perimeter}');
  print('Factory - Area: ${factory.area}, Perimeter: ${factory.perimeter}');
}
```

**Output:**
```
Rectangle 1 - Area: 15.0, Perimeter: 16.0
Square - Area: 16.0, Perimeter: 16.0
Unit - Area: 1.0, Perimeter: 4.0
Factory - Area: 12.0, Perimeter: 16.0
```

#### Example 3: Inheritance
```dart
// Base class
class Animal {
  String name;
  int age;
  
  Animal(this.name, this.age);
  
  void makeSound() {
    print('Some generic animal sound');
  }
  
  void eat() {
    print('$name is eating');
  }
  
  void sleep() {
    print('$name is sleeping');
  }
}

// Derived class
class Dog extends Animal {
  String breed;
  
  Dog(String name, int age, this.breed) : super(name, age);
  
  // Override method
  @override
  void makeSound() {
    print('$name barks: Woof! Woof!');
  }
  
  // Additional method
  void fetch() {
    print('$name is fetching the ball');
  }
}

// Another derived class
class Cat extends Animal {
  String color;
  
  Cat(String name, int age, this.color) : super(name, age);
  
  @override
  void makeSound() {
    print('$name meows: Meow! Meow!');
  }
  
  void climb() {
    print('$name is climbing the tree');
  }
}

void main() {
  Dog dog = Dog('Buddy', 3, 'Golden Retriever');
  Cat cat = Cat('Whiskers', 2, 'Orange');
  
  // Using inherited methods
  dog.eat();
  dog.sleep();
  dog.makeSound();
  dog.fetch();
  
  print('---');
  
  cat.eat();
  cat.sleep();
  cat.makeSound();
  cat.climb();
}
```

**Output:**
```
Buddy is eating
Buddy is sleeping
Buddy barks: Woof! Woof!
Buddy is fetching the ball
---
Whiskers is eating
Whiskers is sleeping
Whiskers meows: Meow! Meow!
Whiskers is climbing the tree
```

#### Example 4: Abstract Classes and Interfaces
```dart
// Abstract class
abstract class Shape {
  double get area;
  double get perimeter;
  
  // Abstract method
  void draw();
  
  // Concrete method
  void displayInfo() {
    print('Area: $area, Perimeter: $perimeter');
  }
}

// Interface (using abstract class)
abstract class Drawable {
  void draw();
  void setColor(String color);
}

// Concrete class implementing both abstract class and interface
class Circle extends Shape implements Drawable {
  double radius;
  String color = 'black';
  
  Circle(this.radius);
  
  @override
  double get area => 3.14159 * radius * radius;
  
  @override
  double get perimeter => 2 * 3.14159 * radius;
  
  @override
  void draw() {
    print('Drawing a $color circle with radius $radius');
  }
  
  @override
  void setColor(String color) {
    this.color = color;
  }
}

class Rectangle extends Shape implements Drawable {
  double width;
  double height;
  String color = 'black';
  
  Rectangle(this.width, this.height);
  
  @override
  double get area => width * height;
  
  @override
  double get perimeter => 2 * (width + height);
  
  @override
  void draw() {
    print('Drawing a $color rectangle ${width}x$height');
  }
  
  @override
  void setColor(String color) {
    this.color = color;
  }
}

void main() {
  Circle circle = Circle(5.0);
  Rectangle rectangle = Rectangle(4.0, 6.0);
  
  circle.setColor('red');
  circle.draw();
  circle.displayInfo();
  
  print('---');
  
  rectangle.setColor('blue');
  rectangle.draw();
  rectangle.displayInfo();
}
```

**Output:**
```
Drawing a red circle with radius 5.0
Area: 78.53975, Perimeter: 31.4159
---
Drawing a blue rectangle 4.0x6.0
Area: 24.0, Perimeter: 20.0
```

#### Example 5: Polymorphism
```dart
// Base class
class Vehicle {
  String brand;
  int year;
  
  Vehicle(this.brand, this.year);
  
  void start() {
    print('$brand vehicle is starting');
  }
  
  void stop() {
    print('$brand vehicle is stopping');
  }
  
  void accelerate() {
    print('$brand vehicle is accelerating');
  }
}

// Derived classes
class Car extends Vehicle {
  int doors;
  
  Car(String brand, int year, this.doors) : super(brand, year);
  
  @override
  void accelerate() {
    print('$brand car with $doors doors is accelerating smoothly');
  }
  
  void honk() {
    print('$brand car is honking');
  }
}

class Motorcycle extends Vehicle {
  bool hasWindshield;
  
  Motorcycle(String brand, int year, this.hasWindshield) : super(brand, year);
  
  @override
  void accelerate() {
    print('$brand motorcycle is accelerating quickly');
  }
  
  void wheelie() {
    print('$brand motorcycle is doing a wheelie');
  }
}

class Truck extends Vehicle {
  double cargoCapacity;
  
  Truck(String brand, int year, this.cargoCapacity) : super(brand, year);
  
  @override
  void accelerate() {
    print('$brand truck is accelerating slowly with heavy cargo');
  }
  
  void loadCargo() {
    print('$brand truck is loading cargo');
  }
}

void main() {
  // Polymorphism: same interface, different implementations
  List<Vehicle> vehicles = [
    Car('Toyota', 2020, 4),
    Motorcycle('Honda', 2019, true),
    Truck('Ford', 2021, 2.5),
  ];
  
  for (Vehicle vehicle in vehicles) {
    vehicle.start();
    vehicle.accelerate();
    vehicle.stop();
    print('---');
  }
  
  // Type-specific methods
  Car car = Car('BMW', 2022, 2);
  car.honk();
  
  Motorcycle bike = Motorcycle('Yamaha', 2020, false);
  bike.wheelie();
}
```

**Output:**
```
Toyota vehicle is starting
Toyota car with 4 doors is accelerating smoothly
Toyota vehicle is stopping
---
Honda vehicle is starting
Honda motorcycle is accelerating quickly
Honda vehicle is stopping
---
Ford vehicle is starting
Ford truck is accelerating slowly with heavy cargo
Ford vehicle is stopping
---
BMW car is honking
Yamaha motorcycle is doing a wheelie
```

#### Example 6: Encapsulation and Access Modifiers
```dart
class BankAccount {
  // Private fields (encapsulation)
  double _balance;
  String _accountNumber;
  String _accountHolder;
  
  // Constructor
  BankAccount(this._accountNumber, this._accountHolder, this._balance);
  
  // Public getters
  double get balance => _balance;
  String get accountNumber => _accountNumber;
  String get accountHolder => _accountHolder;
  
  // Public methods
  void deposit(double amount) {
    if (amount > 0) {
      _balance += amount;
      print('Deposited \$${amount.toStringAsFixed(2)}. New balance: \$${_balance.toStringAsFixed(2)}');
    } else {
      print('Invalid deposit amount');
    }
  }
  
  bool withdraw(double amount) {
    if (amount > 0 && amount <= _balance) {
      _balance -= amount;
      print('Withdrew \$${amount.toStringAsFixed(2)}. New balance: \$${_balance.toStringAsFixed(2)}');
      return true;
    } else {
      print('Invalid withdrawal amount or insufficient funds');
      return false;
    }
  }
  
  void displayInfo() {
    print('Account: $_accountNumber');
    print('Holder: $_accountHolder');
    print('Balance: \$${_balance.toStringAsFixed(2)}');
  }
  
  // Private method
  void _logTransaction(String type, double amount) {
    print('Transaction logged: $type \$${amount.toStringAsFixed(2)} at ${DateTime.now()}');
  }
}

void main() {
  BankAccount account = BankAccount('123456789', 'John Doe', 1000.0);
  
  account.displayInfo();
  print('---');
  
  account.deposit(500.0);
  account.withdraw(200.0);
  account.withdraw(2000.0); // Should fail
  
  print('---');
  account.displayInfo();
}
```

**Output:**
```
Account: 123456789
Holder: John Doe
Balance: $1000.00
---
Deposited $500.00. New balance: $1500.00
Withdrew $200.00. New balance: $1300.00
Invalid withdrawal amount or insufficient funds
---
Account: 123456789
Holder: John Doe
Balance: $1300.00
```

#### Example 7: Static Members and Constants
```dart
class MathUtils {
  // Static constant
  static const double pi = 3.14159;
  
  // Static variable
  static int calculationCount = 0;
  
  // Static method
  static double circleArea(double radius) {
    calculationCount++;
    return pi * radius * radius;
  }
  
  static double circleCircumference(double radius) {
    calculationCount++;
    return 2 * pi * radius;
  }
  
  static double rectangleArea(double width, double height) {
    calculationCount++;
    return width * height;
  }
  
  static void resetCounter() {
    calculationCount = 0;
  }
  
  static void displayStats() {
    print('Total calculations performed: $calculationCount');
  }
}

class Counter {
  // Instance variable
  int _count = 0;
  
  // Instance method
  void increment() {
    _count++;
  }
  
  int get count => _count;
  
  // Static method that creates instances
  static Counter createCounter() {
    return Counter();
  }
}

void main() {
  // Using static methods without creating instances
  double area = MathUtils.circleArea(5.0);
  double circumference = MathUtils.circleCircumference(5.0);
  double rectArea = MathUtils.rectangleArea(4.0, 6.0);
  
  print('Circle area: ${area.toStringAsFixed(2)}');
  print('Circle circumference: ${circumference.toStringAsFixed(2)}');
  print('Rectangle area: ${rectArea.toStringAsFixed(2)}');
  
  MathUtils.displayStats();
  
  print('---');
  
  // Creating instances using static method
  Counter counter1 = Counter.createCounter();
  Counter counter2 = Counter.createCounter();
  
  counter1.increment();
  counter1.increment();
  counter2.increment();
  
  print('Counter 1: ${counter1.count}');
  print('Counter 2: ${counter2.count}');
}
```

**Output:**
```
Circle area: 78.54
Circle circumference: 31.42
Rectangle area: 24.00
Total calculations performed: 3
---
Counter 1: 2
Counter 2: 1
```

#### Example 8: Mixins
```dart
// Mixin for flying behavior
mixin Flyable {
  void fly() {
    print('Flying through the air');
  }
  
  void land() {
    print('Landing safely');
  }
}

// Mixin for swimming behavior
mixin Swimmable {
  void swim() {
    print('Swimming in water');
  }
  
  void dive() {
    print('Diving deep');
  }
}

// Mixin for walking behavior
mixin Walkable {
  void walk() {
    print('Walking on land');
  }
  
  void run() {
    print('Running fast');
  }
}

// Base class
class Animal {
  String name;
  
  Animal(this.name);
  
  void eat() {
    print('$name is eating');
  }
}

// Classes using mixins
class Bird extends Animal with Flyable, Walkable {
  Bird(String name) : super(name);
  
  void chirp() {
    print('$name is chirping');
  }
}

class Fish extends Animal with Swimmable {
  Fish(String name) : super(name);
  
  void bubble() {
    print('$name is making bubbles');
  }
}

class Duck extends Animal with Flyable, Swimmable, Walkable {
  Duck(String name) : super(name);
  
  void quack() {
    print('$name is quacking');
  }
}

void main() {
  Bird bird = Bird('Eagle');
  Fish fish = Fish('Salmon');
  Duck duck = Duck('Mallard');
  
  // Bird behaviors
  bird.eat();
  bird.fly();
  bird.walk();
  bird.chirp();
  
  print('---');
  
  // Fish behaviors
  fish.eat();
  fish.swim();
  fish.dive();
  fish.bubble();
  
  print('---');
  
  // Duck behaviors (can do everything)
  duck.eat();
  duck.fly();
  duck.swim();
  duck.walk();
  duck.quack();
}
```

**Output:**
```
Eagle is eating
Flying through the air
Walking on land
Eagle is chirping
---
Salmon is eating
Swimming in water
Diving deep
Salmon is making bubbles
---
Mallard is eating
Flying through the air
Swimming in water
Walking on land
Mallard is quacking
```

#### Example 9: Generics
```dart
// Generic class
class Box<T> {
  T _item;
  
  Box(this._item);
  
  T get item => _item;
  
  void setItem(T newItem) {
    _item = newItem;
  }
  
  void display() {
    print('Box contains: $_item (${_item.runtimeType})');
  }
}

// Generic method
T getFirst<T>(List<T> list) {
  if (list.isNotEmpty) {
    return list.first;
  }
  throw Exception('List is empty');
}

// Generic interface
abstract class Repository<T> {
  void save(T item);
  T? findById(int id);
  List<T> findAll();
  void delete(int id);
}

// Concrete implementation
class UserRepository implements Repository<User> {
  List<User> _users = [];
  int _nextId = 1;
  
  @override
  void save(User user) {
    user.id = _nextId++;
    _users.add(user);
    print('User saved: ${user.name}');
  }
  
  @override
  User? findById(int id) {
    try {
      return _users.firstWhere((user) => user.id == id);
    } catch (e) {
      return null;
    }
  }
  
  @override
  List<User> findAll() {
    return List.from(_users);
  }
  
  @override
  void delete(int id) {
    _users.removeWhere((user) => user.id == id);
    print('User with id $id deleted');
  }
}

class User {
  int? id;
  String name;
  String email;
  
  User(this.name, this.email);
  
  @override
  String toString() => 'User(id: $id, name: $name, email: $email)';
}

void main() {
  // Using generic class
  Box<String> stringBox = Box('Hello');
  Box<int> intBox = Box(42);
  Box<double> doubleBox = Box(3.14);
  
  stringBox.display();
  intBox.display();
  doubleBox.display();
  
  print('---');
  
  // Using generic method
  List<String> names = ['Alice', 'Bob', 'Charlie'];
  List<int> numbers = [1, 2, 3, 4, 5];
  
  String firstName = getFirst(names);
  int firstNumber = getFirst(numbers);
  
  print('First name: $firstName');
  print('First number: $firstNumber');
  
  print('---');
  
  // Using generic repository
  UserRepository userRepo = UserRepository();
  
  userRepo.save(User('Alice', 'alice@example.com'));
  userRepo.save(User('Bob', 'bob@example.com'));
  
  List<User> allUsers = userRepo.findAll();
  print('All users: $allUsers');
  
  User? user = userRepo.findById(1);
  print('Found user: $user');
}
```

**Output:**
```
Box contains: Hello (String)
Box contains: 42 (int)
Box contains: 3.14 (double)
---
First name: Alice
First number: 1
---
User saved: Alice
User saved: Bob
All users: [User(id: 1, name: Alice, email: alice@example.com), User(id: 2, name: Bob, email: bob@example.com)]
Found user: User(id: 1, name: Alice, email: alice@example.com)
```

#### Example 10: Advanced OOP Concepts
```dart
// Abstract base class
abstract class Shape {
  String name;
  
  Shape(this.name);
  
  // Abstract methods
  double get area;
  double get perimeter;
  
  // Concrete method
  void displayInfo() {
    print('$name - Area: ${area.toStringAsFixed(2)}, Perimeter: ${perimeter.toStringAsFixed(2)}');
  }
}

// Interface
abstract class Drawable {
  void draw();
  void setColor(String color);
}

// Mixin
mixin Movable {
  void move(double x, double y) {
    print('Moving to position ($x, $y)');
  }
}

// Concrete class implementing multiple concepts
class Circle extends Shape implements Drawable with Movable {
  double radius;
  String color = 'black';
  double x = 0, y = 0;
  
  Circle(String name, this.radius) : super(name);
  
  @override
  double get area => 3.14159 * radius * radius;
  
  @override
  double get perimeter => 2 * 3.14159 * radius;
  
  @override
  void draw() {
    print('Drawing a $color circle with radius $radius at ($x, $y)');
  }
  
  @override
  void setColor(String color) {
    this.color = color;
  }
  
  @override
  void move(double x, double y) {
    this.x = x;
    this.y = y;
    super.move(x, y);
  }
}

// Generic class with constraints
class Container<T extends Shape> {
  List<T> shapes = [];
  
  void addShape(T shape) {
    shapes.add(shape);
    print('Added ${shape.name} to container');
  }
  
  void displayAll() {
    print('Container contents:');
    for (var shape in shapes) {
      shape.displayInfo();
    }
  }
  
  double get totalArea {
    return shapes.fold(0.0, (sum, shape) => sum + shape.area);
  }
}

// Factory pattern
class ShapeFactory {
  static Shape createShape(String type, String name, List<double> params) {
    switch (type.toLowerCase()) {
      case 'circle':
        return Circle(name, params[0]);
      case 'rectangle':
        return Rectangle(name, params[0], params[1]);
      default:
        throw ArgumentError('Unknown shape type: $type');
    }
  }
}

class Rectangle extends Shape implements Drawable with Movable {
  double width;
  double height;
  String color = 'black';
  double x = 0, y = 0;
  
  Rectangle(String name, this.width, this.height) : super(name);
  
  @override
  double get area => width * height;
  
  @override
  double get perimeter => 2 * (width + height);
  
  @override
  void draw() {
    print('Drawing a $color rectangle ${width}x$height at ($x, $y)');
  }
  
  @override
  void setColor(String color) {
    this.color = color;
  }
  
  @override
  void move(double x, double y) {
    this.x = x;
    this.y = y;
    super.move(x, y);
  }
}

void main() {
  // Using factory pattern
  Shape circle = ShapeFactory.createShape('circle', 'MyCircle', [5.0]);
  Shape rectangle = ShapeFactory.createShape('rectangle', 'MyRectangle', [4.0, 6.0]);
  
  // Using polymorphism
  List<Shape> shapes = [circle, rectangle];
  
  for (var shape in shapes) {
    shape.displayInfo();
  }
  
  print('---');
  
  // Using generic container
  Container<Shape> container = Container<Shape>();
  container.addShape(circle);
  container.addShape(rectangle);
  
  container.displayAll();
  print('Total area: ${container.totalArea.toStringAsFixed(2)}');
  
  print('---');
  
  // Using mixins and interfaces
  Circle drawableCircle = Circle('DrawableCircle', 3.0);
  drawableCircle.setColor('red');
  drawableCircle.move(10.0, 20.0);
  drawableCircle.draw();
}
```

**Output:**
```
MyCircle - Area: 78.54, Perimeter: 31.42
MyRectangle - Area: 24.00, Perimeter: 20.00
---
Added MyCircle to container
Added MyRectangle to container
Container contents:
MyCircle - Area: 78.54, Perimeter: 31.42
MyRectangle - Area: 24.00, Perimeter: 20.00
Total area: 102.54
---
Moving to position (10.0, 20.0)
Drawing a red circle with radius 3.0 at (10.0, 20.0)
```
## 7. Null Safety In Dart

### Overview 
Null safety in Dart ensures that variables cannot contain null unless explicitly allowed. This helps prevent runtime errors caused by unexpected null values.

### Key Concepts
- **Non-nullable types**: Cannot be null.
- **Nullable types**: Can be null, declared with ?.
- **Null-aware operators**: Help handle nulls safely (??, ?., ??=).
- **Sound null safety**: Guarantees at compile time that non-nullable variables are never null.

  ### 10 Examples For Null Safety In Dart
  ### Example-1 Non-nullable vs Nullable Variables
  ```dart
  void main() {
  int a = 10;
  int? b = null;
  print(a); // Output: 10
  print(b); // Output: null
  }
  ```
  ### Example-2 Null-aware Operator ??
  ```dart
  void main() {
  String? name;
  print(name ?? 'Guest'); // Output: Guest
  }
  ```
  ### Example-3 Null-aware Access ?.
  ```dart
  void main() {
  String? name = 'Dart';
  print(name?.length); // Output: 4
  }
  ```
  ### Example-4  Null-aware Assignment ??=
  ```dart
  void main() {
  String? name;
  name ??= 'Fallback';
  print(name); // Output: Fallback
  }
  ```
  ### Example-5 Function with Nullable Parameter
  ```dart
  void greet(String? name) {
  print('Hello, ${name ?? 'Guest'}');
  }

  void main() {
  greet(null); // Output: Hello, Guest
  }
  ```
  ### Example-6 Type Promotion
  ```dart
  void printLength(String? text) {
  if (text != null) {
    print(text.length); // Output: 5
  }
  }

  void main() {
  printLength('Hello');
  }
  ```
  ### Example-7 Late Initialization
  ```dart
  late String title;

  void main() {
  title = 'Dart Guide';
  print(title); // Output: Dart Guide
  }
  ```
  ### Example-8 Required Named Parameters
  ```dart
  void display({required String message}) {
  print(message);
  }

  void main() {
  display(message: 'Hello Dart'); // Output: Hello Dart
  }
  ```
  ### Example-9 Nullable List Elements
  ```dart
  void main() {
  List<String?> names = ['Alice', null, 'Bob'];
  print(names); // Output: [Alice, null, Bob]
  }
  ```
  ### Example-10 Extension Method on Nullable Type
  ```dart
  extension StringExtension on String? {
  String orEmpty() => this ?? '';
  }

  void main() {
  String? name = null;
  print(name.orEmpty()); // Output: (empty string)
  }
  ```













