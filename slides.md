---
layout: center
theme: default
---

**Table of contents**

<Toc maxDepth="1"/>

---
layout: intro
theme: default
---

# Lecture 1, basics of the study module, eg. Schedule

### Cross-Platform Mobile Application Development



---

## Assignments

- ### **Learning Diary (80 Points)**
-- To complete this course, a personal learning diary or report is required.
- ### **Extras (30 Points)**
-- Smaller tasks to complement the learning diary will be published later.

#### _Total of 110 points available_
---


## Learning Diary (80 Points)

To complete this course, a personal learning diary or report is required:

- **Follow** Lapland UAS learning diary guidelines.
- **Minimum length**: 10 pages.
- **Encouraged**: Extensive use of images and code samples.
- **Include**:
  - Instructions for setting up the development environment.
  - Steps to get your application running.
  - Self-assessment before and after development.
  - Reflections on your learning and its impact on your future career.
  - Clear explanations of development choices and learning outcomes.
  - Visualized architecture of your application.
- **Study Path 1**: Include assignments given in the lectures.

**Alternatively, you may keep a **blog** or **vlog** as your learning diary.**

---


## Grading

### **Learning Diary**
- Maximum of 80 points.
- **Study Path 1**: Evaluated based on quality, amount of work, and completion of assignments.
- **Study Path 2**: Evaluated based on the quality and amount of work.

### **Extras**
- Smaller tasks to increase your grade by up to 30 points.

**Points to Grade:**
- 40 points ➔ Grade 1
- 50 points ➔ Grade 2
- 60 points ➔ Grade 3
- 70 points ➔ Grade 4
- 80 points ➔ Grade 5

> Example: With 79.5 points, the grade is **4**.

---

## Schedule

<div class="table-container">
<table>
  <thead>
    <tr>
      <th>Date</th>
      <th>Time</th>
      <th>Location</th>
      <th>Topic</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>21.01.2025</td>
      <td>08:15 - 11:45</td>
      <td>B243</td>
      <td>Basics of cross-platform mobile development</td>
    </tr>
    <tr>
      <td>28.01.2025</td>
      <td>08:15 - 11:45</td>
      <td>B243</td>
      <td>Hands-on cross-platform development</td>
    </tr>
    <tr>
      <td>04.02.2025</td>
      <td>08:15 - 11:45</td>
      <td>B243</td>
      <td>Programming language of chosen technology</td>
    </tr>
    <tr>
      <td>20.02.2025</td>
      <td>08:15 - 11:45</td>
      <td>B243</td>
      <td>First cross-platform mobile application</td>
    </tr>
    <tr>
      <td>27.02.2025</td>
      <td>08:15 - 11:45</td>
      <td>B243</td>
      <td>Best practices with chosen technology</td>
    </tr>
    <tr>
      <td>12.03.2025</td>
      <td>12:30 - 16:00</td>
      <td>B243</td>
      <td>Workshop</td>
    </tr>
    <tr>
      <td>20.03.2025</td>
      <td>08:15 - 11:45</td>
      <td>B243</td>
      <td>Platform-specific code</td>
    </tr>
    <tr>
      <td>27.03.2025</td>
      <td>08:15 - 11:45</td>
      <td>B243</td>
      <td>Testing the application</td>
    </tr>
    <tr>
      <td>03.04.2025</td>
      <td>08:15 - 11:45</td>
      <td>B243</td>
      <td>Deployment to production</td>
    </tr>
    <tr>
      <td>17.04.2025</td>
      <td>08:15 - 11:45</td>
      <td>B243</td>
      <td>Wrap-up and final guidance</td>
    </tr>
  </tbody>
</table>
</div>

---

## Study Paths
<br/>

### **1. Lecture sets**
- Complete the course by following lectures and completing the assignments.

<br/>


### **2. Independent Study**
- Choose a cross-platform mobile application technology/framework.
- Develop an application that meets given requirements.

> **Main Goal:** Develop a mobile application that is meaningful to you. Examples include tools, games, or problem-solving applications.

---

## Instructor

