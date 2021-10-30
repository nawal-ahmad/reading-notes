# Read: 26 - Android Fundamentals

- Android apps can be written using Kotlin, Java, C++ ...etc languages. 
- Android SDK tools compile the code along with any data and resource files into an APK or an Android App Bundle.
- Android package is an archive file with an .apk suffix, contains the contents of an Android app that are required at runtime and it is the file that Android-powered devices use to install the app.
- An Android App Bundle is an archive file with an .aab suffix, contains the contents of an Android app project including some additional metadata that is not required at runtime.
- An AAB is a publishing format and is not installable on Android devices, it defers APK generation and signing to a later stage.

**Android security features:**
1. The Android operating system is a multi-user Linux system in which each app is a different user.
2. By default, the system assigns each app a unique Linux user ID (the ID is used only by the system and is unknown to the app). 
3. The system sets permissions for all the files in an app so that only the user ID assigned to that app can access them. 
4. Each process has its own virtual machine (VM), so an app's code runs in isolation from other apps.
5. By default, every app runs in its own Linux process.
6. It's possible to arrange for two apps to share the same Linux user ID, in which case they are able to access each other's files
7. To conserve system resources, apps with the same user ID can also arrange to run in the same Linux process and share the same VM, The apps must also be signed with the same certificate.
8. An app can request permission to access device data such as the device's location, camera, and Bluetooth connection. 


 **App components**
They are essential building blocks of an Android app. Each component is an entry point through which the system or a user can enter your app. Some components depend on others.


**Types of app components:**
1. Activities: its the entry point for interacting with the user. It represents a single screen with a user interface.
2. Services:  is a general-purpose entry point for keeping an app running in the background for all kinds of reasons.
3. Broadcast receivers: is a component that enables the system to deliver events to the app outside of a regular user flow, allowing the app to respond to system-wide broadcast announcements.
4. Content providers: manages a shared set of app data that you can store in the file system, in a SQLite database, on the web, or on any other persistent storage location that your app can access. 


**The manifest file**
 Before the Android system can start an app component, the system must know that the component exists by reading the app's manifest file, AndroidManifest.xml. Your app must declare all its components in this file, which must be at the root of the app project directory.

**Declaring components**
manifest file can declare an activity as follows: 

```
<?xml version="1.0" encoding="utf-8"?>
<manifest ... >
    <application android:icon="@drawable/app_icon.png" ... >
        <activity android:name="com.example.project.ExampleActivity"
                  android:label="@string/example_label" ... >
        </activity>
        ...
    </application>
</manifest>
```
