# Helloworld Android代码实现

在Android studio上新建android项目，在建立第一个项目的时候，软件会联网下载gradle相关的文件，但由于需要连到国外服务器进行下载，因此下载较慢。

安装android sdk相关的文件，安装最新的Android 8.0对应的API版本，用于开发最新的android程序。

新建项目之后，软件会在第一个项目中自动写入Helloworld相关的代码，在运行后，软件会提示安装相应的安卓虚拟机，我安装的是Pixel XL API 26，用于运行编写的安卓程序。

运行后，在屏幕上的安卓虚拟机上显示Helloworld的信息。

<div align=center>
  <img width="300" height="600" src="https://github.com/reeseyuan/Android-Course/blob/master/Helloworld/image.png"/>
</div>

在一个android程序中，界面的相关布局程序写在activity_main.xml中，相关逻辑等代码写在MainActivity.java中。

如下代码为MainActivity.java中的代码：

package com.example.reese.helloworld;

import android.support.v7.app.AppCompatActivity;

import android.os.Bundle;



public class MainActivity extends AppCompatActivity {

  protected void onCreate(Bundle savedInstanceState) {

   super.onCreate(savedInstanceState);

   setContentView(R.layout.activity_main);

  }

}


在代码中，MainActivity继承自AppCompatActivity，Activity是android系统提供的一个活动基类，项目中的所有活动都必须继承它或者是它的子类才能拥有活动的特性。

onCreate()方法是一个活动在被创建时必定要执行的方法。

在android程序中的设计是讲究逻辑和视图分离的，因此需要在布局文件中编写界面，然后在活动中引入进来

在onCreate()方法的第二行调用了setContentView()方法，就是给当前的活动引入了一个activity_main布局，因此Helloworld就是在这个文件中定义的，打开activity_main.xml文件观察其中的代码。


<?xml version="1.0" encoding="utf-8"?>

<android.support.constraint.ConstraintLayout xmlns:android="http://schemas.android.com/apk/res/android"

   xmlns:app="http://schemas.android.com/apk/res-auto"

   xmlns:tools="http://schemas.android.com/tools"

   android:layout_width="match_parent"

   android:layout_height="match_parent"

   tools:context="com.example.reese.helloworld.MainActivity">

   <TextView

   android:layout_width="wrap_content"

   android:layout_height="wrap_content"

   android:text="Hello World!"

   app:layout_constraintBottom_toBottomOf="parent"

   app:layout_constraintLeft_toLeftOf="parent"

   app:layout_constraintRight_toRightOf="parent"

   app:layout_constraintTop_toTopOf="parent" />

</android.support.constraint.ConstraintLayout>



代码中的TextView是android提供的一个控件，用于在布局中显示文字，因此在上图中的`Helloworld`就是通过`android:text="Hello World!"`这句代码定义的。