**Matias Hiltunen**  
[matias.hiltunen@lapinamk.fi](mailto:matias.hiltunen@lapinamk.fi)  

Best way to contact me is through Teams or email!

---

## First task

_Answer how you currently understand the terms_

#### 1. What is cross-platform development?

#### 2. What cross-platform technologies do you know currently? 

#### 3. How would you describe your knowledge of Web technologies?

#### 5. How would you describe your knowledge of object-oriented languages? 

---

# Lecture 2, Flutter & React Native 


<br/>

### hands-on experience of the most used cross-platform development tools


Requirements:

> Install latest versions 

- Android Studio, https://developer.android.com/studio
- Git, https://git-scm.com/
- NodeJs, https://nodejs.org/en
- VSCode (recommended), https://code.visualstudio.com/

React Native: https://reactnative.dev/docs/set-up-your-environment

Flutter: https://docs.flutter.dev/get-started/install

-- _React Native and Flutter setup will be done together on lecture_

---

## Assignment of the lecture

### Setup both, Flutter and React Native development environments

**Using starter applications of each technology:**

1. Modify the code to create two simple buttons to the view

2. Apply state modifiers so that one button increments and other button decrements displayed value

3. Add comparison to learning diary (or blog) of the state management approaches of Flutter and React Native.

4. Search for more information about the differences between React Native and Flutter, add summary of the differences to learning diary.

--- 

## Voting for the Path 1 technology

*Flutter was chosen to Path 1's cross-platform development framework!*

---

# Lecture 3, Dart - Programming language of The chosen technology

*See the links to the videos on Moodle about the assignment!*

Dart documentation: https://dart.dev/docs
Package repository for Dart & Flutter libraries: https://pub.dev/

--- 

# Lecture 4, First Flutter Application

1. Start with working on Google's codelab: https://docs.flutter.dev/get-started/codelab

We are going to use that code created in codelab as a base for our application: *Movie Match (or whatever you would like to call it!)*

Example of a real-world flutter application (Proof of Consept), made in a DWELL project: https://github.com/MatiasHiltunen/dwellapp-example

---

#### The App

The app we are building is going to have following features:

