# Text and Scrolling Views Quiz

## Multiple Choice Questions (MCQs)

1. What is the primary function of a `TextView` in Android?
    - a) To display textual content on the screen
    - b) To input text from the user
    - c) To navigate between activities
    - d) To display images

2. Which of the following is true about `EditText`?
    - a) It is a subclass of `TextView` that allows user input
    - b) It is used to format text in bold and italics
    - c) It cannot be used for multiline input
    - d) It is used for date input only

3. What attribute is used to define the width of a `TextView` in XML?
    - a) `android:width`
    - b) `android:layout_width`
    - c) `android:text_width`
    - d) `android:height_width`

4. Which of the following is the correct way to specify a string resource in a `TextView`?
    - a) `android:text="Hello World"`
    - b) `android:text="@string/hello_world"`
    - c) `android:text="@text/hello_world"`
    - d) `android:textResource="hello_world"`

5. What class is used to create vertical scrolling for a layout?
    - a) `LinearLayout`
    - b) `RelativeLayout`
    - c) `ScrollView`
    - d) `FrameLayout`

6. To enable automatic hyperlink detection for web URLs in a `TextView`, which attribute is used?
    - a) `android:linkify`
    - b) `android:autoLink="web"`
    - c) `android:linkAuto`
    - d) `android:textAppearance`

## Fill-in-the-Blanks

1. The ____________ attribute controls the color of the text in a `TextView`.
2. The `__________` class is used to enable vertical scrolling of content that exceeds the screen size.
3. A `ScrollView` can contain only one direct child element, which can be a ____________ to hold multiple elements.
4. To reference a `TextView` in your Java code, use the `____________` method to find it by its ID.
5. To set the size of the text in a `TextView`, use the attribute ___________.

## True/False

1. The `TextView` class can display both single-line and multiline text. (True/False)
2. An `EditText` cannot inherit attributes from `TextView` because it is a separate class. (True/False)
3. A `ScrollView` can scroll both vertically and horizontally at the same time. (True/False)
4. The `android:lineSpacingExtra` attribute allows you to set extra spacing between lines in a `TextView`. (True/False)
5. `TextView` can automatically convert phone numbers and emails into clickable links using `android:autoLink`. (True/False)

## Short Answer Questions

1. Explain the main difference between `TextView` and `EditText` in Android.
2. What are some common attributes of `TextView` that control how text appears on the screen?
3. How does `ScrollView` enhance the user experience when displaying large amounts of text?
4. Describe how to create a scrolling view that contains both text and other UI elements, like a button.
5. What performance considerations should be taken into account when using `ScrollView` with large layouts?

---

## Answers

### Multiple Choice Questions

1. a) To display textual content on the screen
2. a) It is a subclass of `TextView` that allows user input
3. b) `android:layout_width`
4. b) `android:text="@string/hello_world"`
5. c) `ScrollView`
6. b) `android:autoLink="web"`

### Fill-in-the-Blanks

1. `android:textColor`
2. `ScrollView`
3. `ViewGroup`
4. `findViewById()`
5. `android:textSize`

### True/False

1. True
2. False
3. False
4. True
5. True

### Short Answer Questions

1. `TextView` is used to display text that the user cannot edit, while `EditText` is a subclass of `TextView` that allows the user to input and edit text.
2. Common attributes of `TextView` include `android:text` to set the text, `android:textColor` for the text color, `android:textSize` for the size of the text, and `android:textStyle` for the style (bold, italic, etc.).
3. `ScrollView` allows users to scroll vertically through content that exceeds the screen size, improving navigation for longer texts or multiple views on smaller screens.
4. You can create a layout that includes a `ScrollView` and inside it, a `LinearLayout` with a `TextView` for the text and other UI elements like a `Button`. The `ScrollView` will make the whole layout scrollable.
5. Using complex layouts with `ScrollView` may lead to performance issues, especially when nesting multiple `LinearLayout`s or displaying large images. It’s important to optimize the layout and consider using `RecyclerView` for lists or dynamic content.
