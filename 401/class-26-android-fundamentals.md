# [Class 26 - Android App Fundamentals](https://developer.android.com/guide/components/fundamentals)

- `.apk` files are Android Package files, which are what the device uses to install the app
- `.aab` files are Android App Bundles - an archive file containing info about the app that can be used to generate an `.apk`

## Security features

Each app runs on its own virtual machine in isolation from other apps. The operating system assigns each app a Linux user ID (unknown to the app) that allows it to access the system resources it needs. Apps are only allowed to access the resources they need to run, and must ask permission to access resources like the camera, microphone, etc. Apps that are signed with the same certificate can share a user ID.

## App components

In the Android operating system, any app can access other apps' components, like a social media app using the camera app to capture pictures without "leaving" the original app. Because each component is independent, there is no `main()` function. Apps access each others' components by sending a message to the system.

### Activities

Each different screen in an app that a user can interact with is an "activity." Each activity is independent of the others, and can potentially be accessed by different apps (i.e., a photo app might access a messaging app to share a photo). Activities give the system information like what needs to be running right now, what was running recently that might need to run again soon, what would need to be restored if the app crashes, and how the app can interact with other apps.

### Services

Services are background processes that the user can't interact with, like playing music or retrieving new messages. Playing music is an example of a started service, which the system is supposed to run until they're done with whatever they're doing. Services like music get a high priority because users will notice when they're interrupted, while other services can be paused to conserve system resources.

Bound services are essentially APIs that run because another app wants to use the service.

### Broadcast Receivers

Broadcast receivers are another non-interactive component. They allow apps to receive data outside of the user flow and respond to things like the screen being on or off, the battery being low, etc. Apps can also tell other apps things, like that they've finished a process they other app might need.

### Content Providers

Content providers manage app information, like a user's contacts. Apps can map the data they receive to their own URI namespace, and make those URIs available to other apps.

### Activating components

Activities, Services, and Receivers are activated by "intents," which are asynchronous messages that bind compoents to each other at runtime. Intents define the action to perform and, if relevant, the URI of data needed to perform that action. Content providers are activated by requests from a `ContentResolver`.

## The manifest file

Each app has a manifest at `AndroidManifest.xml`. This file is at the root of the app directory, and performs the following functions:

- **Declaring components**
- **Identifying user permissions**
- **Declaring minimum API level**
- **Declaring hardware/software features used by the app**
- **Declaring API libraries the app links to**

## App resources

Apps can include resources like sound and images, as well as .xml files that control the visual appearance of the app.

## Things I'd like to know more about

How to make sure apps are compatible with different systems.
