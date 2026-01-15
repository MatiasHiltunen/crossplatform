---
layout: center
theme: default
---

**Table of contents**

<Toc maxDepth="2"/>

---
layout: intro
theme: default
---

# Cross-Platform Mobile Application Development

## New Course Structure (Starting 15.01.2026)

---

## Course Goal
Build solid foundations in cross-platform mobile development and deliver a working app with documented technical decisions, testing, and deployment considerations.

---

## Learning Outcomes
By the end of the course, the student can:
- Explain core cross-platform concepts and trade-offs.
- Set up a professional Flutter development environment from scratch.
- Understand Dart language fundamentals and apply them in Flutter.
- Implement a functional Flutter app with async data, state management, and error handling.
- Apply platform-specific UI/logic when needed.
- Test and document an app using unit and widget tests.

---

## Completion Paths
### Path 1: Lecture Track (Flutter only)
- Follow lectures and complete weekly exercises.
- Build a Movie Match style app with API data and real-time features.

### Path 2: Independent Track (Flutter only)
- Build an app from your own idea that matches course requirements.
- Use Flutter and Dart for all implementation.

---

## Weekly Schedule (Zoom)
| Date | Time | Topic | Focus |
|---|---|---|---|
| 15.01.2026 | 17:15 - 19:45 | Course basics + cross-platform fundamentals | Concepts, ecosystem overview, Flutter focus |
| 19.01.2026 | 17:15 - 19:45 | Tooling and environment setup | Flutter SDK, emulators, tooling checks |
| 28.01.2026 | 17:15 - 19:45 | Dart basics | Syntax, types, control flow, functions |
| 12.02.2026 | 17:15 - 19:45 | Flutter widgets + state basics | UI tree, stateful widgets, simple app |
| 24.03.2026 | 17:15 - 19:45 | Async and HTTP | Futures, REST, JSON, error handling |
| 01.04.2026 | 17:15 - 19:45 | Architecture + state management | Provider, separation of concerns |
| 09.04.2026 | 17:15 - 19:45 | Testing | Unit and widget tests, reporting results |
| 15.04.2026 | 17:15 - 19:45 | Platform-specific + deployment | Platform UI, channels, release basics |
| 22.04.2026 | 17:15 - 19:45 | Workshop | Debugging and project review |
| 06.05.2026 | 17:15 - 19:45 | Wrap-up | Final guidance and Q&A |

---

## Required Materials and Links
### Flutter and Dart
- Flutter install guide: https://docs.flutter.dev/get-started/install
- Flutter codelab: https://docs.flutter.dev/get-started/codelab
- Dart language tour: https://dart.dev/language
- Dart core libraries: https://api.dart.dev/stable/dart-core/dart-core-library.html
- Pub packages: https://pub.dev/

### Core Tooling
- Android Studio: https://developer.android.com/studio
- Git: https://git-scm.com/
- VS Code: https://code.visualstudio.com/
  - Flutter extension: https://marketplace.visualstudio.com/items?itemName=Dart-Code.flutter
  - Dart extension: https://marketplace.visualstudio.com/items?itemName=Dart-Code.dart-code

### API Data Source
- TMDB: https://www.themoviedb.org/
- API docs: https://developer.themoviedb.org/docs/getting-started

---

## Course Structure and Content
### Module 1: Foundations and Setup (Weeks 1-2)
**Goal:** Understand cross-platform concepts and get Flutter working locally.

**What you learn**
- Cross-platform vs native development
- Flutter architecture (Dart, widgets, rendering)
- Tooling setup and project structure
- Start the course project and make first UI changes

**Resources**
- Flutter overview: https://docs.flutter.dev/resources/architectural-overview
- Flutter CLI basics: https://docs.flutter.dev/reference/flutter-cli

**Setup checklist**
1. Install Flutter SDK.
2. Run `flutter doctor` and fix all issues.
3. Install Android Studio and create an emulator.
4. Verify `flutter doctor -v` shows no red errors.

---

### Module 2: Dart from Zero (Weeks 3-4)
**Goal:** Build Dart fundamentals needed for Flutter.

**What you learn**
- Variables, types, and null safety
- Lists, maps, and classes
- Functions, async basics, and error handling

