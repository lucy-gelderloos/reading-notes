# Class 27 Reading Notes

## [Android SharedPreferences](https://developer.android.com/training/data-storage/shared-preferences)

The SharedPreferences API can hold a small number of key-value pairs and has simple methods for reading and writing them. They are edited using the SharedPreferencesEditor object, and can be read using methods like getInt() or getString().

## [Espresso](https://developer.android.com/training/testing/espresso)

Espresso lets you write tests for Android apps and runs them efficiently. The tests can behave like users, but don't have direct access to the application's utilities and views to keep tests more stable. Views are easy to test if they each have a unique R.id, but if not, Espresso provides ways to target them. See [Espresso Recipes](https://developer.android.com/training/testing/espresso/recipes) for tutorials on setting up some common Espresso tests.

## [Espresso Test Recorder](https://developer.android.com/studio/test/other-testing-tools/espresso-test-recorder)

The Espresso Test Recorder allows you to create tests by recording your interaction with the app, rather than writing each test as code. First, start the test recording and perform the actions you want to test. Espresso records these, then allows you to add assertions (like what certain text should read at certain points).

## [Tasks and the Back Stack](https://developer.android.com/guide/components/activities/tasks-and-back-stack)

When users move from one activity to another, each new activity is added to the top of the "back stack," which pauses previous activities but maintains them in order so pressing "back" will take the user to the previous screen. Each application has its own back stack, including when running in multi-windowed mode. Views may be in the stack more than once if the user is bouncing around the app. There are activity attributes you can use to control this behavior if you want to go back to things outside the stack.

## Things I'd like to know more about

Still working on understanding new concepts/vocab.