1. It loads a movie list from some movie api alongside the cover images for the movies, such as: https://developer.themoviedb.org/reference/intro/getting-started
2. Backend service (example [here](https://github.com/MatiasHiltunen/dart_movies_server)) that we can connect to get access to realtime API which allows us to register new account, singin with the account and then connect with a friend
   - Second phone/emulator can be used with testing/experimenting with features
4. Idea is to have an application that allows choosing a movie with a friend that you both would like to watch, and when first "match" happens, that shows on both devices as a "pop-up" that you have now a movie that you both would like to watch!

---

# Lecture 5, Async Dart with Flutter

### Adding movie data to our Flutter application

---

## TMDB API Access


- **Link**: [https://www.themoviedb.org/](https://www.themoviedb.org/)
- **API Documentation**: [https://developer.themoviedb.org/docs/getting-started](https://developer.themoviedb.org/docs/getting-started)


## API Access Keys

API Read Access Key is available in Moodle

---

## Flutter & Dart Documentation

### Asynchronous Programming
- **Dart Async**: [https://dart.dev/codelabs/async-await](https://dart.dev/codelabs/async-await)
- **Futures and Error Handling**: [https://dart.dev/guides/libraries/futures-error-handling](https://dart.dev/guides/libraries/futures-error-handling)
- **Streams**: [https://dart.dev/tutorials/language/streams](https://dart.dev/tutorials/language/streams)

### HTTP & JSON
- **HTTP Package**: [https://pub.dev/packages/http](https://pub.dev/packages/http)
- **JSON and Serialization**: [https://docs.flutter.dev/data-and-backend/json](https://docs.flutter.dev/data-and-backend/json)

---

## Lecture Code Resources

- **Starting point**: Google Code lab's "First Flutter Application" 
  - [https://github.com/flutter/codelabs/blob/main/namer/step_08/lib/main.dart](https://github.com/flutter/codelabs/blob/main/namer/step_08/lib/main.dart)

- **Refactored code** based on that is available here: 
  - [https://github.com/MatiasHiltunen/moviematch](https://github.com/MatiasHiltunen/moviematch)


## Implementation Notes

- If you clone the application code from repository, **add the Read Access API key** to `providers/app_state.dart`

- We also tried running the Flutter app on a real device, guide here: 
  - [https://docs.flutter.dev/get-started/install/windows/mobile#configure-your-target-android-device](https://docs.flutter.dev/get-started/install/windows/mobile#configure-your-target-android-device)


---

## Async/Await Basics

```dart
// Simple async function
Future<String> fetchData() async {
  await Future.delayed(Duration(seconds: 1));
  return "Data loaded";
}

// Using it
void loadData() async {
  var result = await fetchData();
  print(result);
}
```

---

## Explanation: Async/Await

- **async** keyword marks a function that returns a Future
- **await** pauses execution until the Future completes
- Code after await runs only when the Future is resolved
- `Future.delayed` simulates a network request or database query
- Without async/await, you would need to use callbacks or .then()

**Documentation**: [https://dart.dev/codelabs/async-await](https://dart.dev/codelabs/async-await)

---

## HTTP Request

```dart
import 'package:http/http.dart' as http;
import 'dart:convert';

// Fetch movies
Future<List> getMovies(String apiKey) async {
  final url = 'https://api.themoviedb.org/3/movie/popular?api_key=$apiKey';
  final response = await http.get(Uri.parse(url));
  
  if (response.statusCode == 200) {
    return jsonDecode(response.body)['results'];
  } else {
    throw Exception('Failed to load movies');
  }
}
```

---

## Explanation: HTTP Request

- **http package** provides functions to make API calls
- **await http.get()** sends a GET request and waits for response
- **jsonDecode** converts the JSON string to Dart objects
- **statusCode == 200** checks if request was successful
- **throw Exception** handles errors in a way that can be caught
- The function returns a Future that will eventually contain movie data

**Documentation**: [https://pub.dev/packages/http/example](https://pub.dev/packages/http/example)

---

## FutureBuilder

```dart
FutureBuilder<List>(
  future: getMovies(apiKey),
  builder: (context, snapshot) {
    // Loading
    if (snapshot.connectionState == ConnectionState.waiting) {
      return CircularProgressIndicator();
    }
    
    // Error
    if (snapshot.hasError) {
      return Text('Error: ${snapshot.error}');
    }
    
    // Success
    final movies = snapshot.data!;
    return ListView.builder(
      itemCount: movies.length,
      itemBuilder: (context, index) => ListTile(
        title: Text(movies[index]['title']),
      ),
    );
  },
)
```

---

## Explanation: FutureBuilder

- **FutureBuilder** automatically handles different states of a Future
- **snapshot.connectionState** tells you if data is still loading
- **snapshot.hasError** checks if an error occurred
- **snapshot.data** contains the result when the Future completes
- The widget rebuilds automatically when the Future's state changes
- Perfect for one-time data fetching operations

**Documentation**: [https://api.flutter.dev/flutter/widgets/FutureBuilder-class.html](https://api.flutter.dev/flutter/widgets/FutureBuilder-class.html)

---

## StreamBuilder

```dart
// Simple counter stream
Stream<int> countStream() async* {
  for (int i = 1; i <= 5; i++) {
    await Future.delayed(Duration(seconds: 1));
    yield i;
  }
}

// Usage
StreamBuilder<int>(
  stream: countStream(),
  builder: (context, snapshot) {
    if (!snapshot.hasData) return Text('Loading...');
    
    return Text(
      'Count: ${snapshot.data}',
      style: TextStyle(fontSize: 24),
    );
  },
)
```

---

## Explanation: StreamBuilder

- **Stream** provides a sequence of asynchronous events (like a continuous Future)
- **async*** marks a function that returns a Stream
- **yield** emits values to the stream one at a time
- **StreamBuilder** rebuilds UI whenever new values arrive in the stream
- Great for real-time data, user input, or any continuous data flow
- Used for websockets, location updates, form validation, etc.

**Documentation**: [https://api.flutter.dev/flutter/widgets/StreamBuilder-class.html](https://api.flutter.dev/flutter/widgets/StreamBuilder-class.html)

---

## Provider Pattern

```dart
// Provider class
class MoviesProvider with ChangeNotifier {
  List _movies = [];
  bool _loading = false;
  
  List get movies => _movies;
  bool get loading => _loading;
  
  Future<void> fetchMovies(String apiKey) async {
    _loading = true;
    notifyListeners();
    
    try {
      _movies = await getMovies(apiKey);
    } finally {
      _loading = false;
      notifyListeners();
    }
  }
}

// Setup in main.dart
ChangeNotifierProvider(
  create: (_) => MoviesProvider(),
  child: MyApp(),
)
```

---

## Explanation: Provider Pattern

- **ChangeNotifier** is a class that provides change notifications to listeners
- **notifyListeners()** tells widgets to rebuild when data changes
- **ChangeNotifierProvider** makes the state available throughout the widget tree
- Provider separates business logic from UI code
- Centralized state management prevents "prop drilling"
- Helps maintain clean application architecture

**Documentation**: [https://pub.dev/packages/provider](https://pub.dev/packages/provider)

---

## Consumer Widget

```dart
Consumer<MoviesProvider>(
  builder: (ctx, provider, _) {
    // Show loading indicator
    if (provider.loading) {
      return CircularProgressIndicator();
    }
    
    // Show movie list
    return ListView.builder(
      itemCount: provider.movies.length,
      itemBuilder: (ctx, i) => ListTile(
        title: Text(provider.movies[i]['title']),
      ),
    );
  },
)
```

---

## Explanation: Consumer Widget

- **Consumer** rebuilds only when specific provider data changes
- More efficient than rebuilding the entire widget tree
- The **builder** function receives the provider instance
- Automatically listens to changes from notifyListeners()
- Can be nested to consume multiple providers
- Works with any widget, not just lists

**Documentation**: [https://pub.dev/documentation/provider/latest/provider/Consumer-class.html](https://pub.dev/documentation/provider/latest/provider/Consumer-class.html)

---

## Error Handling

```dart
try {
  // Show loading state
  setState(() => loading = true);
  
  // API call
  final movies = await getMovies(apiKey);
  setState(() {
    this.movies = movies;
    error = null;
  });
} catch (e) {
  setState(() => error = 'Failed to load movies');
  print('Error: $e'); // Log for debugging
} finally {
  setState(() => loading = false);
}
```

---

## Explanation: Error Handling

- **try/catch/finally** pattern handles errors gracefully
- **setState()** updates UI based on different states
- **catch** block captures any errors from the try block
- **finally** always executes, ensuring loading state is reset
- Good error handling improves user experience
- Logging errors helps with debugging

**Documentation**: [https://dart.dev/guides/libraries/futures-error-handling](https://dart.dev/guides/libraries/futures-error-handling)

---

# Lecture 6, Workshop 

## Workshop Extra Task
 
This task is evaluated as complementary to the learning Diary (max 10p, around 2-3 pages to get max points)
 
- Flutter apps are traditionally built entirely by crafting the code that creates the UI. There are however multiple visual building tools for Flutter applications. 

- Search for graphical Flutter App building tools and choose one for this task.
 
Task: Familiarize with one of the graphical Flutter App building tools.
 
- _Recommended graphical Flutter App building tool: [flutterflow](https://www.flutterflow.io/)_
 
- This task helps you to understand how the flutter widget tree 
  is actually forming the User Interface. 
- Task introduces a way how you'll get easy hands-on 
  experience about different, readily available Widgets!
 
Remember to update your learning diary/blog about what you found about visual building tools with Flutter!
---

# Lecture 7, Platform-specific Code

### Understanding and implementing platform-specific features in Flutter

---

## Documentation Links

### Platform-Specific Code
- **Platform Class**: [https://api.flutter.dev/flutter/dart-io/Platform-class.html](https://api.flutter.dev/flutter/dart-io/Platform-class.html)
- **Platform Integration**: [https://docs.flutter.dev/platform-integration](https://docs.flutter.dev/platform-integration)

### UI Components
- **Cupertino (iOS-style)**: [https://docs.flutter.dev/development/ui/widgets/cupertino](https://docs.flutter.dev/development/ui/widgets/cupertino)
- **Material (Android-style)**: [https://docs.flutter.dev/development/ui/widgets/material](https://docs.flutter.dev/development/ui/widgets/material)

---

## Cross-Platform Development Challenges

### Native Languages & Hardware

| Platform | Native Languages | Hardware |
|----------|-----------------|-----------|
| iOS | Objective-C, Swift | Apple proprietary |
| Android | Kotlin, Java, C++, Rust | Wide variety |
| Web | JavaScript | Web Browsers |

---

## Flutter's Approach

- Flutter uses a rendering engine to abstract away native code
- Allows same codebase across platforms
- Sometimes manual implementation needed for specific features
  - Example: Apple's LiDAR sensor
  - Platform-specific UI elements
  - Native system dialogs

**Learn more**: [Flutter Architectural Overview](https://docs.flutter.dev/resources/architectural-overview)

---

## Simple Platform Check

```dart
import 'dart:io' show Platform;

// Basic platform check
if (Platform.isIOS) {
  print('Running on iOS');
} else if (Platform.isAndroid) {
  print('Running on Android');
}
```

**Documentation**: [Platform Class](https://api.flutter.dev/flutter/dart-io/Platform-class.html)

---

## Platform-Specific Button

```dart
Widget getPlatformButton() {
  return Platform.isIOS
    ? CupertinoButton(
        child: Text('OK'),
        onPressed: () {},
      )
    : ElevatedButton(
        child: Text('OK'),
        onPressed: () {},
      );
}
```

**Documentation**:
- [CupertinoButton](https://api.flutter.dev/flutter/cupertino/CupertinoButton-class.html)
- [ElevatedButton](https://api.flutter.dev/flutter/material/ElevatedButton-class.html)

---

## Platform-Specific Dialog

```dart
void showPlatformDialog(BuildContext context) {
  if (Platform.isIOS) {
    showCupertinoDialog(
      context: context,
      builder: (_) => CupertinoAlertDialog(
        title: Text('iOS Alert'),
        actions: [
          CupertinoDialogAction(
            child: Text('OK'),
            onPressed: () => Navigator.pop(context),
          ),
        ],
      ),
    );
  } else {
    showDialog(/* ... */);
  }
}
```

**Documentation**:
- [showCupertinoDialog](https://api.flutter.dev/flutter/cupertino/showCupertinoDialog.html)
- [showDialog](https://api.flutter.dev/flutter/material/showDialog.html)

---

## Platform-Specific UI Components

```dart
Widget buildInput() {
  return Platform.isIOS
    ? CupertinoTextField(
        placeholder: 'iOS Input',
      )
    : TextField(
        decoration: InputDecoration(
          hintText: 'Android Input',
        ),
      );
}
```

**Documentation**:
- [CupertinoTextField](https://api.flutter.dev/flutter/cupertino/CupertinoTextField-class.html)
- [TextField](https://api.flutter.dev/flutter/material/TextField-class.html)

---

## Best Practices

1. **Abstract Platform Code**
   - Create wrappers for platform-specific code
   - Use factory patterns for widgets

2. **User Experience**
   - Follow platform design guidelines
   - Maintain feature parity

3. **Testing**
   - Test on both platforms
   - Verify platform behaviors

**Learn more**: [Platform Integration](https://docs.flutter.dev/platform-integration)

---

## Platform Channels

For native functionality:

```dart
const platform = MethodChannel('app/platform');

// Call native code
try {
  final result = await platform.invokeMethod('getNativeFeature');
  print('Result: $result');
} catch (e) {
  print('Error: $e');
}
```

**Documentation**: [Writing custom platform-specific code](https://docs.flutter.dev/platform-integration/platform-channels)

---

<style>




.table-container {
    margin: 20px auto;
    font-size: 0.9em;
    border-collapse: collapse;
    width: 80%;
    overflow-x: auto;
}

.table-container th, .table-container td {
    text-align: left;
    padding: 8px;
}

</style>
