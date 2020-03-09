# ml-barcode-scanner
The project contains ML based barcode scanner developed with the help of Google ML Kit barcode scanner tutorial project 
with some customizations according to our need.

To use the repository add : (root/build.gradle)
allprojects {
		repositories {
			maven { url 'https://jitpack.io' }
		}
	}
  
AND : 
dependencies {
	        implementation 'com.github.medha742:ml-barcode-scanner:Tag'
	}
in app/build.gradle

To use in a layout : 

 <!-- rectangle width and height is the white rectangle dimensions 
    which specifies the rectangle boundary the barcode must come under --> 

<androidx.coordinatorlayout.widget.CoordinatorLayout 
    xmlns:android="http://schemas.android.com/apk/res/android"
    android:layout_width="match_parent"
    android:layout_height="match_parent"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    android:keepScreenOn="true">

    <com.mogambo.custombarcodescanner.camera.CameraSourcePreview
        android:id="@+id/camera_preview"
        android:layout_width="match_parent"
        app:rectangle_width="75" 
        app:rectangle_height="35"
        android:layout_height="match_parent">

        <include layout="@layout/camera_preview_overlay_kotlin"/>

    </com.mogambo.custombarcodescanner.camera.CameraSourcePreview>

    <include
        layout="@layout/top_action_bar_in_live_camera"
        android:layout_width="match_parent"
        android:layout_height="wrap_content"
        android:layout_gravity="top"/>

</androidx.coordinatorlayout.widget.CoordinatorLayout>

For your reference : 
https://github.com/firebase/mlkit-material-android

  
