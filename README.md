# Google-Africa-Developer-Scholarship-2021-Summary  
### Creating Accessibility-friendly Applications  
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
### Android Security: Effective Permission Handling  
#####Permission best practices
1. avoid unnecessary permissions  
2. Make permissions accesses explicit i.e **very clear** They should be detailed to void doubt or confussion  
3. Dont overwhel the user
4. Know the permissions required by users  
5. be transparent with user
6. use support libraries for backward compatibility
-always use `targetSdkVersion` version that is latest as possible  
-
-




