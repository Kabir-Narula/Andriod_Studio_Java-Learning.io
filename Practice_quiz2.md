
# Android UI Components Quiz

This quiz focuses on Android UI elements such as Buttons, Input Controls, Menus, Pickers, RecyclerView, and User Navigation.

---

## Multiple Choice Questions

1. **Which method is used to handle button clicks in Android?**
   - a) `onClick()`
   - b) `onKeyDown()`
   - c) `onTap()`
   - d) `onLongPress()`

2. **Which type of button allows the user to toggle between two states in Android?**
   - a) `ToggleButton`
   - b) `RadioButton`
   - c) `ImageButton`
   - d) `CheckBox`

3. **Which of the following is an input control?**
   - a) `SeekBar`
   - b) `Switch`
   - c) `EditText`
   - d) All of the above

4. **Which method do you use to add options in the `OptionsMenu` of an activity?**
   - a) `onCreateOptionsMenu()`
   - b) `onPrepareOptionsMenu()`
   - c) `onMenuItemClick()`
   - d) `onCreateContextMenu()`

5. **Which picker allows the user to select a time in Android?**
   - a) `DatePicker`
   - b) `TimePicker`
   - c) `RangePicker`
   - d) `DateTimePicker`

6. **What layout manager is recommended for a vertical list in RecyclerView?**
   - a) `LinearLayoutManager`
   - b) `GridLayoutManager`
   - c) `RelativeLayout`
   - d) `ConstraintLayout`

7. **Which navigation pattern is typically used to move back to a parent screen?**
   - a) Lateral navigation
   - b) Back navigation
   - c) Hierarchical navigation
   - d) Descendant navigation

8. **Which method inflates a layout in a RecyclerView Adapter?**
   - a) `onBindViewHolder()`
   - b) `onCreateViewHolder()`
   - c) `getItemCount()`
   - d) `onItemViewClick()`

9. **Which method adds a button click handler in the XML layout file?**
   - a) `android:onPress`
   - b) `android:onClick`
   - c) `android:onTap`
   - d) `android:onTouch`

10. **What component is used to navigate between sibling screens in Android?**
    - a) Tabs
    - b) Back button
    - c) RecyclerView
    - d) Switch

---

## Fill-in-the-Blanks

11. The `_____________` method is used to handle a button's click event programmatically.
12. A `_____________` is an input control that allows users to select multiple options.
13. The `_____________` class is used to display a list of scrollable items.
14. To handle a menu item selection, the `_____________` method is overridden.
15. `_____________` navigation allows the user to navigate back through the hierarchy of screens.
16. A `_____________` is used to allow the user to pick a specific date.
17. The `_____________` method is responsible for creating the options menu in an activity.
18. In `RecyclerView`, the `_____________` method binds data to the ViewHolder.
19. The `android:onClick` attribute is used to specify a method to be invoked when the button is _____________.
20. A `_____________` allows users to navigate through sibling screens, such as swiping between tabs.

---

## True or False

21. Buttons in Android cannot handle click events through XML. (True/False)
22. A `CheckBox` allows multiple selections, whereas a `RadioButton` allows only one selection. (True/False)
23. The `SeekBar` input control is used to pick a date. (True/False)
24. The `onCreateOptionsMenu()` method is responsible for handling the selection of menu items. (True/False)
25. RecyclerView can be used to display both horizontal and vertical lists. (True/False)
26. The Back button handles hierarchical navigation by default. (True/False)
27. `TimePicker` is used to select both date and time. (True/False)
28. RecyclerView automatically handles data binding without an adapter. (True/False)
29. `LinearLayoutManager` arranges items in a vertical list. (True/False)
30. The `Up` button is used for lateral navigation between sibling screens. (True/False)

---

## Short Answer Questions

31. How can you handle button clicks directly in the XML layout file?
32. What is the difference between `RadioButton` and `CheckBox`?
33. Name two input controls in Android and describe their use.
34. Explain how the `OptionsMenu` is created and handled in an activity.
35. What is the function of the `DatePicker` control in Android?
36. Describe how to set up a `RecyclerView` with a `LinearLayoutManager`.
37. What is the difference between back navigation and hierarchical navigation?
38. How can you implement sibling navigation using tabs in Android?
39. What is the role of `onBindViewHolder()` in a `RecyclerView.Adapter`?
40. How does Android handle Up navigation in activities?

---

## Answers

1. a) `onClick()`
2. a) `ToggleButton`
3. d) All of the above
4. a) `onCreateOptionsMenu()`
5. b) `TimePicker`
6. a) `LinearLayoutManager`
7. c) Hierarchical navigation
8. b) `onCreateViewHolder()`
9. b) `android:onClick`
10. a) Tabs

11. `setOnClickListener()`
12. `CheckBox`
13. `RecyclerView`
14. `onOptionsItemSelected()`
15. `Hierarchical`
16. `DatePicker`
17. `onCreateOptionsMenu()`
18. `onBindViewHolder()`
19. `clicked`
20. `TabLayout`

21. False
22. True
23. False
24. False
25. True
26. True
27. False
28. False
29. True
30. False

31. By using the `android:onClick` attribute in the XML layout file.
32. `RadioButton` allows only one selection in a group, while `CheckBox` allows multiple selections.
33. Examples include `EditText` (for text input) and `SeekBar` (for selecting a value by sliding).
34. The `OptionsMenu` is created in `onCreateOptionsMenu()` and handled in `onOptionsItemSelected()`.
35. `DatePicker` is used to allow users to select a date.
36. Set the `RecyclerView` with `setLayoutManager(new LinearLayoutManager(this))`.
37. Back navigation follows the history stack, while hierarchical navigation moves within a hierarchy.
38. Implement a `TabLayout` with a `ViewPager` for swiping between sibling screens.
39. `onBindViewHolder()` binds the data to the `ViewHolder` in a `RecyclerView`.
40. Up navigation is handled by specifying the parent activity in `AndroidManifest.xml` and enabling the Up button in the action bar.
