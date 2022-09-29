# [Publishing your app](https://developer.android.com/studio/publish)

## Preparing you app for release

- Configuration: remove log calls, `android:debuggable` from the manifest. Set version information and any other settings necessary to meet Google Play requirements. In Gradle files, set "release" build type.
- Build & Sign: using Gradle files with the "release" build type
- Test: thoroughly test the app on at least one handset device and one tablet device.
- Update: any other resources, like graphics, are available and accessible
- Remote: make sure any remote resources are available and accessible

Apps can be distributed through marketplaces like Google Play, through a website, or individually. To prepare for releasing through the Play store:

- Prepare promotional materials
- Configure options and upload assets
- Publishing a release version

If you distribute through your own site, be aware that many users' devices default to not allowing apps from unknown publishers.

## Things I'd like to know more about

How to create promotional materials and other assets, like app icons.
