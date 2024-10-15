
# Menus and Pickers


## 1. Types of Menus <a name="types-of-menus"></a>

A **menu** is a set of options allowing users to perform actions such as searching, saving, editing, or navigating. Android provides various types of menus:

- **Options menu**: Located in the app bar, offering global actions like Search, Share, or Settings.
- **Contextual menu**: Appears when users perform a long press on a view (e.g., Edit, Delete).
- **Popup menu**: Anchored to a view, offering extended actions (e.g., Reply, Forward in Gmail).

---

## 2. The App Bar and Options Menu <a name="the-app-bar-and-options-menu"></a>

The **app bar** (or action bar) is the dedicated space at the top of each activity. It contains options for navigation, action icons, and an overflow menu for less frequent actions.

### Key Features:
- **Navigation Button/Up Button**: Used for app navigation.
- **Title**: Displays the app title.
- **Action Icons**: Represents frequently used actions.
- **Overflow Menu**: For additional actions not shown in the app bar.

#### Adding the App Bar:
Use the `Toolbar` class to set up the app bar with full compatibility across Android versions.

Example code:
```xml
<android.support.design.widget.AppBarLayout
    android:layout_width="match_parent"
    android:layout_height="wrap_content">

    <android.support.v7.widget.Toolbar
        android:id="@+id/toolbar"
        android:layout_width="match_parent"
        android:layout_height="?attr/actionBarSize" />
</android.support.design.widget.AppBarLayout>
```

---

## 3. Contextual Menus <a name="contextual-menus"></a>

Contextual menus appear as floating lists when users long-press a UI element. Two types of contextual menus are:

- **Floating Context Menu**: Shows a list of actions for a selected item (e.g., Edit, Share).
- **Contextual Action Bar**: Replaces the app bar and provides action items (e.g., multi-select edit/delete).

### Steps to Implement:
1. Create a menu resource file (`res/menu/menu_context.xml`).
2. Register a view for a context menu using `registerForContextMenu()`.
3. Implement the `onCreateContextMenu()` method to inflate the menu.

---

## 4. Popup Menu <a name="popup-menu"></a>

A **PopupMenu** is anchored to a view and displays a list of actions in a vertical orientation.

### Steps to Implement:
1. Create a menu resource file (`res/menu/menu_popup.xml`).
2. Create an `ImageButton` in the XML layout.
3. Use `PopupMenu` class to create a popup and inflate it.

Example:
```java
PopupMenu popup = new PopupMenu(MainActivity.this, view);
popup.getMenuInflater().inflate(R.menu.menu_popup, popup.getMenu());
popup.show();
```

---

## 5. Dialogs and Pickers <a name="dialogs-and-pickers"></a>

**Dialogs** are used to alert users or request input. Android provides various dialog types, including `AlertDialog`, `DatePickerDialog`, and `TimePickerDialog`.

### AlertDialog Example:
```java
AlertDialog.Builder builder = new AlertDialog.Builder(this);
builder.setMessage("Are you sure?")
       .setPositiveButton("Yes", new DialogInterface.OnClickListener() {
           public void onClick(DialogInterface dialog, int id) {
               // User clicked Yes
           }
       })
       .setNegativeButton("No", new DialogInterface.OnClickListener() {
           public void onClick(DialogInterface dialog, int id) {
               // User clicked No
           }
       });
builder.create().show();
```

### Pickers:
Use **DatePickerDialog** and **TimePickerDialog** to let users select a date or time.

Example for DatePicker:
```java
DatePickerDialog datePicker = new DatePickerDialog(this, 
    new DatePickerDialog.OnDateSetListener() {
        public void onDateSet(DatePicker view, int year, int month, int day) {
            // Do something with the chosen date
        }
    }, year, month, day);
datePicker.show();
```

---

## Related Practical <a name="related-practical"></a>
- Practice adding different types of menus and dialogs to your app.

## Learn More <a name="learn-more"></a>
- [Menus in Android Documentation](https://developer.android.com/guide/topics/ui/menus)
- [Dialogs in Android Documentation](https://developer.android.com/guide/topics/ui/dialogs)
