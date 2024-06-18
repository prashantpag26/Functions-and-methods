### Functions in Dart

A function in Dart is a block of code designed to perform a particular task. It can take inputs (parameters) and return an output (a value). Functions are essential building blocks in Dart, used for encapsulating code to make it reusable and easier to understand.

#### Declaring Functions

Here’s the basic syntax for declaring a function:

```dart
ReturnType functionName(ParameterType parameterName) {
  // Function body
  return value;
}
```

Example:

```dart
int add(int a, int b) {
  return a + b;
}
```

#### Calling Functions

You call a function by using its name followed by parentheses, including any arguments if the function requires them.

```dart
void main() {
  int result = add(2, 3);
  print(result); // Output: 5
}
```

#### Optional Parameters

Dart supports optional parameters, which can be either positional or named.

**Positional Optional Parameters:**

```dart
String greet(String name, [String title = '']) {
  return 'Hello, $title $name';
}

void main() {
  print(greet('Alice')); // Output: Hello, Alice
  print(greet('Alice', 'Ms.')); // Output: Hello, Ms. Alice
}
```

**Named Optional Parameters:**

```dart
String greet(String name, {String title = '', String suffix = ''}) {
  return 'Hello, $title $name $suffix';
}

void main() {
  print(greet('Alice')); // Output: Hello, Alice 
  print(greet('Alice', title: 'Ms.', suffix: 'PhD')); // Output: Hello, Ms. Alice PhD
}
```

### Methods in Dart

Methods are functions that are associated with an object. In Dart, methods are functions defined within a class. They operate on instances of the class and can access the class’s properties and other methods.

#### Defining Methods

Here’s an example of a class with methods:

```dart
class Person {
  String name;
  int age;

  Person(this.name, this.age);

  void introduce() {
    print('Hello, my name is $name and I am $age years old.');
  }

  int calculateBirthYear() {
    int currentYear = DateTime.now().year;
    return currentYear - age;
  }
}

void main() {
  Person p = Person('Alice', 30);
  p.introduce(); // Output: Hello, my name is Alice and I am 30 years old.
  print('I was born in ${p.calculateBirthYear()}'); // Output: I was born in 1994 (assuming the current year is 2024)
}
```

#### Static Methods

Static methods belong to the class itself rather than an instance of the class. They are defined using the `static` keyword.

```dart
class MathUtils {
  static int add(int a, int b) {
    return a + b;
  }
}

void main() {
  int result = MathUtils.add(2, 3);
  print(result); // Output: 5
}
```

### In Short

- **Functions:** Independent blocks of code that can be called from anywhere in your program.
- **Methods:** Functions that belong to an object (or class) and can interact with the object’s data.
- **Static Methods:** Belong to the class itself and can be called without creating an instance of the class.

