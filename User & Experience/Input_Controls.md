
# 4.2: Input Controls


## Input Controls

This chapter introduces the Android input controls. Input controls are interactive elements in your app's UI that accept data input. Users input data to apps by entering text or numbers into fields using the on-screen keyboard. Users also select options from checkboxes, radio buttons, and drop-down menus, and they change settings and turn on or turn off certain features.

Android provides a variety of input controls for your UI. Some popular ones include:

- **EditText field** for entering text using a keyboard
- **SeekBar** for sliding left or right to a setting
- **CheckBox elements** for selecting one or more options
- **RadioGroup of RadioButton elements** for selecting one option
- **Switch** for turning on or off an option
- **Spinner drop-down menu** for selecting one option

### Best Practices
When your app needs to get data from the user, try to make the process as easy as possible by minimizing user gestures and pre-filling forms.

---

## Input Controls for Making Choices

### Checkboxes

A **Checkbox** allows the user to select one or more choices. Each checkbox is independent, meaning selecting one checkbox does not affect the others.

Example XML layout for checkboxes:
```xml
<CheckBox
    android:id="@+id/checkbox_chocolate"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Chocolate" />
<CheckBox
    android:id="@+id/checkbox_sprinkles"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Sprinkles" />
```

In Java, to retrieve the state of the checkbox:
```java
CheckBox chocolateCheckbox = findViewById(R.id.checkbox_chocolate);
boolean isChecked = chocolateCheckbox.isChecked();
```

### Radio Buttons

**Radio buttons** are used when the user must select one option from a group. They are usually placed inside a **RadioGroup**, which automatically handles the deselection of other radio buttons.

Example XML layout for radio buttons:
```xml
<RadioGroup
    android:layout_width="wrap_content"
    android:layout_height="wrap_content">
    <RadioButton
        android:id="@+id/radio_one"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Option 1"/>
    <RadioButton
        android:id="@+id/radio_two"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Option 2"/>
</RadioGroup>
```

To handle clicks:
```java
public void onRadioButtonClicked(View view) {
    boolean checked = ((RadioButton) view).isChecked();
    switch(view.getId()) {
        case R.id.radio_one:
            if (checked)
                // Handle Option 1
            break;
        case R.id.radio_two:
            if (checked)
                // Handle Option 2
            break;
    }
}
```

---

## Spinner

A **Spinner** provides a drop-down menu with a list of options. It is a good alternative when the user needs to select from a long list without taking up much screen space.

Example XML layout for a Spinner:
```xml
<Spinner
    android:id="@+id/my_spinner"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"/>
```

Setting up the spinner with an array:
```java
Spinner spinner = findViewById(R.id.my_spinner);
ArrayAdapter<CharSequence> adapter = ArrayAdapter.createFromResource(this,
        R.array.options_array, android.R.layout.simple_spinner_item);
adapter.setDropDownViewResource(android.R.layout.simple_spinner_dropdown_item);
spinner.setAdapter(adapter);
```

---

## Toggle Buttons and Switches

### Toggle Button

A **ToggleButton** lets the user switch between two states (on/off). It is often used for settings like Wi-Fi or Bluetooth.

Example XML layout:
```xml
<ToggleButton
    android:id="@+id/toggle_button"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"/>
```

Handling toggle button state in Java:
```java
ToggleButton toggleButton = findViewById(R.id.toggle_button);
toggleButton.setOnCheckedChangeListener(new CompoundButton.OnCheckedChangeListener() {
    @Override
    public void onCheckedChanged(CompoundButton buttonView, boolean isChecked) {
        if (isChecked) {
            // Toggle is ON
        } else {
            // Toggle is OFF
        }
    }
});
```

### Switch

A **Switch** provides a more visually appealing way to toggle between states compared to a **ToggleButton**. 

Example XML layout:
```xml
<Switch
    android:id="@+id/switch_button"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"/>
```

Handling Switch state:
```java
Switch mySwitch = findViewById(R.id.switch_button);
mySwitch.setOnCheckedChangeListener(new CompoundButton.OnCheckedChangeListener() {
    @Override
    public void onCheckedChanged(CompoundButton buttonView, boolean isChecked) {
        if (isChecked) {
            // Switch is ON
        } else {
            // Switch is OFF
        }
    }
});
```

---

## Text Input

The **EditText** control allows users to enter text, numbers, or other symbols. 

Example XML for a text field:
```xml
<EditText
    android:id="@+id/text_input"
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:hint="Enter your name"/>
```

In Java, to get the user's input:
```java
EditText editText = findViewById(R.id.text_input);
String input = editText.getText().toString();
```

---

## Related Practical

Try building a simple form that uses a combination of these input controls—such as checkboxes, radio buttons, and text input—to gather information from the user.

## Learn More

Explore the [Android Developer Documentation](https://developer.android.com/guide/topics/ui/controls) for more details on input controls and best practices.
