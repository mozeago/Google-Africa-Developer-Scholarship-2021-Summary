### Google-Africa-Developer-Scholarship-2021-Summary  
#### Creating Accessibility-friendly Applications  
empasise by using colors, headers, icons. You can use `android:accessibilityHeading="true"` to mark a textView as a header for screen readers.  
Android uses TalkBack to help the visually impared to enhacne accessibility of apps  
TouchDelegate can as well be used to in screen readers  
android `Accessibility.View` class is also used to monitor in the background and listen when buttons arte clicked and items focused  
Use icons as much as possible for color blinded users  
for backgrounds with colors that may be problematic to users, we can wash the colors so that they are more of black or white or you may use outline on the text to make it stand more  
use contrast ratio of 4.5:1 for all text and 3:1 for large text  
Never use text as images, screen readers will never be able to read them  unless they are given description  
contrast can be improved more by making the background overlay darker to make the text stand out  
android apps can use the **Google_Accessibility_scanner** to check how best contrast has been applied  
#### Android Security: Effective Permission Handling  
##### Permission best practices
1. avoid unnecessary permissions  
2. Make permissions accesses explicit i.e **very clear** They should be detailed to void doubt or confussion  
3. Dont overwhel the user
4. Know the permissions required by users  
5. be transparent with user
6. use support libraries for backward compatibility
-always use `targetSdkVersion` version that is latest as possible  
#### The four permission protection levels are:
##### 1. Normal
##### 2. dangerous
##### 3. signature
##### 4. special permissions

##### 1. Normal  
for accessing device features, auto-granted at install and no user interaction is needed
##### 2. Dangeraous  
Require user consent and display a notification for user to approve. e.g camera,location
##### 3. signature  
Theses are custom permission defined by the developer
Two apps that share data and must have been signed with the same certificate e.g. from the same developer
they are auto-granted at install time and no user interaction is needed.
##### 4. Special  
They may change the entire user experience on the device e.g WRITE_SETTINGS which can be used to change settings.  
##### Best practices for permission request
1. Avoid unneccesary permissions---use intents where neccesary
2. Make permissions accesses explicit
3. Know permissions needed by your libraries---select libs that need minimum permissions
4. Dont overwhelm the user with permissions
5. Be transparent with the user---explain why the permission is needed, provide continuous indications when accessing mic or location to remind user about that
6. user suport libs for backward compatibility

Check the status of the permission before requesting for it  
Request for the permission when its really at the functionality it needs to be eg, after clicking camera icon or location icon or call icon  
-Explain a permission when where it is requested is not obvious e.g location in a chat application.  
-only explain permission if the user had denied the permission earlier on, use `ActivityCompat.shouldShowRequestPermissionRationale`  
##### Broadcast best practices
1. Use local broadcast manager whenever possible  
2. protect all broadcasts containing sensitive information  
3. Limit exposure to incomming broadcasts

#### Android Location-aware Apps with Kotlin  
##### Location APis
1. fused location provider
2. geofencing
3. Google maps platform: Maps
4. Google maps platform: Routes
5. Google maps platform: Places  

###### *Fused location provider uses all the (tower,wifi,gps)*  
it has accuracy options:
1. high
2. balanced
3. low power---celular
4. no power---relies on other apps  

*Google requires that we prominently disclose the use of background data*
1. Must be in the app
2. User must see the disclosure as part of their normal interaction with the app, dont burry it in menus or settings  
3. can not be only on the Terms of privacy
4. Can not be bundled with other disclosures
5. must be optional  

##### Data Requirements  
1. Must explain what is being collected
2. Explain what data is used for
3. How data is shared especially for advertising  

Use location emulator applications to simulate GPS apps and turn off wifi for accuracy.  
Navigation safe Args is used to pass variables between fragments  
For the paid google maps features/APIs, include as many data per request as possible to keeps costs down, cost is per request.  
For one to use the **speed limit API** they must have special asset-tracking license and you must confirm that the country does return the speed limit data as there are 20% + of countries in the world returning the speed limit data.  
#####Routs API considerations  
1. the request should always come from the server and not the android application.  

