# Lab_2_Layout
Lab 2

1.利用LinearLayout实现如下界面

<img height=400 width=500 src="https://github.com/jinrongrong815/img_folder/blob/master/Lab_2_1.png">

2.利用ConstraintLayout实现如下界面

<img height=400 width=500 src="https://github.com/jinrongrong815/img_folder/blob/master/Lab_2_2q.png">

3.利用TableLayout实现如下界面

<img height=400 width=300 src="https://github.com/jinrongrong815/img_folder/blob/master/Lab_2_3q.png">

结果截图：

mainlayout：

<img height=350 width=500 src="https://github.com/jinrongrong815/img_folder/blob/master/Lab_2_mainlayout.png">

linearlayout:

<img height=350 width=500 src="https://github.com/jinrongrong815/img_folder/blob/master/Lab_2_linearlayout.png">

constraintlayout:

<img height=350 width=500 src="https://github.com/jinrongrong815/img_folder/blob/master/Lab_2_constraintlayout.png">

tablelayout:

<img height=350 width=500 src="https://github.com/jinrongrong815/img_folder/blob/master/Lab_2_tablelayout.png">

关键代码：

***MainLayout.java***

public class MainLayout extends AppCompatActivity {

    Button b1 , b2, b3;
    Intent a1, a2, a3;
    @Override
    
    protected void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);
        setContentView(R.layout.main_layout);
        b1 = findViewById(R.id.button);
        b2 = findViewById(R.id.button2);
        b3 = findViewById(R.id.button3);
        b1.setOnClickListener(new ButtonListener());
        b2.setOnClickListener(new ButtonListener());
        b3.setOnClickListener(new ButtonListener());
    }
    
    private class ButtonListener implements View.OnClickListener {
        @Override
        public void onClick(View v) {
            switch (v.getId()) {
                case R.id.button:
                    a1 = new Intent(MainLayout.this, LinearLayout.class);
                    startActivity(a1);
                    break;

                case R.id.button2:
                    a2 = new Intent(MainLayout.this, ConstraintLayout.class);
                    startActivity(a2);
                    break;

                case R.id.button3:
                    a3 = new Intent(MainLayout.this, TableLayout.class);
                    startActivity(a3);
                    break;
                default:
                    break;
            }
        }
    }
}

***main_layout.xml***

    <Button
        android:id="@+id/button"
        android:layout_width="120dp"
        android:layout_height="wrap_content"
        android:layout_marginBottom="8dp"
        android:text="@string/linear"
        android:textAllCaps="false"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent"
        app:layout_constraintVertical_bias="0.171" />

    <Button
        android:id="@+id/button2"
        android:layout_width="120dp"
        android:layout_height="wrap_content"
        android:layout_marginStart="8dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginBottom="2dp"
        android:text="@string/constraint"
        android:textAllCaps="false"
        app:layout_constraintBottom_toTopOf="@+id/button3"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toBottomOf="@+id/button" />

    <Button
        android:id="@+id/button3"
        android:layout_width="120dp"
        android:layout_height="wrap_content"
        android:layout_marginBottom="124dp"
        android:text="@string/table"
        android:textAllCaps="false"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

***linear_layout.xml***

    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
    
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <TextView
            android:gravity="center"
            android:layout_weight="1"
            android:background="@drawable/textview"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/t11" />

        <TextView
            android:gravity="center"
            android:layout_weight="1"
            android:background="@drawable/textview"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/t12" />

        <TextView
            android:gravity="center"
            android:background="@drawable/textview"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/t13" />

        <TextView
            android:gravity="center"
            android:background="@drawable/textview"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/t14" />
    </LinearLayout>
    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <TextView
            android:gravity="center"
            android:background="@drawable/textview"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/t21" />

        <TextView
            android:gravity="center"
            android:background="@drawable/textview"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/t22" />

        <TextView
            android:gravity="center"
            android:background="@drawable/textview"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/t23" />

        <TextView
            android:gravity="center"
            android:background="@drawable/textview"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/t24" />
    </LinearLayout>

    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <TextView
            android:gravity="center"
            android:background="@drawable/textview"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/t31" />

        <TextView
            android:gravity="center"
            android:background="@drawable/textview"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/t32" />

        <TextView
            android:gravity="center"
            android:background="@drawable/textview"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/t33" />

        <TextView
            android:gravity="center"
            android:background="@drawable/textview"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/t34" />
    </LinearLayout>

    <LinearLayout xmlns:android="http://schemas.android.com/apk/res/android"
        android:layout_width="match_parent"
        android:layout_height="wrap_content">

        <TextView
            android:gravity="center"
            android:background="@drawable/textview"
            android:layout_width="44dp"
            android:layout_height="wrap_content"
            android:layout_weight="1"
            android:textColor="#ffffff"
            android:text="@string/t41" />

        <TextView
            android:gravity="center"
            android:background="@drawable/textview"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/t42" />

        <TextView
            android:gravity="center"
            android:background="@drawable/textview"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/t43" />

        <TextView
            android:gravity="center"
            android:background="@drawable/textview"
            android:layout_weight="1"
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/t44" />
    </LinearLayout>

