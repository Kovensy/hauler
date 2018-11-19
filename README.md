# Hauler

Hauler is a library containing custom layout which enables to easily create swipe to dismiss activity.
Implementation is based on code in project  [Plaid](https://github.com/nickbutcher/plaid)


# How to use 
 - Create custom style for activity which is meant to be dismissed eg:

 ```xml
<style name="AppTheme.Dragable" parent="Theme.AppCompat.Light.NoActionBar">
        <item name="android:colorBackgroundCacheHint">@null</item>
        <item name="android:windowContentOverlay">@null</item>
        <item name="android:windowIsFloating">false</item>
        <item name="android:windowIsTranslucent">true</item>
        <item name="android:windowNoTitle">true</item>
        <item name="android:windowBackground">@color/scrim</item>
</style>
```
- Put content of your activity in to `ElasticDragDismissFrameLayout` an register `ElasticDragDismissFrameLayout.OnDismissListener`

 ```xml
<com.thefuntasty.hauler.ElasticDragDismissFrameLayout
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        app:dragDismissDistance="112dp"
        app:dragDismissScale="0.95"/>
```
- Finally put content of your activity which is meant to reister drag of your finger in to `NestedScrollView` or in to `LockableNestedScrollView`
