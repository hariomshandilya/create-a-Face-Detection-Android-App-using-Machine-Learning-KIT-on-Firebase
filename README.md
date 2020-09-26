# create-a-Face-Detection-Android-App-using-Machine-Learning-KIT-on-Firebase
Firebase ML KIT aims to make machine learning more accessible, by providing a range of pre-trained models that can use in the iOS and Android apps. Let’s use ML Kit’s Face Detection API which will identify faces in photos. By the end of this article, we’ll have an app that can identify faces in an image, and then display information about these faces, such as whether the person is smiling, or has their eyes closed with wonderful GUI.
Step 1: Create a New Project

Open a new project in android studio with whatever name you want.
We are gonna work with empty activity for the particular project.
The minimum SDK required for this particular project is 23, so choose any API of 23 or above.
The language used for this project would be JAVA.
Leave all the options other than those mentioned above, untouched.
Click on FINISH.
Login or signup on Firebase.
In Firebase console, create a new project or if you wanna work with an existing project then open that.
Name the project as per your choice.
Go to Docs.
Click on Firebase ML, and in the left space, choose ‘recognize text‘ under Vision.
Go through the steps mentioned for better understanding.
Come back to Android Studio.
Go to Tools -> Firebase -> Analytics -> Connect with Firebase -> Choose your project from the dialog box appeared -> Click Connect. (This step connects your android app to the Firebase)
Step 3: Custom Assets and Gradle

For enhancing the GUI either choose an image of .png format and add it in the res folder and set it as the background of main .xml file, or  set a background color by going to the design view of the layout and customizing background under Declared Attributes
To, include the ML KIT dependencies, in the app, go to Gradle Script -> build.gradle(Module:app) and add an implementation mentioned below:
implementation ‘com.google.firebase:firebase-ml-vision:17.0.0’

Now copy the below-mentioned text, and paste it at the very end of the app level Gradle, outside all the brackets as shown in the image below.
apply plugin: ‘com.google.gms.google-services’
Next, go to bulid.gradle (project) and copy the below-mentioned text, and paste it in ‘dependencies’ classpath as shown in the image below.
classpath ‘com.google.gms:google-services:4.2.0’
<?xml version="1.0" encoding="UTF-8"?> 
<androidx.constraintlayout.widget.ConstraintLayout
    tools:context=".MainActivity"
    android:layout_height="match_parent"
    android:layout_width="match_parent"
xmlns:tools="http://schemas.android.com/tools"
    xmlns:app="http://schemas.android.com/apk/res-auto"
    xmlns:android="http://schemas.android.com/apk/res/android"> 
  
 <Button
        android:background="#000000"
        android:layout_height="wrap_content"
        android:layout_width="wrap_content"
        app:layout_constraintStart_toStartOf="parent"
        app:layout_constraintEnd_toEndOf="parent"
        app:layout_constraintBottom_toBottomOf="parent"
 android:text=CAMERA
        android:layout_marginBottom="100dp"
        android:padding="16dp"
        android:id="@+id/camera_button"/> 
</androidx.constraintlayout.widget.ConstraintLayout>
