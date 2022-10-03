# Class 36 reading notes - Amplify and Cognito

## [Getting Started](https://docs.amplify.aws/lib/auth/getting-started/q/platform/android/)

Amplify can work with Cognito to authenticate users. It can be added from the command line using the command `amplify add auth` (use the default setup prompts; push usng `amplify push`). Add `implementation 'com.amplifyframework:aws-auth-cognito:1.37.5'` to your build.gradle. The authentication session can be generated when the app starts, and can be accessed within the onCreate method.

## [Sign In](https://docs.amplify.aws/lib/auth/signin/q/platform/android/)

You can use Auth to have users register with a username, password, and email, with options to verify both email and phone number. Once you've created inputs for the user to sign in, Auth can validate that sign-in.

Note that using multi-factor authentication requires quite a bit more setup and must be done at the `amplify add auth` stage.

## Things I'd like to know more about

Is there any way (or reason) to use non-Amplify authentication with an app that uses Amplify for other services?
