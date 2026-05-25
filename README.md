# Ex.No:2a Develop program to create a text field and a button “Navigate”. When you enter “www.gmail.com” and press navigate button it should open google page using Implicit Intents.


## AIM:

To create a navigate button using Implicit Intent to display the gmail page using Android Studio.

## EQUIPMENTS REQUIRED:

Latest Version Android Studio

## ALGORITHM:

1. **Start the project:** Create a new Android project in Android Studio.

2. **Design the UI:** In `activity_main.xml`, add an `EditText` (to accept the URL input) and a `Button` (to trigger the navigation).

3. **Initialize components:** In `MainActivity.java`, map the `EditText` and `Button` variables to their respective XML IDs using `findViewById()`.

4. **Set click listener:** Attach an `OnClickListener` to the button to listen for user click events.

5. **Get input:** Inside the `onClick` method, extract the text entered in the `EditText` and convert it to a string.

6. **Create implicit intent:** Instantiate an `Intent` with the action `Intent.ACTION_VIEW` and pass the parsed URL string using `Uri.parse()`.

7. **Start activity:** Call `startActivity(intent)` to trigger the OS to open the webpage in an available web browser.

8. **Stop:** Run and test the application.

## PROGRAM:
```
/*
Program to print the text “Implicitintent”.
Developed by: S.VENGADA KRISHNAN
Registeration Number : 212223110061
*/
```
## MainActivity.java
```java
package com.example.implicitintent;

import android.content.Intent;
import android.net.Uri;
import android.os.Bundle;
import android.widget.Button;
import android.widget.EditText;

import androidx.appcompat.app.AppCompatActivity;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {

        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        EditText editText;
        Button button;

        button = findViewById(R.id.button);
        editText = findViewById(R.id.editText);

        button.setOnClickListener(view -> {
            String url=editText.getText().toString();
            Intent intent = new Intent(Intent.ACTION_VIEW, Uri.parse(url));
            startActivity(intent);
        });
    }
}
```
## activity_main.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <!-- Title -->
    <TextView
        android:id="@+id/textView"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="@string/title_implicit_intents"
        android:textColor="#D32F2F"
        android:textStyle="bold"
        android:textSize="20sp"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintBottom_toTopOf="@id/editTextText"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"/>

    <!-- Input Field -->
    <EditText
        android:id="@+id/editTextText"
        android:layout_width="0dp"
        android:layout_height="48dp"
        android:minHeight="48dp"
        android:padding="12dp"
        android:hint="@string/hint_enter_link"
        android:inputType="textUri"
        android:textColor="#000000"
        android:textColorHint="#757575"
        app:layout_constraintTop_toBottomOf="@id/textView"
        app:layout_constraintBottom_toTopOf="@id/button"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginStart="24dp"
        android:layout_marginEnd="24dp"
        android:layout_marginTop="24dp"/>

    <!-- Button -->
    <Button
        android:id="@+id/button"
        android:layout_width="wrap_content"
        android:layout_height="48dp"
        android:text="@string/btn_navigate"
        app:layout_constraintTop_toBottomOf="@id/editTextText"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        android:layout_marginTop="24dp"/>

</androidx.constraintlayout.widget.ConstraintLayout>
```
## OUTPUT
<img width="1918" height="1073" alt="image" src="https://github.com/user-attachments/assets/0559ce51-3984-40b8-9dd3-ba886e02f7d9" />
<img width="1919" height="1039" alt="image" src="https://github.com/user-attachments/assets/3f57fa0b-49cc-4540-91d3-7bc98e3fd53f" />

<img width="1914" height="1079" alt="image" src="https://github.com/user-attachments/assets/5da7f775-0af4-455e-acfa-406ff650944d" />




## RESULT
Thus a Simple Android Application create a navigate button using Implicit Intent to display the gmail page using Android Studio is developed and executed successfully.


