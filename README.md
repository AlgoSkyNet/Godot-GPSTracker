#Godot-GPSTracker
- GPS (global position system) support on Godot engine for Android. (https://github.com/godotengine/)

- Godot version 2.1.1 stable.

##How to use
- Drop the gpstracker folder inside godot/modules

- Move the gpstracker/GPSTracker.java to godot/platform/android/java/src/org/godotengine/godot

**Note:** The gpstracker/android.jar is taken from  *android-sdk-linux/platforms/android-16*. You may choose to use any other api version.

###Compile
1. #> scons platform=android
2. cd godot/platform/android/java
3. #> ./gradlew build
4. The resulting apk will be available at godot/platform/android/java/build/outputs/apk
 
###Configure
Add the following in the engine.cfg file:

> [android]

> modules="org/godotengine/godot/GPSTracker"

**Use them in the script:**

> var gps = Globals.get_singleton("GPSTracker")

> var latitude = gps.getLatitude()   # latitude

> var longitude = gps.getLongitude() # longitude

###Build the game apk
From the settings of the godot engine UI:

> Export->Target->Android


Custom Package (Debug/Release): 
> Point to the newly built apk

> Permission check: Access Fine Location

> Permission check: Internet

####License
MIT
