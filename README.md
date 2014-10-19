This projects will describe you how to add a smooth moving progress bar in your android application. You can use this progress bar in your web activities, or anywhere to show the loading process.

![sample-image] (https://github.com/nikoo28/buttery-progress-bar-android/blob/master/screenshot/device-2014-10-20-024211.png)

Import the file __ButteryProgressBar.java__ in your application project.

Edit the following values for a desired effect.

 ```java
mBarColor = c.getResources().getColor(android.R.color.holo_green_dark);
mSolidBarHeight = Math.round(DEFAULT_BAR_HEIGHT_DP * mDensity);
mSolidBarDetentWidth = Math.round(DEFAULT_DETENT_WIDTH_DP * mDensity);
 ```
 
Now move to your __MainActivity__ where you want to show the progress bar and add this code.

```java
// create new ProgressBar and style it
final ButteryProgressBar progressBar = new ButteryProgressBar(this);
progressBar.setLayoutParams(new LayoutParams(LayoutParams.MATCH_PARENT, 2500));

// retrieve the top view of our application
final FrameLayout decorView = (FrameLayout) getWindow().getDecorView();
decorView.addView(progressBar);

setContentView(R.layout.activity_main);
```

This is it. You will have a really smooth progress bar in your application. Just import the source code in eclipse and run the application on your device for a live demo.