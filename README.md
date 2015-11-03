# OpenCV 3.0 Camera Preview Example 

opencvcamerapreviewsample-melvincabatuan created by Classroom for GitHub

This project illustrates how to utilize a 3rd party library, e.x. OpenCV in Android.

## Prerequisite:

1. Download and extract OpenCV 3.0 for Android from http://opencv.org/.
2. Create a new project in Android Studio with "No Activity".

![alt tag](https://github.com/DeLaSalleUniversity-Manila/opencvcamerapreviewsample-melvincabatuan/blob/master/OpenCV_001.png)

![alt tag](https://github.com/DeLaSalleUniversity-Manila/opencvcamerapreviewsample-melvincabatuan/blob/master/OpenCV_002.png)

![alt tag](https://github.com/DeLaSalleUniversity-Manila/opencvcamerapreviewsample-melvincabatuan/blob/master/OpenCV_003.png)

## Procedures:

1. Create a folder called "libraries" inside your Android Studio project.

2. Copy the entire content of 'OpenCV-android-sdk/sdk/java' into "libraries" directory created in Procedure 2. 

3. Rename 'AndroidStudioProjects/OpenCV3-CameraPreview/libraries/java' into 'AndroidStudioProjects/OpenCV3-CameraPreview/libraries/opencv' 
4. Add "include ':libraries:opencv'" to 'settings.gradle'.
5. Create a 'build.gradle' file inside 'AndroidStudioProjects/OpenCV3-CameraPreview/libraries/opencv'
Ex. 

```gradle
apply plugin: 'android-library'

buildscript {
  repositories {
    mavenCentral()
  }
  dependencies {
    classpath 'com.android.tools.build:gradle:1.3.0'
  }
}


android {
    compileSdkVersion 22
    buildToolsVersion "22.0.1"

    defaultConfig {
    	minSdkVersion 15
    	targetSdkVersion 22
    	versionCode 3000
    	versionName "3.0.0"
    }
	
	sourceSets {
    	main {
      		manifest.srcFile 'AndroidManifest.xml'
      		java.srcDirs = ['src']
      		resources.srcDirs = ['src']
      		res.srcDirs = ['res']
      		aidl.srcDirs = ['src']
    	}
	}
}
```
Note: This file is subject to your own 'compileSdkVersion','buildToolsVersion','targetSdkVersion', etc.

* Go to 'File/Project Structure' and inside 'Modules' click 'app', then from the Tab pick 'Dependencies', click '+' to add new dependency, pick 'Module Dependency', and add 'library:opencv' dependency to your project, then click OK.

![alt tag](https://github.com/DeLaSalleUniversity-Manila/opencvcamerapreviewsample-melvincabatuan/blob/master/OpenCV_004.png)

## Adding the Sample Project

1. Go to 'OpenCV-android-sdk/samples', pick a sample project, e.x. 'tutorial-1-camerapreview'.  

2. Delete the 'res' folder inside your own project app/src/main, then place the res folder from the samples inside your app/src/main folder.

3. Delete the 'java' folder from app/src/main, then copy the 'src' folder from the samples in there. Rename the copied 'src' folder into 'java'.

4. Replace the manifest inside your own project using the samples manifest.

E.x.

```xml
<?xml version="1.0" encoding="utf-8"?>
<manifest xmlns:android="http://schemas.android.com/apk/res/android"
    package="org.opencv.samples.tutorial1"
    android:versionCode="301"
    android:versionName="3.01">

    <application
        android:label="@string/app_name"
        android:icon="@drawable/icon"
        android:theme="@android:style/Theme.NoTitleBar.Fullscreen" >

        <activity android:name="Tutorial1Activity"
            android:label="@string/app_name"
            android:screenOrientation="landscape"
            android:configChanges="keyboardHidden|orientation">
            <intent-filter>
                <action android:name="android.intent.action.MAIN" />
                <category android:name="android.intent.category.LAUNCHER" />
            </intent-filter>
        </activity>
    </application>

    <supports-screens android:resizeable="true"
        android:smallScreens="true"
        android:normalScreens="true"
        android:largeScreens="true"
        android:anyDensity="true" />

    <uses-sdk android:minSdkVersion="8" />

    <uses-permission android:name="android.permission.CAMERA"/>

    <uses-feature android:name="android.hardware.camera" android:required="false"/>
    <uses-feature android:name="android.hardware.camera.autofocus" android:required="false"/>
    <uses-feature android:name="android.hardware.camera.front" android:required="false"/>
    <uses-feature android:name="android.hardware.camera.front.autofocus" android:required="false"/>

</manifest>
```

## Accept

To accept the assignment, click the following URL:

https://classroom.github.com/assignment-invitations/464e11aa7991992628993a725524a17f

## Sample Solution:

https://github.com/DeLaSalleUniversity-Manila/opencvcamerapreviewsample-melvincabatuan

## Submission Procedure with Git: 

```shell
$ cd /path/to/your/android/app/
$ git init
$ git add –all
$ git commit -m "your message, e.x. Assignment 1 submission"
$ git remote add origin <Assignment link copied from assignment github, e.x. https://github.com/DeLaSalleUniversity-Manila/secondactivityassignment-melvincabatuan.git>
$ git push -u origin master
<then Enter Username and Password>
```


## Screenshot:

![alt tag](https://github.com/DeLaSalleUniversity-Manila/opencvcamerapreviewsample-melvincabatuan/blob/master/device-2015-11-02-084936.png)

![alt tag](https://github.com/DeLaSalleUniversity-Manila/opencvcamerapreviewsample-melvincabatuan/blob/master/device-2015-11-02-085223.png)

"*There is nothing funny about Halloween. This sarcastic festival reflects, rather, an infernal demand for revenge by children on the adult world.*" - Jean Baudrillard
