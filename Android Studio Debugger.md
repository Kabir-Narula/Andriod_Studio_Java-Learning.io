
# Android Studio Debugger: Detailed Cheat Sheet

In this detailed cheat sheet, we walk through the key concepts, tools, and techniques for using the Android Studio debugger effectively. Learn about breakpoints, stepping through code, inspecting variables, and more, along with practical tips for debugging Android apps.

---

## **About Debugging**

**Debugging** is the process of identifying and fixing errors or unexpected behavior in your code. Common debugging tools in Android Studio include:
- **Logcat**: Displays log messages to track errors and execution flow.
- **Debugger Pane**: Displays frames, threads, variables, and the call stack.
- **Debug Mode**: Allows you to run apps with breakpoints to pause execution and inspect state.
- **Test Frameworks**: Includes tools like JUnit or Espresso.
- **Dalvik Debug Monitor Server (DDMS)**: Tracks resource usage like memory and CPU.

---

## **Running the Debugger**

There are two primary ways to run the debugger in Android Studio:

1. **Run your app in debug mode**:
   - Click the **Debug** icon from the toolbar.
   - Android Studio builds the APK, installs it on the selected device, and runs the app in debug mode.

   You can view the following panes:
   - **Frames Pane**: Displays the current call stack of the app, showing all methods invoked.
   - **Variables Pane**: Shows the variables in scope and their current values.
   - **Watches Pane**: Allows you to monitor specific variables or expressions.

2. **Attach the debugger to a running app**:
   - Go to `Run > Attach debugger to Android process` or click the **Attach** icon in the toolbar.
   - Select the app process to which you want to attach the debugger.

---

## **Breakpoints: Essential Tool for Debugging**

### **Adding Breakpoints**
A **breakpoint** pauses the execution of your code at a specific line. Use it to inspect variables, evaluate expressions, or troubleshoot issues.

- **To add a breakpoint**:
  - Click in the left gutter of the editor next to the line of code where you want to pause.
  - A red dot will appear, indicating a breakpoint has been set.
  
### **Conditional Breakpoints**
Conditional breakpoints only trigger if a certain condition evaluates to `true`.

- **To set a conditional breakpoint**:
  - Right-click a breakpoint and add a condition (e.g., `i > 5`).

### **View and Configure Breakpoints**
- Click the **View Breakpoints** icon to view all breakpoints and configure their behavior (e.g., enable/disable, set conditions).

### **Disable or Mute Breakpoints**
- **Mute** all breakpoints: Click the **Mute Breakpoints** icon in the toolbar to temporarily disable all breakpoints.

---

## **Stepping Through Code**

Once your app is paused at a breakpoint, you can step through your code line by line:

- **Step Over (F8)**: Executes the next line but skips over method calls.
- **Step Into (F7)**: Jumps into a method call and shows its execution.
- **Step Out (Shift + F8)**: Completes the current method and returns to the calling method.

### **Use Case Example:**
- Pausing execution inside a loop and stepping through iterations to check the state of variables in each pass.

---

## **Viewing Execution Stack Frames**

The **Frames Pane** shows the execution stack (call stack) of the app, with each class and method called in reverse order. Each frame represents an active method call.

- **To view a frame**: Click on any method in the Frames Pane to open the associated source code file and highlight the line where the method was invoked.

---

## **Inspecting and Modifying Variables**

### **Inspect Variables**
The **Variables Pane** shows all variables in the current scope and their values. For objects and arrays, you can expand them to inspect their properties or elements.

### **Modify Variables**
You can change variable values during runtime to see how the app behaves with different inputs.

- **To modify a variable**:
  - Right-click on a variable in the Variables Pane and choose **Set Value**.
  - Enter a new value and press Return.

---

## **Setting Watches**

Watches let you monitor specific variables or expressions over the duration of the debugging session.

- **To set a watch**:
  - Click the **Show Watches** icon, and then click the plus (+) button.
  - Enter the variable name or expression and press Enter.

Watches are useful for tracking the state of critical variables, especially those that are used frequently in loops or methods.

---

## **Evaluating Expressions**

The **Evaluate Expression** feature lets you execute expressions or call methods on the fly.

- **To evaluate an expression**:
  - Click the **Evaluate Expression** icon or use `Run > Evaluate Expression`.
  - Enter any Java expression, then click **Evaluate** to see the result.

You can even manipulate object properties or call methods within the current scope.

---

## **More Debugging Tools**

### **System Log (Logcat Pane)**
The **Logcat Pane** displays log messages that you can filter to find specific tags, errors, or warnings.

- **Writing logs in your code**:
  ```java
  Log.d("TAG", "Debug message");
  ```

### **Trace Logging**
**Method tracing** is a tool that shows how long methods take to execute. You can create trace files and analyze them in **Traceview**.

- **Start tracing**:
  ```java
  Debug.startMethodTracing("traceFile");
  ```

- **Stop tracing**:
  ```java
  Debug.stopMethodTracing();
  ```

### **Android Profiler**
Android Studio provides real-time data about CPU, memory, and network usage. You can use the **CPU Profiler** to record method traces and inspect thread activity, while the **Network Profiler** allows you to examine network traffic.

---

## **Best Practices for Debugging**

1. **Log strategically**: Avoid overusing `Log.d` or `Log.e` as it can clutter the logcat. Instead, log critical checkpoints and error states.
2. **Use conditional breakpoints**: If you’re dealing with loops or repetitive tasks, set conditions on breakpoints to reduce debugging time.
3. **Test edge cases**: Set breakpoints near the boundary conditions in your code (e.g., array limits, null values).
4. **Profile often**: Use Android Profiler to monitor memory and CPU usage early to catch performance bottlenecks.

---

## **Trace Logging and the Android Manifest**

- To make your app debuggable, ensure the `android:debuggable` attribute in the `<application>` tag of `AndroidManifest.xml` is set to `true` for debug builds.
  
```xml
<application android:debuggable="true">
```

### **Before Release**:
- Disable logging and debug traces in production by:
    - Removing `Log.d` statements.
    - Setting `android:debuggable` to `false` in the release build.

---

## **Related Practical Sessions**
1. **Using Breakpoints in Android Studio**.
2. **Debugging an Application in Android Studio**.
3. **Using Logcat for Debugging Android Applications**.

## **Learn More**
- [Official Debugging Documentation](https://developer.android.com/studio/debug)
- [Using Logcat in Android Studio](https://developer.android.com/studio/debug/am-logcat)
- [Android Profiler Overview](https://developer.android.com/studio/profile)

---

This cheat sheet should serve as a quick reference for Android developers looking to debug apps efficiently in Android Studio. By leveraging breakpoints, stepping through code, and using advanced features like method tracing and variable watches, you can diagnose and fix issues more effectively.
