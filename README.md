# How to use

The Mobile SDK allows to program the Mini 3 Pro drone. It provides a library to access the drone hardware features. 

Pre-requisites:
> - MSDK version: 5.12.0
> - Remote controller for the drone: RC N1
> - Mobile device to run the android app

Take a look at [MSDK tutorial](https://developer.dji.com/doc/mobile-sdk-tutorial/en/quick-start/run-sample.html)

Steps:
> - Create a developer account: go to [Developer Center](https://account.dji.com/login?appId=dji_sdk&amp;backUrl=https%3A%2F%2Fdeveloper.dji.com%2Fuser&amp;locale=)
> - Generate an App Key 
> - Download the sample code: go to [Mobile sdk v5](https://github.com/dji-sdk/Mobile-SDK-Android-V5)
> - Create a project on Android Studio and import the package **android-sdk-v5-as** 
> - Past your App Key into **"gradle.properties"** file

Our code allows to sendo the drone forward using a button on the mobile device. After you have the sample code, you'll nedd to do some changes: 
> - Replace the **DJIMainActivity.kt** file located in the sample code, for the one located in the **src** folder. This file contains our custom buttons (_forward_, _takeoff_ and _land_).
> - Go to **res** folder and you'll find a **layout** folder: Replace the **layout.xml** file for the one located in the **src** folder. This file places the buttons on the main app screen.
> - Go to the **layout.xml** file and link the buttons to the functions: for each button, go to the attributes tab and link the respective function on the **onClick** attribute.
>> - _takeoff button_: **fun takeoffButton(view: View?)** 
>> - _land button_: **fun landButton(view: View?)**
>> - _forward button_:  **fun virtualStickForwardButton(view: View?)** 
> - For each button you'll need to add a string in the **strings.xml** file: Go to the **res** folder, you'll find a **values** folder. Replace the **strings.xml** file for the ond in the **src** folder. Also, you'll nedd to add a tag for each button with a chinese translation in the **strings.xml** located in the **values-zh-rCN** folder. 

To run: 
> - Syncronize and build the project
> - Generate the apk file for the application
> - Install the apk file into your mobile device
> - Connect the remote controller to the aircraft
> - Connect the mobile device to the remote controller
> - Run the app.
