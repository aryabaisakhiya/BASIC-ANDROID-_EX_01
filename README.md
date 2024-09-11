# Ex.No:1 Implementation of a Hello world Activity using all lifecycles methods using Android Studio.

# AIM:
To create Hello world Activity using all lifecycles methods to display messages using android studio.

# EQUIPMENTS REQUIRED:
Android Studio(Min. required Artic Fox)

# ALGORITHM:
Step 1: Open Android Stdio and then click on File -> New -> New project.
Step 2: Then type the Application name as HelloWorld and click Next.
Step 3: Then select the Minimum SDK as shown below and click Next.
Step 4: Then select the Empty Activity and click Next. Finally click Finish.
Step 5: Design layout in activity_main.xml.
Step 6: Display message give in MainActivity file.
Step 7: Save and run the application.

# PROGRAM:
```
/*
Program to implement a Hello world Activity using all lifecycles methods using Android Studio .
Developed by: Bolisetti Sanjitha
RegisterNumber: 212222040027
*/
```

# MainActivity.java:
```
package com.example.helloworld;

import android.os.Bundle;
import android.widget.Toast;
import androidx.activity.EdgeToEdge;
import androidx.appcompat.app.AppCompatActivity;
import androidx.core.graphics.Insets;
import androidx.core.view.ViewCompat;
import androidx.core.view.WindowInsetsCompat;

public class MainActivity extends AppCompatActivity {

    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        EdgeToEdge.enable(this);
        setContentView(R.layout.activity_main);
        ViewCompat.setOnApplyWindowInsetsListener(findViewById(R.id.main), (v, insets) -> {
            Insets systemBars = insets.getInsets(WindowInsetsCompat.Type.systemBars());
            v.setPadding(systemBars.left, systemBars.top, systemBars.right, systemBars.bottom);
            return insets;
        });
    }

    @Override
    protected void onStart() {
        super.onStart();
        Toast.makeText(getApplicationContext(), "OnStart Executed", Toast.LENGTH_LONG).show();
    }

    @Override
    protected void onResume() {
        super.onResume();
        Toast.makeText(getApplicationContext(), "OnResume Executed", Toast.LENGTH_LONG).show();
    }

    @Override
    protected void onPause() {
        super.onPause();
        Toast.makeText(getApplicationContext(), "OnPause Executed", Toast.LENGTH_LONG).show();
    }

    @Override
    protected void onStop() {
        super.onStop();
        Toast.makeText(getApplicationContext(), "OnStop Executed", Toast.LENGTH_LONG).show();
    }

    @Override
    protected void onRestart() {
        super.onRestart();
        Toast.makeText(getApplicationContext(), "OnRestart Executed", Toast.LENGTH_LONG).show();
    }

    @Override
    protected void onDestroy() {
        super.onDestroy();
        Toast.makeText(getApplicationContext(), "OnDestroy Executed", Toast.LENGTH_LONG).show();
    }
}
```

# activitymain.xml:
```
<?xml version="1.0" encoding="utf-8"?>
<androidx.constraintlayout.widget.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/main"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <TextView
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:text="Hello World!"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

</androidx.constraintlayout.widget.ConstraintLayout>
```

# OUTPUT:
![MAD ex1 on create](https://github.com/user-attachments/assets/a792356a-08e6-4dfc-950a-21b9147c7922)
![MAD ex1 onresume](https://github.com/user-attachments/assets/9950437d-8dbc-49df-a569-cbc159a9f22c)
![MAD ex1 onpause](https://github.com/user-attachments/assets/c8c67c6c-70cb-4b4a-bdf2-ef347f07e8e8)
![MAD ex1 onstop](https://github.com/user-attachments/assets/6988128a-4838-47d2-8e12-24a74857bc55)
![MAD ex1 onrestart](https://github.com/user-attachments/assets/8001b3f7-21ac-4af4-90bc-a4ae84cf4df9)
![MAD ex1 ondestroy](https://github.com/user-attachments/assets/b8b79617-3790-475b-840a-47826c1e9f09)

# RESULT:
Thus a program to implement the various life cycles of an activity is written and successfully executed using Android Studio.

