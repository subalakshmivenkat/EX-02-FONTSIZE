## Ex.No:2 Develop an application that uses Font Size using Android Studio.
## AIM:
To develop an application that uses Font Size using android studio.

# EQUIPMENTS REQUIRED:
Android Studio(Min. required Artic Fox)

# ALGORITHM:
Step 1: Create a New Android Project: • Click New in the toolbar. • In the window that appears, open the Android folder, select Android Application Project, and click next. • Provide the application name and the project name and then finally give the desired package name. • Choose a launcher icon for your application and then select Blank Activity and then click Next • Provide the desired Activity name for your project and then click Finish.

Step 2: Create a New AVD (Android Virtual Device): • click Android Virtual Device Manager from the toolbar. • In the Android Virtual Device Manager panel, click New. • Fill in the details for the AVD. Give it a name, a platform target, an SD card size, and a skin (HVGA is default). • Click Create AVD and Select the new AVD from the Android Virtual Device Manager and click Start.

Step 3: Design the graphical layout with a text view and two command buttons.

Step 4: Run the application.

Step 5:On pressing the change font size button, the size of the font gets altered.

Step 6:Close the Android project.

## Program:

Program to Develop an application that uses Font Size using Android Studio .
Developed by: Subalakshmi V
Register Number:  212222040162

# MainActivity.java:
```
package com.example.demo;

import androidx.appcompat.app.AppCompatActivity;
import android.os.Bundle;
import android.graphics.Color;
import android.view.View;
import android.widget.Button;
import android.widget.TextView;



public class MainActivity extends AppCompatActivity {
    int ch=1;
    float font=30;

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        final TextView t= (TextView) findViewById(R.id.textView);
        Button b1= (Button) findViewById(R.id.button1);
        b1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                t.setTextSize(font);
                font = font + 5;
                if (font == 50)
                    font = 30;
            }
        });
        Button b2= (Button) findViewById(R.id.button2);
        b2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                switch (ch) {
                    case 1:
                        t.setTextColor(Color.RED);
                        break;
                    case 2:
                        t.setTextColor(Color.GREEN);
                        break;
                    case 3:
                        t.setTextColor(Color.BLUE);
                        break;
                    case 4:
                        t.setTextColor(Color.CYAN);
                        break;
                    case 5:
                        t.setTextColor(Color.YELLOW);
                        break;
                    case 6:
                        t.setTextColor(Color.MAGENTA);
                        break;
                }
                ch++;
                if (ch == 7)
                    ch = 1;
            }
        });


    }
}
```
# MainActivity.XML
```
<?xml version="1.0" encoding="utf-8"?>
<LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    android:orientation="vertical"
    android:layout_width="match_parent"
    android:layout_height="match_parent">
 
    <TextView
        android:id="@+id/textView"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="30dp"
        android:gravity="center"
        android:text="Hello World!"
        android:textSize="25sp"
        android:textStyle="bold" />
 
    <Button
        android:id="@+id/button1"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="20dp"
        android:gravity="center"
        android:text="Change font size"
        android:textSize="25sp" />
    <Button
        android:id="@+id/button2"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_margin="20dp"
        android:gravity="center"
        android:text="Change color"
        android:textSize="25sp" />
</LinearLayout>
```
# Output:
![image](https://github.com/user-attachments/assets/a89e9004-f4ed-4479-97b7-b545c536c84b)

# Result:
Thus, the program for android application, Font Size was executed successfully using Android Studio.
