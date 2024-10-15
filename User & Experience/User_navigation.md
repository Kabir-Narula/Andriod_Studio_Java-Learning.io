
# 4.4: User Navigation


## Providing users with a path through your app
In the early stages of developing an app, it's essential to determine the user paths for each task. Tasks include actions like placing orders or browsing content. Each path guides users across, into, and out of different screens and tasks within the app. 

Android apps typically feature the following navigation types:
- **Back navigation**: Users move to the previous screen using the system's Back button.
- **Hierarchical navigation**: Users move through a hierarchy of screens, where each set of child screens has a parent screen.

## Back-button navigation
The **Back button** in Android provides users with a simple way to navigate through the app. This button is a key feature, taking users back through their history of screens, starting from the Launcher (the device's home screen). 

Android manages tasks and back stacks automatically, but in certain situations, you might want to override the default behavior. For instance, in an embedded browser scenario, overriding the `onBackPressed()` method lets you handle the browser's internal back behavior:

```java
@Override
public void onBackPressed() {
    // Add the Back key handler here.
    return;
}
```

## Hierarchical navigation patterns
Hierarchical navigation organizes app screens in a parent-child relationship. This structure is essential for apps with many layers of information, such as news or e-commerce apps. Key elements:
- **Parent screen**: The top-level screen, often the main Activity.
- **First-level child screen siblings**: Screens under the parent, often representing collections like news sections.
- **Second-level child screen siblings**: Screens that hold detailed content, such as articles.

Hierarchical navigation includes:
- **Descendant navigation**: Moving from parent to child.
- **Ancestral navigation**: Moving up from child to parent.
- **Lateral navigation**: Moving across sibling screens.

## Ancestral navigation (the Up button)
**Ancestral navigation** helps users move up from child screens back to parent screens using the Up button in the app bar. For example, when a user views an article, tapping the Up button takes them back to the article's section. This behavior contrasts with the system's Back button, which returns users to the previous screen, regardless of hierarchy.

To implement Up navigation, define parent-child relationships in `AndroidManifest.xml`:

```xml
<activity android:name=".ChildActivity"
    android:parentActivityName=".ParentActivity">
    <meta-data android:name="android.support.PARENT_ACTIVITY"
        android:value=".ParentActivity"/>
</activity>
```

## Descendant navigation
This type of navigation helps users move down from a parent to a child screen. You can implement descendant navigation using buttons or image targets (e.g., dashboards with images that users can tap to open another screen).

### Example:
A **navigation drawer** can offer descendant navigation from the parent Activity to child screens. To implement it:
- Add a **DrawerLayout** as the root view in your layout file.
- Include a **NavigationView** for the drawer menu.
  
## Lateral navigation with tabs and swipes
Lateral navigation allows users to navigate between sibling screens, such as switching between tabs in a news app. Android supports lateral navigation with:
- **Tabs**: For sibling navigation, ideal for small sets of related screens (e.g., categories in an app).
- **Swipe views**: Allow users to swipe left and right between screens (common with tabbed interfaces).

### Implementing Tab Navigation:
1. Define a `TabLayout` in your main activity.
2. Create a `Fragment` for each tab content.
3. Use a `PagerAdapter` to manage the fragments.

```java
public class PagerAdapter extends FragmentStatePagerAdapter {
    int mNumOfTabs;
    
    public PagerAdapter(FragmentManager fm, int NumOfTabs) {
        super(fm);
        this.mNumOfTabs = NumOfTabs;
    }
    
    @Override
    public Fragment getItem(int position) {
        switch (position) {
            case 0: return new TabFragment1();
            case 1: return new TabFragment2();
            default: return null;
        }
    }
    
    @Override
    public int getCount() {
        return mNumOfTabs;
    }
}
```

## Good Practices and Tips:
- **Design for simplicity**: Avoid unnecessary navigation layers.
- **Use tabs for small sets**: Tabs are most effective with fewer than 4 screens.
- **Be consistent**: Ensure users can intuitively navigate up, down, or sideways without confusion.
- **Use gestures**: Swipe gestures provide a seamless, intuitive way to switch between related screens.

---

*Generated on 2024-10-15*
