# Read: 36 - Cognito

## Amplify and Cognito

> The **Amplify Auth** category provides an interface for authenticating a user. Behind the scenes, it provides the necessary authorization to the other Amplify categories. It comes with default, built-in support for Amazon Cognito User Pool and Identity Pool. The Amplify CLI helps you to create and configure the auth category with an authentication provider.

![cognito](https://i.stack.imgur.com/8Fe2t.png)

 **Prerequisites**

+ An Android application targeting at least Android SDK API level 16 with Amplify libraries integrated.

**Configure Auth Category**

1. amplify add auth : we use this command to To start provisioning auth resources in the backend, after that you will see this screen.

```
? Do you want to use the default authentication and security configuration?
    `Default configuration`
? How do you want users to be able to sign in?
    `Username`
? Do you want to configure advanced settings?
    `No, I am done.`
```

2. then we do the amplify push to push the changes to the cloude.

***

**dependencies for cognito**

```
dependencies {
    implementation 'com.amplifyframework:aws-auth-cognito:1.24.0'
}
```

**Initialize Amplify Auth**

```
// Add this line, to include the Auth plugin.
Amplify.addPlugin(new AWSCognitoAuthPlugin());
Amplify.configure(getApplicationContext());
```