**Resources**
- Dart language tour: https://dart.dev/language
- Effective Dart style: https://dart.dev/effective-dart/style

**Code snippet: variables and functions**
```dart
int add(int a, int b) {
  return a + b;
}

String formatUser(String name, int age) {
  return '$name is $age years old';
}

void main() {
  final total = add(2, 3);
  print(total);
  print(formatUser('Alex', 21));
}
```

**Code snippet: lists and maps**
```dart
final movies = ['Dune', 'Arrival', 'Interstellar'];
final ratings = {'Dune': 5, 'Arrival': 4};

void main() {
  movies.add('Blade Runner');
  print(movies[0]);
  print(ratings['Dune']);
}
```

---

### Module 3: Flutter UI Basics (Week 5)
**Goal:** Understand the widget tree and build simple UI.

**What you learn**
- Stateless vs Stateful widgets
- Layout with Row, Column, and Container
- Handling user input and state

**Resources**
- Widgets catalog: https://docs.flutter.dev/development/ui/widgets
- Layout basics: https://docs.flutter.dev/development/ui/layout

**Code snippet: simple counter**
```dart
class CounterPage extends StatefulWidget {
  const CounterPage({super.key});
  @override
  State<CounterPage> createState() => _CounterPageState();
}

class _CounterPageState extends State<CounterPage> {
  int count = 0;

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: const Text('Counter')),
      body: Center(
        child: Text('Count: $count', style: const TextStyle(fontSize: 24)),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: () => setState(() => count++),
        child: const Icon(Icons.add),
      ),
    );
  }
}
```

---

### Module 4: Async and HTTP (Week 6)
**Goal:** Fetch data from APIs and handle asynchronous flows.

**What you learn**
- async/await and Futures
- HTTP requests and JSON decoding
- Loading and error states

**Resources**
- Async guide: https://dart.dev/codelabs/async-await
- HTTP package: https://pub.dev/packages/http

**Code snippet: fetch data**
```dart
import 'dart:convert';
import 'package:http/http.dart' as http;

Future<List<dynamic>> fetchMovies(String apiKey) async {
  final url = Uri.parse(
    'https://api.themoviedb.org/3/movie/popular?api_key=$apiKey',
  );
  final response = await http.get(url);

  if (response.statusCode != 200) {
    throw Exception('Failed to load movies');
  }

  final data = jsonDecode(response.body) as Map<String, dynamic>;
  return data['results'] as List<dynamic>;
}
```

---

### Module 5: Architecture and State Management (Week 7)
**Goal:** Organize code and manage state cleanly.

**What you learn**
- Folder structure and separation of concerns
- Provider pattern
- Data flow from services to UI

**Resources**
- Provider package: https://pub.dev/packages/provider
- App architecture concepts: https://docs.flutter.dev/app-architecture/concepts

**Code snippet: provider setup**
```dart
class MoviesProvider with ChangeNotifier {
  final List<dynamic> _movies = [];
  bool _loading = false;

  List<dynamic> get movies => _movies;
  bool get loading => _loading;

  Future<void> loadMovies(String apiKey) async {
    _loading = true;
    notifyListeners();
    try {
      final results = await fetchMovies(apiKey);
      _movies
        ..clear()
        ..addAll(results);
    } finally {
      _loading = false;
      notifyListeners();
    }
  }
}
```

---

### Module 6: Testing (Week 8)
**Goal:** Validate logic and UI with tests.

**What you learn**
- Unit tests for functions and services
- Widget tests for UI rendering
- Reporting results

**Resources**
- Flutter testing: https://docs.flutter.dev/testing
- Flutter test package: https://api.flutter.dev/flutter/flutter_test/flutter_test-library.html

**Code snippet: unit test**
```dart
import 'package:flutter_test/flutter_test.dart';

int add(int a, int b) => a + b;

void main() {
  test('add returns correct sum', () {
    expect(add(2, 3), 5);
  });
}
```

---

### Module 7: Platform-Specific and Deployment (Week 9)
**Goal:** Add platform-specific behavior and understand release basics.

**What you learn**
- Platform checks
- Cupertino vs Material
- Release build basics

