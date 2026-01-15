## Dart Recap (Cheatsheet)

### Dart
Dart is the language of Flutter. It compiles to native code for iOS and Android and can also target web and desktop from the same codebase.  
Dart supports both JIT and AOT:
- **JIT** (Just-In-Time) in development for fast hot reload  
- **AOT** (Ahead-Of-Time) in production for strong performance  
Dart has **null safety**, which prevents a large class of runtime crashes.

Good documentation:
- https://dart.dev/language
- https://api.dart.dev/

This recap covers the core Dart features you will use in Flutter.

---

## Variables
Dart uses `var`, `final`, and `const`.
- **var**: inferred type, value can be reassigned
- **final**: assigned once at runtime
- **const**: compile-time constant

```dart
var name = 'Alex';
name = 'Taylor';

final age = 20;
// age = 21; // Error

const pi = 3.14159;
```

**Note:** `final` and `const` prevent reassignment, but object contents can still change unless the object itself is `const`.

---

## Null Safety Basics
`?` makes a type nullable.  
`!` force-unwraps a nullable value (unsafe if it is null).

```dart
String? maybeName;
maybeName = 'Alex';
print(maybeName?.length); // 4

String name = maybeName!; // if null -> runtime error
```

### Null Safety Quirks You Must Know
- **Late initialization:** Use `late` only when you guarantee it will be set before use.
```dart
late String token;
token = 'abc123';
print(token);
```
- **Promotions are limited:** A nullable variable may not be promoted after async gaps.
```dart
String? value;
if (value != null) {
  // In async code, Dart may not promote this reliably
  print(value.length);
}
```
- **Default values with `??`:**
```dart
String? title;
final safeTitle = title ?? 'Untitled';
```
- **Null-aware access:** `?.` and `?..`
```dart
user?.profile?.refresh();
```

---

## String
Strings use `'` or `"` and support interpolation `${}`.

```dart
final first = 'Hello';
final second = "World";
print('$first $second');

final number = 123;
final text = 'Number is ${number + 1}';
```

Common string methods:
```dart
final str = 'Small fox jumped over the fence.';
str.contains('fox');
str.split(' ');
str.replaceAll('fox', 'rabbit');
str.toUpperCase();
```

---

## Number
Dart has `int` and `double`.

```dart
int count = 10;
double price = 12.50;

int parsed = int.parse('123');
double parsedDouble = double.parse('12.5');
```

Math library:
```dart
import 'dart:math';

final randomValue = Random().nextInt(100); // 0-99
final circleArea = pi * 10 * 10;
```

---

## Boolean
```dart
bool isOpen = false;
if (isOpen) {
  print('Open');
} else {
  print('Closed');
}
```

---

## List
```dart
final numbers = [1, 2, 3];
numbers.add(4);
print(numbers[0]); // 1
print(numbers.length); // 4
```

Common list methods:
```dart
final doubled = numbers.map((n) => n * 2).toList();
final evens = numbers.where((n) => n.isEven).toList();
final sum = numbers.reduce((a, b) => a + b);
```

---

## Map
```dart
final user = {
  'name': 'Alex',
  'age': 20,
};
print(user['name']);
```

Map methods:
```dart
user['city'] = 'Rovaniemi';
user.containsKey('age'); // true
```

---

## Functions
```dart
int add(int a, int b) => a + b;

void main() {
  print(add(2, 3)); // 5
}
```

Optional parameters:
```dart
String greet(String name, {String prefix = 'Hi'}) {
  return '$prefix $name';
}
```

---

## OOP Essentials

### Classes, Constructors, and Methods
```dart
class User {
  final String name;
  final int age;

  User(this.name, this.age);

  String info() => '$name is $age years old';
}
```

### Named Constructors
```dart
class User {
  final String name;
  final int age;

  User(this.name, this.age);
  User.guest() : name = 'Guest', age = 0;
}
```

