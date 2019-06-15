# live_cams

Add a new activity to display a list of traffic camera locations. The list should display name (label) and image for each camera. 


Data can be loaded from http://brisksoft.us/ad340/traffic_cameras_merged.json (Links to an external site.)Links to an external site. . 

Note - your code will need to account for missing SDOT camera images.


JSON data should be mapped to a Camera Java class for use within your application,
Your activity should check the device network status and display a graceful warning if not connected. You should only make a network request if your application has connectivity


Update one of the buttons on your main screen to launch this new activity when clicked

Hint -

Make sure your application specifies this permission in AndroidManifest.xml: 
<uses-permission android:name="android.permission.INTERNET" />
Because the  traffic-camera image urls don't use HTTPS, you'll need to set this attribute on your 'application' tag in AndroidManifest.xml:
android:usesCleartextTraffic="true" 
If unsure how to check network status, see this example - https://github.com/googlesamples/android-BasicNetworking/blob/master/Application/src/main/java/com/example/android/basicnetworking/MainActivity.java#L93 (Links to an external site.)Links to an external site.

See Volley's standard request examples for loading JSON data
You can use Picasso, Glide, or Volley's ImageLoader class to load images into a view

Your recyclerView or listView adapter should defined outside your data-parsing loop,

After parsing all the JSON data, you'll need to trigger a UI update. You can use the notifyDataSetChanged() method - https://developer.android.com/reference/android/widget/ArrayAdapter (Links to an external site.)Links to an external site.
 

Video tutorial on making API requests (Links to an external site.)Links to an external site.



Extra OPTIONAL:

Add a UI element that lets users filter results by ownership (WSDOT or SDOT)
 

 
