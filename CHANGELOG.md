## [0.6.21]
* Adds customSound feature for Android (only applicable for versions older than Android 8 (Oreo))
* Type parameter T removed from AwesomeAssertUtils to allows it to be compatible with Flutter web parser.
## [0.6.20]
* Adds rounded images for large icon and big picture
* Adds bool value extraction for Map objects in dart
* Fixes immutable error for input buttons in Android 12
* Network images for foreground services are temporarily disabled (https://github.com/rafaelsetragni/awesome_notifications/issues/369)
## [0.6.19]
* Adds sound extension for notifications with categories Alarm and Call
* Adds call notification behavior (stay floating on screen and keep playing the sound in loop) for Call category
* Adds CancellationManager to reorganize all dismiss and cancellation methods in a single place
* Created StatusBarManager to manage which notifications are currently active, improving performance and extending support to Android 5.0 Lollipop (SDK 21)
* Notification layouts BigPicture, Messaging and MessagingGroup improved to be more performative and to reuses network connection data
* Adds history box to notification's reply buttons on Android 8.0 to 12.0
* iOS swift completion handlers modified to allow display notifications from another plugins
## [0.6.18+2]
* Update readme file and PermissionManager to be compatible with Android 12 and Java 7
## [0.6.18+1]
* Java lambda expressions removed to turn Android source compatible with old Java 7
## [0.6.18]
* Adds Channel's Group feature for Android
* Adds notification's category feature for Android
* Adds fullScreenIntent permission and content option to allow to show notifications in full screen mode.
* Adds PreciseAlarms permission and schedule option to allow to show scheduled notifications with more precision.
* Adds showPage methods to provide shortcuts to channel permissions page and alarm permission page.
* Adds shouldShowRationale method for android to check if the requested permissions require user intervention to be enable.
* Adds request permissions methods to demand the users permissions considered dangerous by the system.
* Permission's request methods refactored to enable a more modular and scalable evolution to comport future permissions for Android
* Documentation has been improved with the new permissions methods, channel's group, notification categories, fullScreenIntent and PreciseAlarms permissions
## [0.6.17]
* Adds wakeUpScreen option in notification content to wake up screen when a notification is displayed (Requires to add WAKE_LOCK permission into AndroidManifest.xml).
* Adds custom permissions for method requestPermissionToSendNotifications (has no effect on Android).
* Documentation has been improved with wakeUpScreen option
## [0.6.16]
* Media button receiver removed from AndroidManifest.xml due incompatibility with some Galaxy models and another plugins (#81 and #320)
* Documentation on scheduling notifications has been improved
## [0.6.15]
* PushNotification class deprecated, as all push features are being moved to the new companion plugin. Instead, use NotificationModel.
* Adds isDangerousOption for action buttons, to color the text in red to indicate a dangerous option for the user.
* Adds color option for action buttons, to color the text in Android 8.0 Oreo and beyond (has no effect on iOS).
* Fixes for issue #321, when a new notification is erroneously created when the user taps on notification action button.
## [0.6.14]
* Adds validation to prevent scheduling with repeating intervals smaller than 60 seconds (iOS restriction)
* Adds crontab schedule to allow complex schedules based on initial and expiration date, a list of precise dates, or a crontab expression, and all four options can be combined together (only for Android)
* Defined the final standard to replace negative IDs by random values
* Minimum Android requirements increased to SDK 23 (Android 6.0 Marshmallow) due to new cancellation methods with unsecure procedures on API prior 23
## [0.6.13]
* Adds messaging layout and messaging group layout
* Adds method showNotificationPage to programmatically redirect the user to O.S. notifications permission page
* Minimum Android requirements increased to SDK 21 (Android 5.0 Lollipop) due to new cancellation methods
* Adds new cancellation methods (dismiss, cancel schedules and cancel all (dismiss and schedules at same time))) based on group key or channel key
* Property "autoCancel" changed to "autoDismissable", to match the new cancellation methods naming principles
* Adds internal group key based on ID, to prevent Android auto grouping with 4+ notification from same channel when group key was not specified
* Android channels refactored to keep the original channel key at maximum as possible, maximizing the compatibility with another plugins.
* Models refactored to follow the native standards and transformations from map data
* Calendar millisecond precision has been deprecated, due devices do not provide or ignore such precision.
* Adds error handling for image assets (iOS)
* Adds video tutorial into README file
* Version numbering has changed to better translate the stage of development for future releases.
## [0.0.6+12]
* Adds showInCompactView property for MediaPlayer buttons
* Adds support to multiple subscriptions on created, displayed, action and dismissed stream
* Removed channel key from Android Badge methods, because the segregation in channel keys was never used (now is all global)
* Adds increment and decrement badge methods (more performative)
## [0.0.6+11]
* Fix Android reschedules on startup process (issue #285)
* Improved Android channels to manage another package channels and convert then to the new standard, using channelKey as hashKey produced from digest channel content
## [0.0.6+10]
* Adds foreground services for Android
* Fixes android reference for guava package
## [0.0.6+9]
* Fixes null reference for main class inside NotificationBuilder.java
## [0.0.6+8]
* Fixes null reference for main class
## [0.0.6+7]
* Improves documentation
* Updates push notifications in the example app
## [0.0.6+6]
* Adds time zones for scheduled notifications
* Adds foreground behavior for input button
* Adds dismiss methods to dismiss the notifications without cancel their respective schedules
## [0.0.6+5]
* Adds behavior of bringing action buttons to foreground on iOS
* Adds debug option on initialize method to lower debug verbosity if not necessary
* Improves error messages and error handling for iOS and Android platforms
## [0.0.6+4]
* Adds native firebase handling for will present notification method
* Adds fixedDate to getNextDate on iOS
* Adds .aiff example files with more quality
* Adjust weekday to work with ISO 8601
## [0.0.6+3]
* Fixes Android canceling for a grouped notification set as summary behaviour
* Adds color hexadecimal representation for json content
## [0.0.6+2]
* Fixes Android first grouped message as summary behaviour.
## [0.0.6+1]
* Flutter version Fixes, according to pub.dev warnings
## [0.0.6]
* Plugin upgraded to support dart Null Safety
* FCM service native support removed for iOS and Android.
* iOS awesome extensions removed.
* Schedule feature downgraded due to iOS official developer's incapacity and SO limitations (could be reactivated manually).
* Adds an example to how to integrate awesome_notification with firebase_messaging plugin.
* Documentation improved
## [0.0.5+8]
* FCM service with comments removed for iOS.
## [0.0.5+7]
* Adds removeChannel method for iOS and error messages for Android removeChannel method.
* ios project and example project recovered.
## [0.0.5+6]
* Releasing of final version with push notifications enabled.
* Adds forceUpdate option on setChannel method, to allows to full update an channel on Android Oreo and above without need to reinstall the app, with the downside to close all current notifications.
* Flutter version updated to 3.0, with null safety support.
* Fixes privacy bugs
* Fixes grouping functionality and Adds sort option (sort only works for Android)
* Fixes media button errors for Android 10 and above
* Fixes media path errors for iOS
* Adds default sound options for Ringtone, Alarm and Notifications.
* Documentation improved
## [0.0.5+5]
* Adds the link to allows the community to remove or not the push notification functionality from Awesome Notifications plugin.
## [0.0.5+4]
* Adds the icon field inside notification content package to allow to change the small icon without need to use another channel
* Included the example for locked notifications for Android and improved the locked priority behaviour
* Adds importance level for notifications (Android 8 and above)
* Documentation improved
## [0.0.5+3]
* Internal firebase packages updated to the last Android and iOS version
* Fixes auto cancel off for schedule notifications (Android)
* Fixes action buttons for push notifications (iOS)
* Solution for DateUtils class conflict with the new Material "DateUtils" included on documentation
* Documentation improved
## [0.0.5+2]
* Included emojis to be used on local and push notifications
* Documentation improved
## [0.0.5+1]
* Included canceling capability to notification push service in cases of invalid notification
* iOS documentation improved
## [0.0.5]
* Finished FCM push messages for iOS 10 or higher
* Decreased the implementation complexity to use NotificationServiceExtension and NotificationContentExtension targets (iOS)
* Adds two app examples on documentation as tutorials
* Improved the native resource decoder to work outside of main thread (Android)
* Included protect mode to native resources against obfuscation (Android)
* Improved object storage to work correctly with minification
* Documentation on README file updated

## [0.0.4+4]
* Improved error messages for notifications disabled in Android Devices
## [0.0.4+3]
* Fixing bug found at Android channel checking process (https://github.com/rafaelsetragni/awesome_notifications/issues/28)
## [0.0.4+2]
* Cleared log messages to decrease visual pollution.
* Replaced the native Java Log package by the Flutter's one.
* Fixes wrong "Invalid push notification content", wrongly showed when notification is successfully created.
## [0.0.4+1]
* Simplifying the iOS setup process for the developer (it's still a bit complex)
## [0.0.4]
* Fixes complex schedules for iOS apps running on Foreground
* Included Global Badge indicators for iOS and some Android distributions
* Included request permission and check permission methods
* Included Firebase support to send push notifications on iOS (work in progress)

## [0.0.3+3]
* Fixes Shader's render problems on iOS devices
## [0.0.3+2]
* Fixes UTC Dates on iOS devices
## [0.0.3+1]
* Adjusting the plugin content to pub.dev patterns
## [0.0.3]
* Documentation updated
* Included DismissedStream to capture dismissed notifications by the user
* Included iOS notification source code to enable send local notifications on iOS devices (still in development)
* Updated asset's load file method inside the java native code, due to flutter's 1.22 deprecation on "FlutterLoader.getInstance()"
* Extracted Bitmap class from bitmap package, due to buildGradle incompatibilities while running the project on release mode (Java)

## [0.0.2+2]
## [0.0.2+1]
* Documentation updated
## [0.0.2]
* Adds precise schedules option to schedule a notification multiple times with precisely date and time

## [0.0.1+7]
## [0.0.1+6]
## [0.0.1+5]
* Documenting the code

## [0.0.1+4]
## [0.0.1+3]
## [0.0.1+2]
## [0.0.1+1]
* Adjusting the plugin content to pub.dev patterns

## [0.0.1]
* Initial release.