### Inheritance and Overrides
```dart
class Animal {
  void speak() => print('...');
}

class Dog extends Animal {
  @override
  void speak() => print('Woof');
}
```

### Abstract Classes and Interfaces
```dart
abstract class Repository {
  Future<List<String>> fetchItems();
}

class ApiRepository implements Repository {
  @override
  Future<List<String>> fetchItems() async => ['a', 'b'];
}
```

### Mixins
```dart
mixin Logger {
  void log(String message) => print('[LOG] $message');
}

class Service with Logger {}
```

---

## Control Flow
```dart
for (int i = 0; i < 3; i++) {
  print(i);
}

for (final item in ['a', 'b']) {
  print(item);
}

if (true) {
  print('yes');
}
```

---

## Async / Await
```dart
Future<String> fetchData() async {
  await Future.delayed(const Duration(seconds: 1));
  return 'Done';
}
```

Try/catch:
```dart
try {
  final result = await fetchData();
  print(result);
} catch (e) {
  print('Error: $e');
}
```

---

## JSON
```dart
import 'dart:convert';

final jsonStr = '{"name":"Alex","age":20}';
final map = jsonDecode(jsonStr);
print(map['name']);

final encoded = jsonEncode({'ok': true});
```

---

## Import / Export
```dart
import 'dart:math';
import 'package:flutter/material.dart';
```

---

## Common Dart Shorthands

### Arrow Functions
```dart
int doubleIt(int x) => x * 2;
```

### Collection If and Spread
```dart
final isAdmin = true;
final items = [
  'home',
  if (isAdmin) 'admin',
  ...['help', 'settings'],
];
```

### Cascade Operator (`..`)
```dart
final buffer = StringBuffer()
  ..write('Hello')
  ..write(' ')
  ..write('World');
```

### Null-Aware Operators
```dart
String? label;
final safe = label ?? 'Default';
label ??= 'Assigned if null';
```

---

## Enums
Enums are fixed sets of values. They improve readability and safety over strings.

```dart
enum Status { idle, loading, success, error }

void main() {
  Status state = Status.loading;
  if (state == Status.loading) {
    print('Loading...');
  }
  print(state.name); // "loading"
}
```

Enhanced enums can include fields and methods:
```dart
enum Role {
  user('User'),
  admin('Admin');

  final String label;
  const Role(this.label);
}
```

---

## Generics
Generics let you write reusable, type-safe code.

```dart
class Box<T> {
  final T value;
  Box(this.value);
}

void main() {
  final intBox = Box<int>(123);
  final strBox = Box<String>('hello');
  print(intBox.value);
  print(strBox.value);
}
```

Generic functions:
```dart
T first<T>(List<T> items) => items.first;
```

Why it matters:
- Prevents accidental type mixing
- Helps IDEs and the compiler catch errors early

---

## Extensions
Extensions add methods to existing classes without modifying them.

```dart
extension StringCaps on String {
  String toCapitalized() {
    if (isEmpty) return this;
    return this[0].toUpperCase() + substring(1);
  }
}

void main() {
  print('dart'.toCapitalized()); // Dart
}
```

Use extensions to keep utility logic tidy and readable.

---

## Records (Dart 3)
Records are lightweight, immutable tuples for grouping values.

```dart
final user = ('Alex', 20); // (String, int)
print(user.$1); // Alex
print(user.$2); // 20
```

Named fields:
```dart
final point = (x: 10, y: 20);
print(point.x);
print(point.y);
```

Records are great for returning multiple values without creating a class.

---

## Pattern Matching (Dart 3)
Pattern matching helps you destructure and check data in a concise way.

### `switch` with patterns
```dart
Object value = (x: 10, y: 20);

switch (value) {
  case (x: int x, y: int y):
    print('Point: $x, $y');
  default:
    print('Unknown');
}
```

### List patterns
```dart
final list = [1, 2, 3];
switch (list) {
  case [1, int second, ...]:
    print('Starts with 1, second is $second');
  default:
    print('Other');
}
```

