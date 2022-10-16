# Intents

## [Intent Filters](https://developer.android.com/training/basics/intents/filters)

Android has some standard intents that can be accessed by other applications. For instance, if your app allows sharing of photos or messages, you can use the `ACTION_SEND` intent to make your app show up as an option when the user shares something from another app (the camera, for instance). You'll also need to add an intent filter to your app's manifest. There, you can declare the intent's action, data, and category. The intent can be read just like an internal intent (by calling `getIntent()` on the activity).

## [Implicit vs. Explicit Intents](https://developer.android.com/guide/components/intents-filters#Types)

Explicit intents specify the application that will perform an action, so it's best to use them inside your own application to access activities. Implicit intents only declare an action to perform, so they can be used to access other applications. Intent filters declare what kinds of intents an external app can receive.

## Things I'd like to know more about

What other setup/configuration needs to be done to access other apps from my app or allow other apps to access mine.
