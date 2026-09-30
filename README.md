# Android Activity Lifecycle Demo

## Experiment Title

**Implement Android Activity Lifecycle Using Lifecycle Methods**

---

## Aim

To implement and demonstrate the different lifecycle methods of an Android Activity using Kotlin in Android Studio.

---

## Objective

The objective of this experiment is to understand the Android Activity Lifecycle and observe how an Activity changes its state during different user actions such as launching, minimizing, reopening, and closing the application.

---

## Technologies Used

* **Android Studio**
* **Kotlin**
* **XML**
* **Android SDK**
* **Gradle**

---

## Concept / Technology

An Android Activity has a lifecycle that describes the different states an Activity goes through during its execution.

The main Activity lifecycle methods used in this experiment are:

### 1. `onCreate()`

Called when the Activity is created for the first time. It is commonly used to initialize the Activity and load the layout.

### 2. `onStart()`

Called when the Activity becomes visible to the user.

### 3. `onResume()`

Called when the Activity becomes active and the user can interact with it.

### 4. `onPause()`

Called when the Activity is partially covered or is about to move into the background.

### 5. `onStop()`

Called when the Activity is no longer visible to the user.

### 6. `onRestart()`

Called when a stopped Activity is about to start again.

### 7. `onDestroy()`

Called before the Activity is destroyed.

---

## Activity Lifecycle Flow

```text
        onCreate()
             ↓
        onStart()
             ↓
        onResume()
             ↓
        Activity Running
             ↓
        onPause()
             ↓
        onStop()
             ↓
        onRestart()
             ↓
        onStart()
             ↓
        onResume()
```

When the Activity is completely closed:

```text
onPause()
    ↓
onStop()
    ↓
onDestroy()
```

---

## Scenario

A simple Android application named **Activity Lifecycle Demo** is developed.

The application displays:

* Student name
* USN
* Activity lifecycle events

The lifecycle events are displayed on the screen whenever the corresponding lifecycle methods are executed.

The application is tested by:

1. Launching the Activity.
2. Moving the application to the background and reopening it.
3. Closing the Activity using the Back button.

---

## Student Details

**Name:** SWARUPA S
**USN:** 25MCAR0091

---

## Project Folder Structure

```text
ActivityLifecycleDemo/
│
├── app/
│   │
│   └── src/
│       │
│       └── main/
│           │
│           ├── java/
│           │   └── com.example.activitylifecycledemo/
│           │       └── MainActivity.kt
│           │
│           ├── res/
│           │   ├── layout/
│           │   │   └── activity_main.xml
│           │   │
│           │   └── values/
│           │       ├── colors.xml
│           │       ├── strings.xml
│           │       └── themes.xml
│           │
│           └── AndroidManifest.xml
│
├── screenshots/
│   ├── testcase1.png
│   ├── testcase2.png
│   └── testcase3.png
│
├── README.md
├── build.gradle.kts
└── settings.gradle.kts
```

---

## Important Files

### `MainActivity.kt`

Contains the implementation of the Activity lifecycle methods:

```text
onCreate()
onStart()
onResume()
onPause()
onStop()
onRestart()
onDestroy()
```

### `activity_main.xml`

Contains the user interface of the application, including:

* Activity Lifecycle Demo title
* Student name
* USN
* Lifecycle event display

---

# Output

When the application is launched, the screen displays the student details and lifecycle events.

Example:

```text
Activity Lifecycle Demo

Name:   Devraath Joshi
USN: 25MCAR0

Lifecycle Events:

onCreate()
onStart()
onResume()
```

---

# Test Cases

## Test Case 1 – Launch Activity

### Test Objective

To verify the lifecycle methods executed when the Activity is launched.

### Action

Open the application.

### Expected Result

The following lifecycle methods should be executed:

```text
onCreate()
onStart()
onResume()
```

### Screenshot

![Test Case 1](screenshots/testcase1.png)

This test case also displays the student's **Name and USN**.

---

## Test Case 2 – Background and Reopen Activity

### Test Objective

To verify the lifecycle methods executed when the Activity is moved to the background and reopened.

### Action

1. Open the application.
2. Press the Home button.
3. Open the application again.

### Expected Result

The following lifecycle methods are observed:

```text
onPause()
onStop()
onRestart()
onStart()
onResume()
```

### Screenshot


<img width="1856" height="992" alt="image" src="https://github.com/user-attachments/assets/9caa76a9-637a-4c27-9baf-9a58e3207293" />

### Expected Result

The following lifecycle methods are observed:

```text
onPause()
onStop()
onDestroy()
```

### Screenshot

![Test Case 3](screenshots/testcase3.png)

---

# Screenshots

## Test Case 1

![Test Case 1](screenshots/testcase1.png)

## Test Case 2

![Test Case 2](screenshots/testcase2.png)

## Test Case 3

![Test Case 3](screenshots/testcase3.png)

---

# Learning Outcomes

After completing this experiment, the following concepts were understood:

* Android Activity Lifecycle
* Lifecycle callback methods
* Activity state changes
* Handling Activity creation and destruction
* Difference between foreground and background states
* Using Kotlin to implement lifecycle methods
* Testing Activity lifecycle behavior

---

# Conclusion

The Android Activity Lifecycle was successfully implemented using Kotlin in Android Studio. The lifecycle callback methods such as `onCreate()`, `onStart()`, `onResume()`, `onPause()`, `onStop()`, `onRestart()`, and `onDestroy()` were implemented and observed during different Activity states.

The experiment helped in understanding how Android manages an Activity when it is launched, moved to the background, reopened, and closed.
