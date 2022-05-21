# Ex.No:6 Build a program  to create a first display screen of any search engine using Auto Complete Text View.
## AIM:
To develop a program to create a first display screen of any search engine using AutoComplete TextView in Android Studio.

## EQUIPMENTS REQUIRED:
Android Studio(Min.required Artic Fox)

## ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as searchengine and click Next.

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using AutoComplete TextView in activity_main.xml.

Step 6: Display screen of search engine in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
/* Program to print the text “display screen of any search engine”.
Developed by: Balaji 
Registeration Number : 212220230006 */

## activity_main.xml
```java
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:orientation="vertical"
    android:padding="16dp"
    tools:context=".MainActivity">


    <AutoCompleteTextView
        android:id="@+id/autoCompleteTextView"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:completionThreshold="1"
        android:text="search"/>

    <TextView
        android:id="@+id/textview1"
        android:layout_width="match_parent"
        android:layout_height="match_parent"
        android:fontFamily="sans-serif-black"
        android:textSize="36sp"
        android:textColor="#9C27B0"
        android:textColorHighlight="#4CAF50"
        android:textColorHint="#03A9F4"
        android:textColorLink="#E91E63"
        android:textStyle="italic" />
</LinearLayout>
```
## MainActivity.java
```java
package com.example.autotext;

import androidx.appcompat.app.AppCompatActivity;

import android.app.Activity;
import android.os.Bundle;
import android.view.View;
import android.widget.AdapterView;
import android.widget.ArrayAdapter;
import android.widget.AutoCompleteTextView;
import android.widget.TextView;
import android.widget.Toast;

public class MainActivity extends Activity {
    AutoCompleteTextView auto;

    String[] words={"Apple ","buffalo","cat","dog","elephant","python","kit","lick","sight","tick","zebraz"};

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);

        auto = (AutoCompleteTextView) findViewById(R.id.autoCompleteTextView);


        ArrayAdapter adapter = new
                ArrayAdapter(this, android.R.layout.simple_list_item_1, words);

        auto.setAdapter(adapter);
        auto.setThreshold(1);


    }
}
    }
}
```
## OUTPUT
![output1](https://user-images.githubusercontent.com/75234946/169632946-f990b64c-8576-492d-95d5-d26d603be1d6.png)



![exp-6 output](https://user-images.githubusercontent.com/75234946/169632995-7184de05-1e38-4a39-b306-6f1c4bf0b1ef.png)












## RESULT
Thus a Simple Android Application develop a program to create a first display screen of any search engine using AutoComplete TextView in Android Studio is developed and executed successfully.
