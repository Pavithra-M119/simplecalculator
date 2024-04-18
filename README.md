# Ex.No:9 Develop a simple calculator using android studio.

## AIM:

To develop a program to develop a simple calculator in Android Studio.

## EQUIPMENTS REQUIRED:

Android Studio(Latest Version)

## ALGORITHM:

Step 1: Open Android Stdio and then click on File -> New -> New project.

Step 2: Then type the Application name as calculator and click Next. 

Step 3: Then select the Minimum SDK as shown below and click Next.

Step 4: Then select the Empty Activity and click Next. Finally click Finish.

Step 5: Design layout using UI components in activity_main.xml.

Step 6: Display the calculator operation in MainActivity file.

Step 7: Save and run the application.

## PROGRAM:
```
/*
Program to print the text “calculator operation”.
Developed by:Pavithra.M
Registeration Number :212221040119
*/
```
## In activity_main.xml :
```
<?xml version="1.0" encoding="utf-8"?>
<RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:id="@+id/relative1"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    tools:context=".MainActivity">

    <EditText
        android:id="@+id/edt1"
        android:layout_width="match_parent"
        android:layout_height="120dp"
        android:fontFamily="sans-serif-medium"
        android:textAlignment="center"
        android:textSize="20sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/button1"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/edt1"
        android:layout_alignEnd="@+id/button4"
        android:layout_alignRight="@+id/button4"
        android:layout_marginTop="127dp"
        android:layout_marginEnd="-1dp"
        android:layout_marginRight="-1dp"
        android:backgroundTint="#CD225C"
        android:backgroundTintMode="src_atop"
        android:text="1"
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/button2"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignTop="@+id/button1"
        android:layout_toStartOf="@+id/button3"
        android:layout_toLeftOf="@+id/button3"
        android:text="2"
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/button3"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignTop="@+id/button2"
        android:layout_centerHorizontal="true"
        android:text="3"
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/button4"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/button1"
        android:layout_toLeftOf="@+id/button2"
        android:text="4"
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/button5"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_alignStart="@+id/button2"
        android:layout_alignLeft="@+id/button2"
        android:layout_alignBottom="@+id/button4"
        android:text="5"
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/button6"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/button3"
        android:layout_alignStart="@+id/button3"
        android:layout_alignLeft="@+id/button3"
        android:text="6"
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/button7"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/button4"
        android:layout_toLeftOf="@+id/button2"
        android:text="7"
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/button8"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/button5"
        android:layout_alignStart="@+id/button5"
        android:layout_alignLeft="@+id/button5"
        android:text="8"
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/button9"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/button6"
        android:layout_alignStart="@+id/button6"
        android:layout_alignLeft="@+id/button6"
        android:text="9"
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/buttonadd"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="80dp"
        android:layout_height="wrap_content"
        android:layout_alignTop="@+id/button3"
        android:layout_alignEnd="@+id/edt1"
        android:layout_alignRight="@+id/edt1"
        android:layout_marginStart="46dp"
        android:layout_marginLeft="37dp"
        android:layout_marginTop="3dp"
        android:layout_marginEnd="61dp"
        android:layout_marginRight="61dp"
        android:layout_toRightOf="@+id/button3"
        android:text="+"
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/buttonsub"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="70dp"
        android:layout_height="wrap_content"
        android:layout_below="@+id/buttonadd"
        android:layout_alignStart="@+id/buttonadd"
        android:layout_alignLeft="@+id/buttonadd"
        android:layout_alignEnd="@+id/buttonadd"
        android:layout_alignRight="@+id/buttonadd"
        android:layout_marginStart="-1dp"
        android:layout_marginLeft="-1dp"
        android:layout_marginTop="0dp"
        android:layout_marginEnd="2dp"
        android:layout_marginRight="2dp"
        android:text="-"
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/buttonmul"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="72dp"
        android:layout_height="wrap_content"
        android:layout_below="@+id/buttonsub"
        android:layout_alignStart="@+id/buttonsub"
        android:layout_alignLeft="@+id/buttonsub"
        android:layout_alignParentEnd="true"
        android:layout_alignParentRight="true"
        android:layout_marginStart="0dp"
        android:layout_marginLeft="0dp"
        android:layout_marginTop="5dp"
        android:layout_marginEnd="60dp"
        android:layout_marginRight="60dp"
        android:text="*"
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/button10"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/button7"
        android:layout_toLeftOf="@+id/button2"
        android:text="."
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/button0"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/button8"
        android:layout_alignStart="@+id/button8"
        android:layout_alignLeft="@+id/button8"
        android:text="0"
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/buttonC"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/button9"
        android:layout_alignStart="@+id/button9"
        android:layout_alignLeft="@+id/button9"
        android:text="C"
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/buttondiv"
        style="?android:attr/buttonStyleSmall"
        android:layout_width="wrap_content"
        android:layout_height="wrap_content"
        android:layout_below="@+id/buttonmul"
        android:layout_alignStart="@+id/buttonmul"
        android:layout_alignLeft="@+id/buttonmul"
        android:layout_alignEnd="@+id/buttonmul"
        android:layout_alignRight="@+id/buttonmul"
        android:text="/"
        android:textSize="16sp"
        android:textStyle="bold" />

    <Button
        android:id="@+id/buttoneql"
        android:layout_width="302dp"
        android:layout_height="wrap_content"
        android:layout_below="@+id/button0"
        android:layout_alignStart="@+id/button10"
        android:layout_alignLeft="@+id/button10"
        android:layout_alignEnd="@+id/buttondiv"
        android:layout_alignRight="@+id/buttondiv"
        android:layout_marginStart="-1dp"
        android:layout_marginLeft="-1dp"
        android:layout_marginTop="39dp"
        android:layout_marginEnd="8dp"
        android:layout_marginRight="8dp"
        android:text="="
        android:textSize="20sp"
        android:textStyle="bold" />
</RelativeLayout>
```
## In MainActivity.java :
```
package com.example.simplecalculator;

import androidx.appcompat.app.AppCompatActivity;

import android.os.Bundle;
import android.view.View;
import android.widget.Button;
import android.widget.EditText;
import android.widget.TextView;

public class MainActivity extends AppCompatActivity {

    Button button0, button1, button2, button3, button4, button5, button6,
            button7, button8, button9, buttonAdd, buttonSub, buttonDivision,
            buttonMul, button10, buttonC, buttonEqual;
    EditText editText;
    float mValueOne, mValueTwo;
    boolean Addition, Subtract, Multiplication, Division;
    @Override
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.activity_main);
        button0 = (Button) findViewById(R.id.button0);
        button1 = (Button) findViewById(R.id.button1);
        button2 = (Button) findViewById(R.id.button2);
        button3 = (Button) findViewById(R.id.button3);
        button4 = (Button) findViewById(R.id.button4);
        button5 = (Button) findViewById(R.id.button5);
        button6 = (Button) findViewById(R.id.button6);
        button7 = (Button) findViewById(R.id.button7);
        button8 = (Button) findViewById(R.id.button8);
        button9 = (Button) findViewById(R.id.button9);
        button10 = (Button) findViewById(R.id.button10);
        buttonAdd = (Button) findViewById(R.id.buttonadd);
        buttonSub = (Button) findViewById(R.id.buttonsub);
        buttonMul = (Button) findViewById(R.id.buttonmul);
        buttonDivision = (Button) findViewById(R.id.buttondiv);
        buttonC = (Button) findViewById(R.id.buttonC);
        buttonEqual = (Button) findViewById(R.id.buttoneql);
        editText = (EditText) findViewById(R.id.edt1);
        button1.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                editText.setText(editText.getText() + "1");
            }
        });
        button2.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                editText.setText(editText.getText() + "2");
            }
        });
        button3.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                editText.setText(editText.getText() + "3");
            }
        });
        button4.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                editText.setText(editText.getText() + "4");
            }
        });
        button5.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                editText.setText(editText.getText() + "5");
            }
        });
        button6.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                editText.setText(editText.getText() + "6");
            }
        });
        button7.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                editText.setText(editText.getText() + "7");
            }
        });
        button8.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                editText.setText(editText.getText() + "8");
            }
        });
        button9.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
               editText.setText(editText.getText() + "9");
            }
        });
        button0.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                editText.setText(editText.getText() + "0");
            }
        });
        buttonAdd.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                if (editText == null) {
                    editText.setText("");
                } else {
                    mValueOne = Float.parseFloat(editText.getText() + "");
                    Addition = true;
                    editText.setText(null);
                }
            }
        });
        buttonSub.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                mValueOne = Float.parseFloat(editText.getText() + "");
                Subtract = true;
                editText.setText(null);
            }
        });
        buttonMul.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                mValueOne = Float.parseFloat(editText.getText() + "");
                Multiplication = true;
                editText.setText(null);
            }
        });
        buttonDivision.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                mValueOne = Float.parseFloat(editText.getText() + "");
                Division = true;
                editText.setText(null);
            }
        });
        buttonEqual.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                mValueTwo = Float.parseFloat(editText.getText() + "");
                if (Addition == true) {
                    editText.setText(mValueOne + mValueTwo + "");
                    Addition = false;
                }
                if (Subtract == true) {
                    editText.setText(mValueOne - mValueTwo + "");
                    Subtract = false;
                }
                if (Multiplication == true) {
                    editText.setText(mValueOne * mValueTwo + "");
                    Multiplication = false;
                }
                if (Division == true) {
                    editText.setText(mValueOne / mValueTwo + "");
                    Division = false;
                }
            }
        });
        buttonC.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
                editText.setText("");
            }
        });
        button10.setOnClickListener(new View.OnClickListener() {
            @Override
            public void onClick(View v) {
               editText.setText(editText.getText() + ".");
            }
        });
    }
}
```

## OUTPUT
![Screenshot (19)](https://github.com/Pavithra-M119/simplecalculator/assets/119229774/26324605-48f5-4b4f-ade7-5ea79f5f5bb9)
![Screenshot (20)](https://github.com/Pavithra-M119/simplecalculator/assets/119229774/bd13e736-99c9-4788-84da-a06dadfb77fe)
![Screenshot (21)](https://github.com/Pavithra-M119/simplecalculator/assets/119229774/d79d71c4-a44f-4cec-b9c9-8c41329cbe49)
![Screenshot (22)](https://github.com/Pavithra-M119/simplecalculator/assets/119229774/cb48a330-7e56-4457-a843-294b4a3c996b)





## RESULT
Thus a Simple Android Application develop a program to create simple calculator in Android Studio is developed and executed successfully.
