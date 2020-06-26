## Problem

Let's say you use `android:textFontWeight` (introduced in API 28) in a `TextAppearance` as follows

```xml
<style name="MyTextStyle" parent="TextAppearance.AppCompat">
    <item name="android:fontFamily">@font/montserrat</item>
    <item name="android:textSize">18sp</item>
    <item name="android:textFontWeight">500</item>
</style>
```

Now, if you set this TextAppearance to a TextView in a layout, **overriding the `textFontWeight` has no effect**. In the following example, The "Hello world" text still renders with font weight of 500 (which was set in the TextAppearance), not 800 (which we set in the layout)

```xml
<TextView
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    android:text="Hello world"
    android:textAppearance="@style/MyTextStyle"
    android:textFontWeight="800" />
``` 

### Screenshot

![Screenshot](screenshots/textFontWeight_issue.png)