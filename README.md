# Location
Dealing with user location 

* Category: Either foreground location or background location
* Accuracy: Either precise location or approximate location.

* Foreground-Location: [ Navigation: turns - Message: Share Current Location ]
    shares or receives location information only once, or for a defined amount of time.
    
    Visible Activity or Foreground Service (recommended)
    
    Foreground Server on Android 10 (API level 29) and higher must declare this foreground service type. in the Manifest.
      <service
        android:name="MyNavigationService"
        android:foregroundServiceType="location" ... >
      </service>
      
    Permissions: (RunTime)
      <!-- Always include this permission -->
      <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
      <!-- Include only if your app benefits from precise location access. -->
      <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION" />
      

* Background-Location
    app constantly shares location with other users.
    
    accesses the device's current location in any situation other than the ones described in the foreground location section.
    
    Permissions: (RunTime)
      <!-- Required only when requesting background location access on Android 10 (API level 29) and higher. -->
      <uses-permission android:name="android.permission.ACCESS_BACKGROUND_LOCATION" />
