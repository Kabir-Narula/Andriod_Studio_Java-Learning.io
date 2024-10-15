
# Android App Development Cheat Sheet: Activities and Intents

---

## Unit 1: Getting Started

### **Lesson 2: Activities and Intents**

---

### **1. Overview of Activities**
- **Activity**: Represents a single screen in an app.
    - Each app usually has multiple activities, representing different screens (e.g., list view, detailed view).
    - One activity is designated as the **main activity** (e.g., `MainActivity`), which is launched when the app starts.
    - Activities work together but are independent, allowing the app to call or start activities from other apps.
  
---

### **2. Lifecycle of an Activity**
- Android activities go through different states. Each state has a corresponding lifecycle callback.

#### **Activity Lifecycle Callbacks:**
- **`onCreate()`**: Called when the activity is first created. Use it to initialize components.
- **`onStart()`**: Activity is becoming visible to the user.
- **`onResume()`**: Activity starts interacting with the user.
- **`onPause()`**: Activity is partially obscured (e.g., another activity appears in front of it).
- **`onStop()`**: Activity is no longer visible.
- **`onDestroy()`**: Activity is finishing or being destroyed by the system.
  
#### **Tip**: Always save important data in `onPause()` because the user might not return to your activity.

---

### **3. Creating and Declaring an Activity**

#### **Create Activity in Java:**
```java
public class MainActivity extends AppCompatActivity {
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
    }
}
```

#### **Declare Activity in `AndroidManifest.xml`:**
```xml
<activity android:name=".MainActivity">
   <intent-filter>
      <action android:name="android.intent.action.MAIN" />
      <category android:name="android.intent.category.LAUNCHER" />
   </intent-filter>
</activity>
```

---

### **4. Understanding Intents**
- **Intent**: Used to start activities and pass data between them.
  - **Explicit Intent**: Specifies the target activity by class name.
  - **Implicit Intent**: Specifies a general action (e.g., sharing, opening a URL), and the Android system decides which activity can handle it.

#### **Example of Explicit Intent:**
```java
Intent intent = new Intent(this, SecondActivity.class);
startActivity(intent);
```

---

### **5. Passing Data Between Activities**
- **Intent Extras**: Used to pass key-value pairs between activities.

#### **Sending data:**
```java
Intent intent = new Intent(this, SecondActivity.class);
intent.putExtra("EXTRA_MESSAGE", "Hello, World!");
startActivity(intent);
```

#### **Receiving data in another Activity:**
```java
Intent intent = getIntent();
String message = intent.getStringExtra("EXTRA_MESSAGE");
```

---

### **6. Getting Data Back from an Activity**
- **Use `startActivityForResult()`** to start an activity and get a result back.

#### **Start Activity for Result:**
```java
Intent intent = new Intent(this, SecondActivity.class);
startActivityForResult(intent, REQUEST_CODE);
```

#### **Handle Result in `onActivityResult()`:**
```java
@Override
protected void onActivityResult(int requestCode, int resultCode, Intent data) {
    super.onActivityResult(requestCode, resultCode, data);
    if (requestCode == REQUEST_CODE && resultCode == RESULT_OK) {
        String result = data.getStringExtra("EXTRA_RESULT");
    }
}
```

#### **Returning Data:**
```java
Intent resultIntent = new Intent();
resultIntent.putExtra("EXTRA_RESULT", "Result Data");
setResult(RESULT_OK, resultIntent);
finish();
```

---

### **Additional StackOverflow Insights**

- **Common Errors and Fixes:**
    - **`NullPointerException`**: Always check if extras are `null` before accessing them.
    ```java
    if (intent != null && intent.hasExtra("EXTRA_KEY")) {
        String data = intent.getStringExtra("EXTRA_KEY");
    }
    ```
    - **Incorrect `requestCode`**: Always match the request code in `onActivityResult()` with what you passed to `startActivityForResult()`.

- **Back Navigation vs Up Navigation:**
    - **Back Navigation**: Temporal navigation through the activity stack.
    - **Up Navigation**: Hierarchical navigation within the app.
    - **Tip**: Use `android:parentActivityName` in the manifest to define Up navigation.

---

## Unit 2: User Experience

### **Lesson 3: Debugging and Support Libraries**

---

### **1. Using the Android Studio Debugger**
- **Breakpoints**: Set breakpoints in your code to pause execution and inspect variables.
- **Key Debugging Commands**:
    - **Step Over (F8)**: Execute the next line, skipping over method calls.
    - **Step Into (F7)**: Enter the method being called.
  
---

### **2. App Testing**

- **Unit Testing**: Use JUnit for logic testing.
- **UI Testing**: Use Espresso for Android UI automation testing.

#### **Example:**
```java
@Test
public void changeText_sameActivity() {
    onView(withId(R.id.textToBeChanged)).perform(click());
    onView(withId(R.id.textToBeChanged)).check(matches(withText("New Text")));
}
```

---

### **3. Android Support Library**

- **Provides backward compatibility** for newer features on older Android versions.
- **Add the library in `build.gradle`:**
```gradle
implementation 'com.android.support:appcompat-v7:28.0.0'
```

---

### **Lesson 4: User Interaction**

---

### **1. Buttons and Clickable Images**

#### **Set `OnClickListener` for Buttons:**
```java
Button myButton = findViewById(R.id.my_button);
myButton.setOnClickListener(new View.OnClickListener() {
    @Override
    public void onClick(View v) {
        // Code to execute on click
    }
});
```

---

### **Lesson 5: Material Design**

#### **Material Design Components:**
- **Toolbar**: Use the `androidx.appcompat.widget.Toolbar` for a consistent app bar.
- **FloatingActionButton**: Provides a circular button for primary actions.
- **CardView and RecyclerView**: For complex layouts and lists.

---

### **Lesson 6: UI Testing**
- Use tools like **Espresso** and **UI Automator** for automated UI testing to ensure your app works across different devices.

---

## References and Resources

### **Official Android Documentation**:
- [Android Activity Lifecycle](https://developer.android.com/guide/components/activities/activity-lifecycle)
- [Intent and Intent Filters](https://developer.android.com/guide/components/intents-filters)

### **StackOverflow**:
- Great for finding answers to specific issues or patterns for common problems in Android development.

---