### Guard clauses
```dart
final (x, y) = (3, 4);
switch ((x, y)) {
  case (int a, int b) when a == b:
    print('Equal');
  case (int a, int b):
    print('Not equal');
}
```

Pattern matching reduces boilerplate and makes data handling safer.

---

## Sealed Classes (Dart 3)
Sealed classes define a closed set of subtypes, which enables exhaustive checks.

```dart
sealed class Result {}

class Success extends Result {
  final String data;
  Success(this.data);
}

class Failure extends Result {
  final String message;
  Failure(this.message);
}

void handle(Result result) {
  switch (result) {
    case Success s:
      print(s.data);
    case Failure f:
      print(f.message);
  }
}
```

This helps you cover every case explicitly in `switch`.

---

## Flutter Connection (Why It Matters)
- **Widgets** are Dart classes
- **State** is normal Dart objects
- **async/await** is required for API calls
- **null safety** prevents crashes on mobile

---

## Flutter Widgets (Why They Are Classes)
Flutter uses **widgets as immutable class instances**. Every UI element is a widget.

Why this design:
- **Immutability**: widgets describe UI; state changes live elsewhere (State objects).
- **Predictable rebuilds**: Flutter can recreate widgets cheaply on every build.
- **Composition**: small widgets compose into bigger ones like functions and classes.
- **Performance**: Flutter compares widget types/keys to reuse underlying elements.

Stateless vs Stateful:
- **StatelessWidget**: UI depends only on input parameters.
- **StatefulWidget**: UI depends on internal mutable State.

```dart
class TitleText extends StatelessWidget {
  const TitleText({super.key, required this.title});
  final String title;

  @override
  Widget build(BuildContext context) {
    return Text(title);
  }
}

class CounterPage extends StatefulWidget {
  const CounterPage({super.key});
  @override
  State<CounterPage> createState() => _CounterPageState();
}

class _CounterPageState extends State<CounterPage> {
  int count = 0;

  @override
  Widget build(BuildContext context) {
    return Column(
      children: [
        Text('Count: $count'),
        ElevatedButton(
          onPressed: () => setState(() => count++),
          child: const Text('Increment'),
        ),
      ],
    );
  }
}
```

---

## Small Application Example (Uses Dart Features)
This mini example uses enums, generics, extensions, records, pattern matching,
null safety, and a sealed result type.

```dart
import 'dart:math';

enum Mood { calm, focused, stressed }

extension MoodLabel on Mood {
  String get label => switch (this) {
        Mood.calm => 'Calm',
        Mood.focused => 'Focused',
        Mood.stressed => 'Stressed',
      };
}

sealed class ApiResult<T> {}

class Success<T> extends ApiResult<T> {
  final T data;
  Success(this.data);
}

class Failure<T> extends ApiResult<T> {
  final String message;
  Failure(this.message);
}

class Box<T> {
  final T value;
  Box(this.value);
}

typedef User = ({String name, int points, Mood mood});

ApiResult<List<User>> fetchUsers() {
  if (Random().nextBool()) {
    return Success([
      (name: 'Alex', points: 42, mood: Mood.focused),
      (name: 'Riley', points: 13, mood: Mood.calm),
    ]);
  }
  return Failure('Network error');
}

String? formatTopUser(List<User> users) {
  if (users.isEmpty) return null;
  final top = users.reduce((a, b) => a.points > b.points ? a : b);
  return '${top.name} (${top.points}) - ${top.mood.label}';
}

void main() {
  final result = fetchUsers();

  switch (result) {
    case Success<List<User>> s:
      final top = formatTopUser(s.data) ?? 'No users';
      final boxed = Box(top);
      print('Top user: ${boxed.value}');
    case Failure<List<User>> f:
      print('Failed: ${f.message}');
  }
}
```

What it demonstrates:
- **enum + extension**: readable labels
- **records**: lightweight user objects
- **sealed + pattern matching**: safe result handling
- **generics**: reusable Box and result types
- **null safety**: nullable return + fallback
