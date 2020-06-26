# Kotlin-View-to-Image-convertor
Convert a view to an Image in Android apps.




Put the ScreenshotUtil.kt file in your android studio project and change the header "com.example.proj.Utils" to your project name header.

Add this to your androidmanifest file:
```<uses-permission android:name="android.permission.WRITE_EXTERNAL_STORAGE" />```


call the function  Screenshot(activity,context,view) with your activty contexts (usually would be "this") and view with your view id
Example:
```
val uriStr=Screenshot(this,this,imageView)
```

 remember that it returns the URI of the file saved in a string format, to convert it to URI to use it for sharing to apps or whatever purpose you want to use it for:
 ```Uri.parse(uriStr)1```
 
 It also checks if the user has given storage write permissions and asks if not granted already.
