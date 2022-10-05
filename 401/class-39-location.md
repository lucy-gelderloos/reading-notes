# Class 39 - [Location](https://developer.android.com/training/location/retrieve-current)

You can use the fused location provider API to access the device's last known (aka current) location.

To prepare:

- [Set up Google Play services](https://developers.google.com/android/guides/setup)
- [Set app permissions](https://developer.android.com/training/location/permissions)

To create a location services client, include this code in the activity's onCreate:

```java
fusedLocationClient = LocationServices.getFusedLocationProviderClient(this);
```

Then use the `getLastLocation()` method to get a location object (which will be null if no location information is available). If it's important to have the most recent data information, you can use `getCurrentLocation()` instead; be aware this may use more resources on the device.

## Things I'd like to know more about

In what situations it's actually necessary to have precise locations at all times.
