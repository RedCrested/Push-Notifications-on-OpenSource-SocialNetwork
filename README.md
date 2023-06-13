# Push Notifications on OpenSource SocialNetwork

Using the OneSignal API, this component allows users to decide if they want to receive notifications on their computer or mobile device for interactions on their posts, friendship requests, or received messages after some time away from the site. The notifications are displayed in the default language of the user's device, with translations required.

The administrator can use the OneSignal Dashboard to send messages to all users who have accepted to receive notifications. The administrator can also set the following:

- The number of times a page is viewed/loaded on the screen before the notification prompt appears;
- The amount of time spent on a single page before the prompt appears;
- Whether the system will send notifications for received messages and the amount of time away;
- The customization of the appearance of the OneSignal bell.

To create the authorization ID in OneSignal, after create an account on that site, go to the https://dashboard.onesignal.com/apps, click on **new app/website**, then fill name and select web and click on **Next**. To finish the process, [follow this instructions](https://documentation.onesignal.com/v7.0/docs/web-push-custom-code-setup).

Note that using this component may incur additional costs. Please see the pricing table at https://onesignal.com/pricing for more information.


**Request on desktop site**<br>
![](https://www.redcrested.net/solutions/ossn/components/OneSignalNotifications/OneSignalNotifications-1.png)

**Request on phone**<br>
![](https://www.redcrested.net/solutions/ossn/components/OneSignalNotifications/OneSignalNotifications-2.png)

**Notification on desktop**<br>
![](https://www.redcrested.net/solutions/ossn/components/OneSignalNotifications/OneSignalNotifications-5.png)

**Notification on desktop**<br>
![](https://www.redcrested.net/solutions/ossn/components/OneSignalNotifications/OneSignalNotifications-6.png)


## How to buy
I am selling this component for US$39.00 through the Buy me a coffee website. To purchase, visit https://www.buymeacoffee.com/redcrested/e/117780 or click on the button 

[![](https://redcrested.net/res/img/button.png)](https://www.buymeacoffee.com/redcrested/e/117780)

## Limitations

The component was tested in free version of OSSN 6.4 and 6.6, in the GoBlue theme. Maybe some adjustments are required in older versions and/or other themes. 

## Version

- 1.6
    - Fixed an issue with messages at likes in comments
    - Notification messages are shown in the user language, if defined. Otherwise, it will be considered default site language.
- 1.5
    - Fixed an issue with messages at likes in comments
- 1.4
    - Fixed language issue with words with single quote
    - Fixed a bug in notification messages when user has emojis in their name field
- 1.3
    - Fixed languages issues
    - When clicking on the received message notification, the site opens directly in the conversation
    - Added persistent notification parameter. This parameter  apply only to Chrome based browsers on non-mobile devices. Details about this configuration in https://documentation.onesignal.com/docs/web-push-options#notification-persistence
    - Fixed an issue when this component is used on OSSN 6.1. Details in **Know Issues** section 
- 1.2
    - Added customized welcome message
    - Improved the German translation file. Courtesy of [Dominik Lieger](https://www.opensource-socialnetwork.org/u/Crossi)
- 1.1 
    - Fixed label Safari Web ID on admin form 
    - Changed commercial name "OneSignal Notifications for OpenSource SocialNetwork" to "Push Notifications on OpenSource SocialNetwork"
- 1.0
    - Initial version

    
## Contributing

Send email to [contact@redcrested.net](contact@redcrested.net).

## License

Go to [Red Crested License](http://www.redcrested.net/license) to read the last version of our terms.
