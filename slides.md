---
layout: center
theme: default
---

**Table of contents**

<Toc />

---
layout: intro
theme: default
---

# Lecture 1, basics of the study module   

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

## Dart - Programming language of The chosen technology

*See the links to the videos on Moodle about the assignment!*

Dart documentation: https://dart.dev/docs
Package repository for Dart & Flutter libraries: https://pub.dev/

--- 

## First Flutter Application

1. Start with working on Google's codelab: https://docs.flutter.dev/get-started/codelab

We are going to use that code created in codelab as a base for our application: *Movie Match (or whatever you would like to call it!)*

_Example of a real-world flutter application, made in a DWELL project: https://github.com/MatiasHiltunen/dwellapp-example_

---

#### The App

The app we are building is going to have following features:

1. It loads a movie list from some movie api alongside the cover images for the movies, such as: https://developer.themoviedb.org/reference/intro/getting-started
2. Backend service (example [here](https://github.com/MatiasHiltunen/dart_movies_server)) that we can connect to get access to realtime API which allows us to register new account, singin with the account and then connect with a friend
   - Second phone/emulator can be used with testing/experimenting with features
4. Idea is to have an application that allows choosing a movie with a friend that you both would like to watch, and when first "match" happens, that shows on both devices as a "pop-up" that you have now a movie that you both would like to watch!

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
