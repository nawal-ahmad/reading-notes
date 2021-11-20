# Read: 41 - Intent Filters

## Intent Filters

**Allowing Other Apps to Start Your Activity**

* If the app can perform an action that might be useful from another app, your app should be prepared to respond to action requests by specifying the appropriate intent filter in the activity.

* to allow other apps to start your activity in this way, you need to add an `<intent-filter>` element in your manifest file for the corresponding `<activity>` element.

**Add an Intent Filter**

The system may send a given Intent to an activity if that activity has an intent filter fulfills the following criteria of the Intent object:

* Action: string naming the action to perform. Usually one of the platform-defined values such as **ACTION_SEND** or **ACTION_VIEW**.

* Data: description of the data associated with the intent.

* Category: Provides an additional way to characterize the activity handling the intent, usually related to the user gesture or location from which it's started.

example of the intent filter:

```
<activity android:name="ShareActivity">
    <intent-filter>
        <action android:name="android.intent.action.SEND"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:mimeType="text/plain"/>
        <data android:mimeType="image/*"/>
    </intent-filter>
</activity>
```

* Each incoming intent specifies only one action and one data type, but it's OK to declare multiple instances of the \<action>, \<category>, and \<data> elements in each \<intent-filter> .

* One activity can have multiple intent filters like this:

```
<activity android:name="ShareActivity">
    <!-- filter for sending text; accepts SENDTO action with sms URI schemes -->
    <intent-filter>
        <action android:name="android.intent.action.SENDTO"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:scheme="sms" />
        <data android:scheme="smsto" />
    </intent-filter>
    <!-- filter for sending text or images; accepts SEND action and text or image data -->
    <intent-filter>
        <action android:name="android.intent.action.SEND"/>
        <category android:name="android.intent.category.DEFAULT"/>
        <data android:mimeType="image/*"/>
        <data android:mimeType="text/plain"/>
    </intent-filter>
</activity>
```