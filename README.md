
# Ex.No:10 To create a option menu to display menu items.


## AIM:

To create a option menu to display menu items using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:
```
step 1:Create XML layout for the main activity.
step 2:Define the main activity Java class.
step 3:Create XML file for the options menu.
step 4:Override onCreateOptionsMenu() method.
step 5:Handle menu item selection.
step 6:Handle menu item actions.
```


## PROGRAM:
```
/*
Program to print the text “optionmenu”.
Developed by: ch.geethika
Registeration Number : 212221040032
*/
```
### activity_main.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <androidx.appcompat.widget.Toolbar
        android:id="@+id/toolbar"
        android:layout_width="match_parent"
        android:layout_height="?attr/actionBarSize"
        android:background="?attr/colorPrimary"
        app:title="Options Menu Example"
        app:titleTextColor="@android:color/white" />

</RelativeLayout>
```
### mainactivity.java:
```
package com.example.menuapp;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.view.Menu;
import android.view.MenuInflater;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);


        androidx.appcompat.widget.Toolbar toolbar = findViewById(R.id.toolbar);
        setSupportActionBar(toolbar);
    }

    @Override
    public boolean onCreateOptionsMenu(Menu menu) {
        MenuInflater inflater = getMenuInflater();
        inflater.inflate(R.menu.option, menu);
        return true;
    }
}
```
### option_xml:
```
<?xml version="1.0" encoding="utf-8"?>
<menu xmlns:android="http://schemas.android.com/apk/res/android">
    <item
        android:id="@+id/action_item1"
        android:title="Item 1" />
    <item
        android:id="@+id/action_item2"
        android:title="Item 2" />
    <item
        android:id="@+id/action_item3"
        android:title="Item 3" />
</menu>
```

## OUTPUT
![Screenshot (454)](https://github.com/chgeethika/menuinandroid/assets/142209368/27adf26a-340d-4856-8a0d-0fd522a3bd31)

![Screenshot (455)](https://github.com/chgeethika/menuinandroid/assets/142209368/d38dcec9-7ff4-4b3e-b768-164c504620a7)





## RESULT
Thus a Simple Android Application to create a option menu to display menu items using Android Studio is developed and executed successfully.
