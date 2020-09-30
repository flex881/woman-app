# woman-app



RelativeLayout xmlns:android="http://schemas.android.com/apk/res/android"
    xmlns:tools="http://schemas.android.com/tools"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    android:background="@drawable/a"
    android:paddingLeft="@dimen/activity_horizontal_margin"
    android:paddingTop="@dimen/activity_vertical_margin"
    android:paddingRight="@dimen/activity_horizontal_margin"
    android:paddingBottom="@dimen/activity_vertical_margin"
    tools:context=".MainActivity">


    <Button
        android:id="@+id/button1"
        android:layout_width="fill_parent"
        android:layout_height="wrap_content"
        android:layout_above="@+id/button2"
        android:layout_alignLeft="@+id/button2"
        android:layout_marginBottom="71dp"
        android:onClick="register"
        android:text="Register" />

    <Button
        android:id="@+id/button3"
        android:layout_width="fill_parent"
        android:layout_height="wrap_content"
        android:layout_below="@+id/button2"
        android:layout_alignLeft="@+id/button2"
        android:layout_marginTop="74dp"
        android:onClick="display_no"
        android:text="View Registered" />

    <Button
        android:id="@+id/button2"
        android:layout_width="fill_parent"
        android:layout_height="wrap_content"
        android:layout_centerHorizontal="true"
        android:layout_centerVertical="true"
        android:onClick="instruct"
        android:text="Instructions" />

    <Button
        android:id="@+id/button4"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_alignParentBottom="true"
        android:layout_centerHorizontal="true"
        android:onClick="verify"
        android:text="Register Your Mobile Number" />

</RelativeLayout>



<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="com.woman.womensafetyapp"
    android:versionCode="1"
    android:versionName="1.0" >

    <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
    <uses-permission android:name="android.permission.INTERNET" />
    <uses-permission android:name="android.permission.SEND_SMS" />
    <uses-permission android:name="android.permission.READ_PHONE_STATE" >
    </uses-permission>
    <application
        android:allowBackup="true"
        android:icon="@drawable/ic_launcher"
        android:label="@string/app_name"
        android:theme="@style/AppTheme" >
        <activity
            android:name="com.woman.womensafetyapp.MainActivity"
            android:label="@string/app_name" >
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />

                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
        <activity
            android:name="com.prabhu.womensafetyapp.Register"
            android:label="@string/title_activity_register"
            android:parentActivityName="com.woman.womensafetyapp.MainActivity" >
            <meta-data
                android:name="android.support.PARENT_ACTIVITY"
                android:value="com.woman.womensafetyapp.MainActivity" />
        </activity>
        <activity
            android:name="com.woman.womensafetyapp.Display"woman
            android:label="@string/title_activity_display"
            android:parentActivityName="com.woman.womensafetyapp.MainActivity" >
            <meta-data
                android:name="android.support.PARENT_ACTIVITY"
                android:value="com.woman.womensafetyapp.MainActivity" />
        </activity>
        <service android:name="com.woman.womensafetyapp.BgService" />
        <
            android:name="com.woman.womensafetyapp.Instructions"
            android:label="@string/title_activity_instructions"
            android:parentActivityName="com.woman.womensafetyapp.MainActivity" >
            <meta-data
                android:name="android.support.PARENT_ACTIVITY"
                android:value="com.woman.womensafetyapp.MainActivity" />
        </activity>
        <activity
            android:name="com.woman.womensafetyapp.Verify"
            android:label="@string/title_activity_verify"
            android:parentActivityName="com.woman.womensafetyapp.MainActivity" >
            <meta-data
                android:name="android.support.PARENT_ACTIVITY"
                android:value="com.woman.womensafetyapp.MainActivity" />
        </activity>
    </application>
</manifest>