**Resources**
- Platform integration: https://docs.flutter.dev/platform-integration
- Platform class: https://api.flutter.dev/flutter/dart-io/Platform-class.html

**Code snippet: platform UI**
```dart
import 'dart:io' show Platform;
import 'package:flutter/cupertino.dart';
import 'package:flutter/material.dart';

Widget platformButton(VoidCallback onPressed) {
  return Platform.isIOS
      ? CupertinoButton(child: const Text('OK'), onPressed: onPressed)
      : ElevatedButton(onPressed: onPressed, child: const Text('OK'));
}
```

---

### Module 8: Workshop and Finalization (Week 10)
**Goal:** Debug, polish, and finalize documentation.

**What you learn**
- Debugging workflow
- Performance basics
- Final submission quality check

---

## Weekly Tasks (Path 1)
### Task 1: Course Baseline
- Answer: What is cross-platform development?
- List known frameworks
- Self-assess web and OOP knowledge
- Create a Git repo and initialize the Flutter project
- Run the app and make one small UI change

### Task 2: Environment Setup
- Install Flutter
- Run `flutter doctor` and capture result
- Create and run the Flutter counter app

### Task 3: Dart Basics
- Write a CLI app with functions, lists, and maps
- Explain variables, types, and control flow in the diary

### Task 4: First Flutter App
- Implement counter app with increment and decrement
- Explain widget tree and state

### Task 5: API Integration
- Fetch data from TMDB
- Display list with images
- Add error handling

### Task 6: Architecture
- Introduce Provider
- Separate UI, data, and state

### Task 7: Testing
- Add at least one unit test
- Add at least one widget test
- Include results in the learning diary

### Task 8: Platform-Specific
- Implement one platform-specific UI or logic
- Explain the reason and behavior

---

## Code Repository Requirement (Git)
- **All students must use Git and push code to a repository.**
- The repository is the evidence of your implementation progress.
- **Learning diary can be written in Markdown (`.md`) inside the repo.**
  - Example file name: `learning-diary.md`
  - If you use a repo-based diary, include screenshots and links in the file.

---

## Example Application (Required Features)
You may build a different app, but it must include these core features:
- **Two meaningful screens** (e.g., list view + detail view)
- **Remote data** (API or cloud database)
- **State management** (Provider or equivalent)
- **Error and loading states** (visible to user)
- **User input** (form, search, or selection)
- **Platform-specific element** (UI or behavior)
- **Testing evidence** (at least 1 unit test + 1 widget test)

---

## Path 2 Requirements (Independent)
Your project must include:
- Working app with at least 2 meaningful screens
- Async data usage (API, database, or file)
- Clear state management approach
- Error handling and recovery
- At least 1 unit test and 1 UI test
- Platform-specific consideration (UI or behavior)

---

## Learning Diary (80 Points)
To complete this course, a personal learning diary or report is required. It must be submitted as a single document (PDF or Word) or as a blog/vlog link with equivalent structure.

- **Follow** Lapland UAS learning diary guidelines.
- **Study Path 1**: Include assignments given in the lectures in the diary.
- **Study Path 2**: Include your own app idea, scope, and implementation plan.

### Completion Criteria (clear and measurable)
Your diary is complete when it includes all of the following:
- **Required sections** listed below
- **All lecture checklists** (L1-L10)
- **Required screenshots** with technical explanations
- **Evidence of working implementation** (code snippets + app screenshots)

### Required structure (use these headings)
- **Cover + table of contents**
- **Weekly log** (per session or per study week)
  - What you implemented
  - Key technical decisions (with justification)
  - Problems encountered and how you solved them
  - Next steps
- **Implementation chapter**
  - Project structure and architecture
  - State management approach
  - Data flow and API usage
  - Testing strategy and results
- **Self-assessment**
  - Before/after competence reflection
  - What you would do differently next time

### Mandatory screenshots (include explanation under each)
1. **Development environment setup** (e.g. `flutter doctor` output, SDK install, emulator setup)
2. **App running on device/emulator** (with your UI visible)
3. **Data/API integration** (e.g. API response, network log, or devtools)
4. **State management or architecture** (diagram or code excerpt + UI behavior)
5. **Testing results** (unit/widget tests, optional integration test)

> Each required screenshot must include a short technical explanation (what it proves and how it works).

