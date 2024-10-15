
# Android Development Quiz

## Fill in the Blanks (10 questions)

1. **________** is used to define the main activity in an Android app.
2. The **________** is responsible for laying out items vertically or horizontally on the screen.
3. **________** are used to handle long-running background tasks in Android.
4. The **________** provides back navigation across different activities in an Android app.
5. **________** is a built-in mechanism for data storage in Android, offering structured storage in tables.
6. The **________** is the default toolbar provided by Android for apps.
7. **________** menus appear when a user long presses on an item.
8. **________** is the library often used for handling REST API requests in Android.
9. The **________** method in an Activity is used to save a user’s preferences between sessions.
10. In Android, **________** provides hierarchical navigation between child and parent screens.

## Multiple Choice (20 questions)

11. Which method is used to start a new activity in Android?
   - a) startActivity()
   - b) beginActivity()
   - c) launchActivity()
   - d) runActivity()

12. Which of the following is used to store simple key-value pairs in Android?
   - a) SQLite
   - b) SharedPreferences
   - c) Room Database
   - d) Internal Storage

13. What class is used to display a scrolling list of elements in Android?
   - a) ListView
   - b) ScrollView
   - c) RecyclerView
   - d) FrameLayout

14. Which layout aligns its children in relative positions to each other?
   - a) LinearLayout
   - b) FrameLayout
   - c) RelativeLayout
   - d) TableLayout

15. Which of the following is NOT a valid Android lifecycle method?
   - a) onCreate()
   - b) onStart()
   - c) onPause()
   - d) onTerminate()

16. What is used to make asynchronous network requests in Android?
   - a) AsyncTask
   - b) HandlerThread
   - c) ThreadPool
   - d) BroadcastReceiver

17. Which component is best suited for handling long-running background tasks that may continue after the app is closed?
   - a) AsyncTask
   - b) Service
   - c) IntentService
   - d) Handler

18. Which Android storage option is used for managing large structured data across app sessions?
   - a) SharedPreferences
   - b) Internal Storage
   - c) SQLite
   - d) Cache

19. What is the primary purpose of the Android Manifest file?
   - a) Defining the app's user interface
   - b) Managing app permissions and components
   - c) Managing layout dimensions
   - d) Defining styles and themes

20. Which of the following best describes the role of the Navigation Drawer?
   - a) For navigating between tabs
   - b) For navigating within nested fragments
   - c) For providing app-wide navigation
   - d) For switching between activities

21. **TabLayout** is used in conjunction with which layout to enable swiping between different screens?
   - a) ViewPager
   - b) LinearLayout
   - c) FrameLayout
   - d) ConstraintLayout

22. Which method is used to create a context menu in Android?
   - a) onCreateContextMenu()
   - b) onContextItemSelected()
   - c) onCreateOptionsMenu()
   - d) onPrepareOptionsMenu()

23. What is the primary function of **RecyclerView** in Android?
   - a) Display static data
   - b) Display dynamic lists efficiently
   - c) Show video elements
   - d) Create a sliding drawer menu

24. Which of the following classes helps manage fragments in Android?
   - a) FragmentTransaction
   - b) FragmentLoader
   - c) FragmentManager
   - d) FragmentLayout

25. The **Snackbar** class is used to:
   - a) Display a pop-up window
   - b) Show a brief message at the bottom of the screen
   - c) Show a notification in the status bar
   - d) Display a menu

26. In the Android activity lifecycle, which method is called when an activity becomes visible to the user?
   - a) onPause()
   - b) onStart()
   - c) onStop()
   - d) onResume()

27. **Services** in Android are primarily used for:
   - a) UI updates
   - b) Background operations
   - c) User input
   - d) Data storage

28. Which UI component allows users to make a selection from a set of options using a pop-up menu?
   - a) AlertDialog
   - b) PopupMenu
   - c) Spinner
   - d) CheckBox

29. In Android, which database is commonly used for storing structured data locally?
   - a) Room
   - b) Retrofit
   - c) Firebase
   - d) SQLite

30. What is the main purpose of the **Intent** class in Android?
   - a) To manage network requests
   - b) To switch between activities
   - c) To create custom views
   - d) To store application data

## True/False (10 questions)

31. The AndroidManifest.xml file is mandatory for every Android app. (True/False)
32. AsyncTask is designed for long-running background operations in Android. (True/False)
33. Fragments in Android have their own independent lifecycle. (True/False)
34. The default data storage option in Android is SQLite. (True/False)
35. RecyclerView is more efficient than ListView for managing large sets of data. (True/False)
36. An activity in Android can have multiple layouts associated with it. (True/False)
37. The onDestroy() method is guaranteed to be called before an activity is destroyed. (True/False)
38. SharedPreferences is primarily used for storing large amounts of structured data. (True/False)
39. Services in Android can continue running even when the app is closed. (True/False)
40. The Up button in Android provides back navigation to the previous screen. (True/False)

## Short Answer (10 questions)

41. What is the purpose of Android's "JobScheduler" class?
42. Describe the difference between AsyncTask and Service in Android.
43. Explain the use of **Room Database** in Android applications.
44. What is the significance of using **Fragments** in Android?
45. How does Android handle background tasks using **WorkManager**?
46. What is the role of **Gradle** in Android Studio projects?
47. Explain how **RecyclerView** differs from **ListView** in Android.
48. What is the purpose of **ViewModel** in Android's architecture components?
49. How can you ensure smooth navigation between activities using **Intent**?
50. What are the best practices for managing **Lifecycle** events in Android apps?

---

## **Answers**

### Fill in the Blanks:
1. AndroidManifest.xml
2. LinearLayout
3. Services
4. Back button
5. SQLite
6. ActionBar
7. Contextual
8. Retrofit
9. SharedPreferences
10. Up button

### Multiple Choice:
11. a) startActivity()
12. b) SharedPreferences
13. c) RecyclerView
14. c) RelativeLayout
15. d) onTerminate()
16. a) AsyncTask
17. b) Service
18. c) SQLite
19. b) Managing app permissions and components
20. c) For providing app-wide navigation
21. a) ViewPager
22. a) onCreateContextMenu()
23. b) Display dynamic lists efficiently
24. c) FragmentManager
25. b) Show a brief message at the bottom of the screen
26. b) onStart()
27. b) Background operations
28. c) Spinner
29. d) SQLite
30. b) To switch between activities

### True/False:
31. True
32. False
33. True
34. True
35. True
36. False
37. False
38. False
39. True
40. False

### Short Answer:
41. It schedules background jobs or tasks to be run at specified times or under specified conditions.
42. AsyncTask is for short-term background tasks while Service is for long-running operations.
43. Room Database is used for structured data storage, providing an abstraction layer over SQLite.
44. Fragments modularize activities and allow for more flexible UI designs.
45. WorkManager is used for deferrable background work and is more robust across app sessions.
46. Gradle manages project dependencies, builds configurations, and automates the build process.
47. RecyclerView provides more flexible and efficient list handling than ListView.
48. ViewModel manages UI-related data in a lifecycle-conscious way to survive configuration changes.
49. By using Intent with startActivity() and passing necessary data via extras.
50. Properly managing onStart(), onPause(), and onDestroy() methods, avoiding memory leaks, and adhering to user interactions.
