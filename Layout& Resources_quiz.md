# Android Studio Menus and Pickers Quiz

## Multiple Choice Questions (MCQs)

1. Which of the following is not a type of menu in Android?
    - a) Options Menu
    - b) Context Menu
    - c) Floating Action Menu
    - d) Popup Menu

2. What method is used to inflate a menu resource in an activity?
    - a) `onCreateOptionsMenu()`
    - b) `onPrepareOptionsMenu()`
    - c) `onMenuItemSelected()`
    - d) `inflateMenu()`

3. Which of the following is a picker widget used to select a date?
    - a) DatePickerDialog
    - b) TimePickerDialog
    - c) NumberPicker
    - d) AlertDialog

4. In Android, which method handles click events for options menu items?
    - a) `onClick()`
    - b) `onOptionsItemSelected()`
    - c) `onMenuClick()`
    - d) `onItemSelected()`

5. Which XML attribute is used to specify the layout file for a menu in Android?
    - a) `android:layout`
    - b) `android:menu`
    - c) `app:menuLayout`
    - d) `res:menuLayout`

6. Which of the following is a correct way to display a popup menu?
    - a) `PopupMenu.show()`
    - b) `PopupMenu.display()`
    - c) `PopupMenu.showMenu()`
    - d) `PopupMenu.showAsDropDown()`

## Fill-in-the-Blanks

1. The ___________ method is used to inflate a menu resource file in a fragment.
2. In an `OptionsMenu`, we define the menu items using the ___________ XML element.
3. The `TimePickerDialog` is used to select a ___________.
4. To create a custom dialog for a picker, the ___________ class is used in Android.
5. A ___________ menu is triggered by a long-click on a UI element in Android.

## True/False

1. The `PopupMenu` is part of the `android.widget` package. (True/False)
2. An `OptionsMenu` is always displayed at the bottom of the screen. (True/False)
3. The `DatePickerDialog` only allows the selection of a month and year. (True/False)
4. The `onCreateContextMenu()` method is used to register a view for the context menu. (True/False)
5. Menus in Android cannot be customized to display icons. (True/False)

## Short Answer Questions

1. What are the main differences between a `PopupMenu` and a `ContextMenu` in Android?
2. Explain how you can handle click events for menu items in an `OptionsMenu`.
3. What is the purpose of the `NumberPicker` widget, and how does it differ from a `DatePicker`?
4. Describe how you can create a custom `TimePickerDialog` in Android.
5. How do you dynamically update menu items in an `OptionsMenu` after the menu is created?

---

## Answers

### Multiple Choice Questions

1. c) Floating Action Menu
2. a) `onCreateOptionsMenu()`
3. a) DatePickerDialog
4. b) `onOptionsItemSelected()`
5. b) `android:menu`
6. d) `PopupMenu.showAsDropDown()`

### Fill-in-the-Blanks

1. `onCreateOptionsMenu()`
2. `<item>`
3. time
4. `Dialog`
5. context

### True/False

1. True
2. False
3. False
4. True
5. False

### Short Answer Questions

1. A `PopupMenu` is typically anchored to a view and appears as a dropdown, while a `ContextMenu` is triggered by a long-press and is associated with specific UI elements. `PopupMenu` is more like a lightweight menu for small actions, whereas `ContextMenu` is context-specific and allows more extensive actions.
2. You can handle click events for menu items by overriding the `onOptionsItemSelected(MenuItem item)` method in the activity or fragment. Each menu item has an ID, and you can use a switch-case block to handle actions based on the selected item's ID.
3. The `NumberPicker` widget allows users to pick a number from a range of values, while a `DatePicker` is a specialized widget designed for selecting dates, including day, month, and year.
4. To create a custom `TimePickerDialog`, you can instantiate the `TimePickerDialog` class, pass a `TimePickerDialog.OnTimeSetListener` to handle the selected time, and customize the dialog’s UI or behavior as needed.
5. You can dynamically update menu items in an `OptionsMenu` by overriding the `onPrepareOptionsMenu(Menu menu)` method. This method is called every time the menu is about to be shown, allowing you to modify the menu items before displaying them to the user.
