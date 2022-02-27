# Day 1
## Main App Anatomy
- Basically your android project contains 
1. Kotlin files for the core logic of the app
2. A resources folder for static content such as images and strings 
3. AN android manifest file that defines essential app details so the OS can lunch your app
4. Gradle scripts, for building and running your app
## Build Dice Roller App
- We have to work on two different things to build and android app 
- these are the the activity file and the xml file related to that activity file
- The main activity file is an example of the activity file
- `What is activity ?` basically this is a core android class which is responsible for drawing an app user interface and receiving input events
- When your app launches,it launches a specific activity. This is the activity that was declared in the manifest with the correct intent filter tag Activities have a associated layout file,which in this case is activity_main.
- Layout files are XML files that express what the app actually looks like.They do this by defining things like text, images and buttons, and where these things will appear onscreen.
- These texts, images, and buttons are called Views.
- The activity of the layout are connected by a process known as layout inflation.
- This process is triggered when the activity starts.
- During layout inflation, the views defined in the XML layout files are turned or inflated into Kotlin view objects in memory.
- Once this happens, the activity can then draw these objects to the screen and also dynamically modify them.
- Source https://youtu.be/OIHnSKwxYiE
#### Find View By Id
- so basically we use this to interact with the views that we implement in the xml file 
- suppose we want to make an variable which is of type button that means there is a button in the xml file and we use this variable to interact with that button
- Then here, I need to add my id, so we're going to use the R class that I talked about before.
- So R.id., and then that id that I just created, which is roll_button.I want you to notice how roll_button appeared as part of the auto-complete. That's because the R class already knows about the id and is ready to link us to that view.
- Now that I have a reference to my button,I could actually use it.I can call methods on roll_button to dynamically modify how it behaves.Pretty much any attribute that exists in the XML I could modify here.
##### Steps
1. **Set button’s id in the activity_main.xml layout file:**
```xml
android:id="@+id/roll_button"
```
2. **Use findViewById to get a reference to the button and assign it to an immutable variable called rollButton:**
3. **(Optional) Dynamically modify the Button view:**
Set the button text to "Roll Button"
```xml
rollButton.text = "Let's Roll"
```
#### OnClickListner
- 