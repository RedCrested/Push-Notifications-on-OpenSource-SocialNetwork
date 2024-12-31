# Push Notifications on OpenSource SocialNetwork

Using the OneSignal API, this component allows users to decide if they want to receive notifications on their computer or mobile device for interactions on their posts, friendship requests, or received messages after some time away from the site. The notifications are displayed in the default language of the user's device, with translations required.

The administrator can use the OneSignal Dashboard to send messages to all users who have accepted to receive notifications. The administrator can also set the following:

- The number of times a page is viewed/loaded on the screen before the notification prompt appears;
- The amount of time spent on a single page before the prompt appears;
- Whether the system will send notifications for received messages and the amount of time away;
- The customization of the appearance of the OneSignal bell.

Furthermore, notifications can be sent directly from OSSN to a custom Android app. For more details, refer to the [Push Notification Sample App](https://github.com/RedCrested/OSSN-Push-Notifications-Sample-App).

According to the OneSignal documentation, iOS apps are supported, though this functionality has not been tested yet.

**Request on desktop site**<br>
![](https://www.redcrested.net/solutions/ossn/components/OneSignalNotifications/OneSignalNotifications-1.png)

**Request on phone**<br>
![](https://www.redcrested.net/solutions/ossn/components/OneSignalNotifications/OneSignalNotifications-2.png)

**Notification bell**<br>
![](https://www.redcrested.net/solutions/ossn/components/OneSignalNotifications/OneSignalNotifications-4.png)

**Notification on desktop**<br>
![](https://www.redcrested.net/solutions/ossn/components/OneSignalNotifications/OneSignalNotifications-5.png)

**Notification on desktop**<br>
![](https://www.redcrested.net/solutions/ossn/components/OneSignalNotifications/OneSignalNotifications-6.png)


## OneSignal Configuration

To create the authorization ID in OneSignal, follow these steps:

1. Create an account at [OneSignal Dashboard](https://dashboard.onesignal.com/apps).
2. Click New App/Website, provide a name and, select "Web" as a first channel and proceed with Next.
3. Choose Custom Code, fill in the site name and URL, then save.
3. Ignore the downloaded SDK files or any additional code. The component includes all necessary files and code.
4. Copy the appId and safari_web_id values into the OSSN administration panel, then click Finish.

To obtain the API key, navigate to Keys & IDs under the settings menu. **Treat your API key as a password for security**.

Note: Using this component may incur additional costs. Refer to the [OneSignal pricing table](https://onesignal.com/pricing) for details.

## Limitations

The component was tested in free and premium version of OSSN 7.6, in GoBlue, Awesome and White themes. Maybe some adjustments are required in older versions and/or other themes. 

## Know issues

For the component to work on OSSN 6.1, it will be necessary to change line 129 of file components/OssnNotifications/classes/OssnNotifications.php. Otherwise, the callback doesn't be triggered.
 
 **Original code**
 ```php
    ossn_trigger_callback('notification', 'add', $callback);
```

**New code**
 ```php
    ossn_trigger_callback('notification', 'add', array(
                            'id'           => $this->getLastEntry(),
                            'instance'     => $this,
                            'notification' => $this->notification,
                        ));
```

## Versions
- 2.0
    - Added support for OneSignal API 11.6.
    - Updated admin layout options.
    - Enabled notification support for Android apps.
    - Introduced a Deeplink App Scheme field to open notifications in the app instead of the browser.
- 1.7
    - When clicking on the notification on the device, the page opens directly on the item. At the same time, the related notification in the notification panel of the OSSN site is marked as read.
    - At the messages page, the notification bell is hidden so that it does not overlap with the buttons on the bottom of the page.
- 1.6
    - Fixed an issue with messages at likes in comments.
    - Notification messages are shown in the user language if defined. Otherwise, it will be considered the default site language.
- 1.5
    - Fixed an issue with messages at likes in comments.
- 1.4
    - Fixed language issues with words with a single quote.
    - Fixed a bug in notification messages when a user has emojis in their name field.
- 1.3
    - Fixed language issues.
    - When clicking on the received message notification, the site opens directly in the conversation
    - Added persistent notification parameter. This parameter applies only to Chrome-based browsers on non-mobile devices. Details about this configuration in https://documentation.onesignal.com/docs/web-push-options#notification-persistence
    - Fixed an issue when this component is used on OSSN 6.1. Details in **Know Issues** section 
- 1.2
    - Added customized welcome message
    - Improved the German translation file. Courtesy of [Dominik Lieger](https://www.opensource-socialnetwork.org/u/Crossi)
- 1.1 
    - Fixed label Safari Web ID on admin form.
    - I changed the commercial name "OneSignal Notifications for OpenSource SocialNetwork" to "Push Notifications on OpenSource SocialNetwork"
- 1.0
    - Initial version

    
## Contributing

Send an email to [contact@redcrested.net](contact@redcrested.net).

## License

Go to [Red Crested License](http://www.redcrested.net/license) to read the last version of our terms.
