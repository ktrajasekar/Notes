### Add Images to Drawable

- Res -> Drawable and right click on the show in explorer then paste the images. 
- Now it ready to use it


``` android
      <ImageView
                android:id="@+id/close_activity"
                android:layout_width="wrap_content"
                android:layout_height="wrap_content"
                android:layout_alignParentRight="true"
                android:layout_gravity="center_vertical|center"
                android:layout_margin="50dp"
                android:padding="20dp"
                android:src="@drawable/login" />

```
Ref : https://stackoverflow.com/questions/29047902/how-to-add-an-image-to-the-drawable-folder-in-android-studio

### Linking to other page 

```
import android.content.Intent;

   public void nextPage(View view){
        Log.d(TAG, "testing ---------------------> ~~~~~~~~~~~~~~~~~~~~~~~~");
        Intent intent = new Intent(this, userChoice.class);
        startActivity(intent);
        Log.d(TAG, "End ---------------------> ~~~~~~~~~~~~~~~~~~~~~~~~");
    }
    
 ```
 ### Toast Notification

```
 Toast.makeText(getApplicationContext(), "Invalid Login Details",Toast.LENGTH_SHORT).show();
 
 ```
 ### Go Back Override 

```
@Override
public void onBackPressed(){
  Intent intent = new Intent(this, ActivityYouWanToGoBack.class);
  startActivity(intent);
}
```