</LinearLayout>

***constraint_layout.xml***

<?xml version="1.0" encoding="utf-8"?>

    <TextView
        android:id="@+id/textView2"
        android:layout_width="250dp"
        android:layout_height="150dp"
        android:background="@android:color/holo_orange_dark"
        android:gravity="center"
        android:text="@string/button2"
        android:textSize="20sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView5"
        android:layout_width="250dp"
        android:layout_height="155dp"
        android:layout_marginEnd="8dp"
        android:background="@android:color/holo_red_dark"
        android:gravity="center"
        android:text="@string/button1"
        android:textSize="20sp"
        app:layout_constraintEnd_toStartOf="@+id/textView2"
        app:layout_constraintHorizontal_bias="0.0"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView6"
        android:layout_width="250dp"
        android:layout_height="150dp"
        android:layout_marginStart="8dp"
        android:background="#ffff00"
        android:gravity="center"
        android:text="@string/button3"
        android:textSize="20sp"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="1.0"
        app:layout_constraintStart_toEndOf="@+id/textView2"
        app:layout_constraintTop_toTopOf="parent" />

    <TextView
        android:id="@+id/textView7"
        android:layout_width="255dp"
        android:layout_height="150dp"
        android:layout_marginStart="8dp"
        android:layout_marginTop="8dp"
        android:layout_marginEnd="8dp"
        android:layout_marginBottom="8dp"
        android:background="#0000ff"
        android:gravity="center"
        android:text="@string/button5"
        android:textSize="20sp"
        app:layout_constraintBottom_toBottomOf="@+id/textView10"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintTop_toTopOf="@+id/textView2" />

    <TextView
        android:id="@+id/textView8"
        android:layout_width="250dp"
        android:layout_height="150dp"
        android:layout_marginStart="8dp"
        android:layout_marginEnd="8dp"
        android:background="#7fff00"
        android:gravity="center"
        android:text="@string/button4"
        android:textSize="20sp"
        app:layout_constraintBaseline_toBaselineOf="@+id/textView7"
        app:layout_constraintEnd_toStartOf="@+id/textView7"
        app:layout_constraintHorizontal_bias="0.7"
        app:layout_constraintStart_toStartOf="parent" />

    <TextView
        android:id="@+id/textView9"
        android:layout_width="250dp"
        android:layout_height="150dp"
        android:layout_marginStart="8dp"
        android:layout_marginEnd="8dp"
        android:background="#4b0082"
        android:gravity="center"
        android:text="@string/button6"
        android:textSize="20sp"
        app:layout_constraintBaseline_toBaselineOf="@+id/textView7"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintHorizontal_bias="0.3"
        app:layout_constraintStart_toEndOf="@+id/textView7" />

    <TextView
        android:id="@+id/textView10"
        android:layout_width="0dp"
        android:layout_height="150dp"
        android:background="#ee82ee"
        android:gravity="center"
        android:text="@string/button7"
        android:textSize="20sp"
        app:layout_constraintBottom_toBottomOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintStart_toStartOf="parent" />

***table_layout.xml***

<?xml version="1.0" encoding="utf-8"?>

    <TableRow>
        <TextView
            android:textColor="#ffffff"
            android:text="@string/open" />

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:gravity="end"
            android:textColor="#ffffff"
            android:text="@string/o" />
    </TableRow>

    <TableRow>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/save" />

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:gravity="end"
            android:textColor="#ffffff"
            android:text="@string/s" />
    </TableRow>

    <TableRow>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/sa" />

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:gravity="end"
            android:textColor="#ffffff"
            android:text="@string/cs" />
    </TableRow>

    <!--加线-->
    <TextView
        android:layout_width="match_parent"
        android:layout_height="1dp"
        android:background="#ffffff"/>

    <TableRow>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/im" />

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="" />
    </TableRow>

    <TableRow>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/ex" />

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:gravity="end"
            android:textColor="#ffffff"
            android:text="@string/e" />
    </TableRow>

    <!--加线-->
    <TextView
        android:layout_width="match_parent"
        android:layout_height="1dp"
        android:background="#ffffff"/>

    <TableRow>
        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:textColor="#ffffff"
            android:text="@string/q" />

        <TextView
            android:layout_width="wrap_content"
            android:layout_height="wrap_content"
            android:text="" />
    </TableRow>
