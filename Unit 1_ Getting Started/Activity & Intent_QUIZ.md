
# Android Development Quiz

## Section 1: Activities and Intents

1. **Fill in the Blank**:  
   An **Activity** represents a single __________ with a user interface in an Android application.

2. **Multiple Choice**:  
   Which of the following best describes the role of an **Intent** in Android development?  
   A) It stores data in SQLite databases  
   B) It is used to display dialogs  
   C) It is used to communicate between different components, such as activities  
   D) It provides a way to handle asynchronous tasks

3. **True or False**:  
   An **Activity** can only have one Intent.

4. **Fill in the Blank**:  
   The method **startActivity(Intent)** is used to __________.

5. **Multiple Choice**:  
   Which of the following statements is true regarding **Activities**?  
   A) An Activity cannot start another activity  
   B) An Activity can start another activity using an Intent  
   C) An Activity can have multiple layouts at once  
   D) An Activity cannot interact with other activities

## Section 2: Activity Lifecycle and State

6. **Fill in the Blank**:  
   The **onCreate()** method is called when an activity is __________.

7. **Multiple Choice**:  
   In which state is the activity visible but not interactable?  
   A) Paused  
   B) Resumed  
   C) Stopped  
   D) Destroyed

8. **True or False**:  
   The **onPause()** method is always called before the **onStop()** method.

9. **Fill in the Blank**:  
   The **onRestart()** method is called when an activity is __________ after being stopped.

10. **Multiple Choice**:  
    Which of the following lifecycle methods is called when the activity is no longer visible?  
    A) onResume()  
    B) onPause()  
    C) onStop()  
    D) onDestroy()

## Section 3: Implicit Intents

11. **Fill in the Blank**:  
    An **implicit intent** is used when you want to perform an action without specifying __________.

12. **Multiple Choice**:  
    What is the primary purpose of an implicit intent?  
    A) To open a specific activity  
    B) To broadcast a system-wide message  
    C) To request an action from any available component that can handle it  
    D) To manage background tasks

13. **True or False**:  
    Implicit intents always specify a target component.

14. **Fill in the Blank**:  
    The **Intent filter** in the AndroidManifest is used to determine which activities can handle a particular __________.

15. **Multiple Choice**:  
    Which of the following is an example of an implicit intent?  
    A) Navigating from one activity to another within the same app  
    B) Opening a web page using an external browser  
    C) Sending data between activities explicitly  
    D) Starting a service within the same app

---

### Answers:

1. screen  
2. C) It is used to communicate between different components, such as activities  
3. False  
4. launch a new activity  
5. B) An Activity can start another activity using an Intent  
6. created  
7. A) Paused  
8. True  
9. restarted  
10. C) onStop()  
11. the component  
12. C) To request an action from any available component that can handle it  
13. False  
14. intent  
15. B) Opening a web page using an external browser  