---

## Lecture-by-Lecture Diary Checklist (Path 1)
These items are **required** in the diary and are graded directly by the rubric.

### Lecture 1
- Your definition of cross-platform development
- Native vs cross-platform comparison
- Why Flutter for this course (2-3 sentences)
- Personal learning goals (3-5 bullets)

### Lecture 2
- Setup steps summary
- `flutter doctor -v` screenshot + fixes
- Emulator/device running starter app
- One setup problem and solution

### Lecture 3
- CLI app code snippet (functions, lists, maps)
- Explanation of `final` vs `var` and null safety
- Class example and usage
- CLI app output screenshot

### Lecture 4
- Counter app screenshot
- Widget tree explanation (top 3-5 widgets)
- Stateless vs Stateful difference
- `setState` usage explanation

### Lecture 5
- `async`/`await` explanation
- API request snippet
- Screenshot of loading + results
- Error handling explanation

### Lecture 6
- Folder structure (screenshot or tree)
- Provider snippet + explanation
- Data flow explanation
- One design decision and rationale

### Lecture 7
- Unit test and widget test descriptions
- Test file locations
- Test results screenshot

### Lecture 8
- Platform-specific code snippet + explanation
- Build command used (APK/iOS) + output screenshot
- Platform limitation or difference noted

### Lecture 9
- Bug list with fixes (min 2)
- Before/after screenshot for one fix
- One UX or performance improvement

### Lecture 10
- Final feature list
- Self-evaluation against rubric
- Future improvements list

---

## Why These Topics Matter (Learning Justification)
Each module builds real-world skills needed in mobile development and supports employability:

- **Foundations & Setup:** You learn how to create a reliable development environment. This prevents wasted time and is expected in professional teams.
- **Dart Basics:** You must understand the language to read, debug, and extend Flutter code safely.
- **Flutter UI + State:** UI structure and state are the core of app behavior. Without these, apps cannot be interactive or maintainable.
- **Async + HTTP:** Modern apps depend on data from APIs. Knowing async patterns avoids crashes and broken UI.
- **Architecture + State Management:** Good structure makes features easier to add and reduces bugs as the project grows.
- **Testing:** Tests prove your code works and protect against regressions, which is required in professional workflows.
- **Platform-Specific + Deployment:** Real apps must respect platform differences and be built for release.
- **Workshop + Finalization:** Debugging and polishing are the difference between a prototype and a usable product.

---

## Grading
### **Learning Diary**
- Maximum of 80 points.
- **Study Path 1**: Evaluated based on quality of implementation, completion of assignments, and depth of technical understanding.
- **Study Path 2**: Evaluated based on technical implementation, scope, and depth of understanding.

### AI Policy (Required)
- **Disclosure required:** If you used AI, you must describe how you used it.
- **Model required:** Name the AI model or models (e.g., GPT-4, Claude, etc.).
- **Grading impact:** The quality of AI usage description affects grading (clarity, honesty, and technical understanding).
- **Mandatory question:** Answer in your diary:
  - **Did you use AI? If yes, how? If no, state that clearly.**

### Rubric (80 points total)
| Area | Points | What is evaluated |
|---|---:|---|
| Lecture deliverables (L1-L10) | 30 | All required diary items completed with evidence |
| Core app functionality | 20 | Features work as described, correct UI behavior, meaningful scope |
| Architecture & state management | 10 | Clear structure, justified choices, maintainable code |
| Data & async flows | 8 | API usage, error handling, async patterns explained |
| Testing | 6 | Unit/widget tests written, results reported |
| Platform-specific or deployment | 6 | Platform-specific UI/logic or deployment steps |
| **Bonus: writing clarity & visuals** | **+5** | Clear writing, grammar, visuals, and presentation |

### **Extras**
- Smaller tasks to increase your grade by up to 30 points.

**Points to Grade:**
- 40 points -> Grade 1
- 50 points -> Grade 2
- 60 points -> Grade 3
- 70 points -> Grade 4
- 80 points -> Grade 5

---

## Submission
- Learning diary or blog/vlog link submitted to Moodle by the deadline.
- Include all required screenshots and technical explanations.
- Clearly label Path 1 or Path 2 in the submission.
