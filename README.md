# **Walkie Talkie/Push To Talk Android SDK for your Chat Apps **



1. Need to add walkie talkie or push-to-talk functionality to your Android app?
2. Worry no more, you can add it quickly with VoicePing Android SDK that works with VoicePing Open Source Router.
3. Simple integration, customizable, and free! What are you waiting for? 🎉

VoicePing Walkie Talkie Android SDK works together with<span style="text-decoration:underline;"> VoicePing Open Source Router</span> to allow you to quickly add group voice broadcast capability to your app. The Android SDK comes with a reference Android App with UI that demonstrates the one button Push-To-Talk interface.


## **Features of VoicePing Walkie Talkie Push-to-Talk (PTT) Android SDK **



1. Easy to integrate to your app; 5 lines of code is all it takes
2. Low data consumption suitable for Mobile Devices: Opus Codec, defined as 16Khz, 60ms Frame size. ~300KB per 1 minute of speech. 
3. Works over all network conditions (2G, 3G, 4G or Wifi) 
4. Auto-reconnect feature when Internet connection is lost
5. Uses WebSecure Socket for transport
6. Works for Android SDK (16 to 30) and Android OS version 4.1 to 11
7. Low battery consumption

## 
**Use Cases**

1. A Uber like application can connect a group of drivers together based on their location or zipcode
2. For Enterprise applications like housekeeping applications, allow a group call to all housekeepers on a certain floor (level) of the hotel
3. For SOS apps, activate voice broadcast if a user is in distress
4. For Chat Apps, allow some users to send instant voice messages that do not need to be manually played. 

## 
**Get Started**


You can test our sample app here: [Google play download link]. The sample app is connected to group channel 1234 and allows you to test the Walkie Talkie function. 


## 
**How simple is it to add VoicePing SDK to your app?**



<p id="gdcalert1" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: inline image link here (to images/image1.png). Store image on your image server and adjust path/filename/extension if necessary. </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert2">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


![alt_text](images/image1.png "image_tooltip")


See those mic buttons?

Yup, that button is the only thing you need to add to your app to have PTT functionality.

But what if you don't want a mic button but another UI instead?

We have got it covered. You can customize it.


## 
**Integrate walkie talkie sdk to your app**

Build it with Android Studio and test on your device.

What you will need to integrate to your code is only 5 lines below.



1. Connect to the VoicePing server.


```
VoicePing.init(appContext, "VP_ROUTER_URL", "COMPANY_NAME")
VoicePing.connect("USER ID", callback)

```



2. Now join the clients to the same channel (group), then they can talk to each other.


```
VoicePing.joinGroup("GROUP_ID", callback)

```



3. To start and stop the PTT (which you can then hook with user events like click and release or something else):


```
VoicePing.startTalking(context, "GROUP_ID")
VoicePing.stopTalking(context)
```



## 
**Customization**

You can customize the size, color, of the mic button.

You can also customize the shape of the mic button. Or you can have your own PTT button.


```
<com.smartwalkie.voicepingsdk.VoicePingButton
    android:layout_width="wrap_content"
    android:layout_height="wrap_content"
    app:shape="..." (oval / rectangle)
    app:radius="..."
    app:backgroundColor="..."
    app:micColor="..."
    />
```



## 
**VoicePing server URL**

VoicePing Android SDK needs a VoicePing server to work. You can test with our hosted server or you can have your own self hosted server later. You can look at this repo (coming soon: open source Router URL) to know how to self-host the server.

The public server URL: `wss://router-lite.voiceping.net`


## 
**Self-hosted server**

If you need to self-hosted the server, you can find more documentation on the server repo: [voiceover-server](https://github.com/SmartWalkieOrg/voiceover-server)



* (This is the repo server, uses VoicePing.js)
* [VoicePing.js](https://github.com/SmartWalkieOrg/VoicePing.js) (This is the library)

## 
**Maintainers**

* [VoicePing team](https://www.voicepingapp.com/)

## 
VoicePing Enterprise


VoicePing Enterprise is the full featured closed source version with support. More features available are [https://www.voicepingapp.com](https://www.voicepingapp.com). You can try VoicePing on:

* [VoicePing Web](https://web.voiceoverping.net/)
* [VoicePing Android](https://play.google.com/store/apps/details?id=com.media2359.voiceping.store)
* [VoicePing ](https://play.google.com/store/apps/details?id=com.media2359.voiceping.store)iOS

Join the same public channel ID and try PTT from the web to the Android app and vice versa. You will find VoicePing has very clear audio and low latency.

VoicePing Enterprise has more features than VoicePing Open Source which can be found here: https://www.voicepingapp.com/blog/design-a-stunning-blog


### **Push To Talk**

**Push To Talk (1-1):** Make private calls that no one else can hear.

**Push To Talk (Group):** Talk to a group of up to 500 users.


### **Group Channels**

**Multi Channel Scanning:** Active Channel is switched automatically when someone is talking.

**Mute Groups:** Silent Groups that you do not need to hear right now.

**Leave Groups:** Leave Groups to save on Battery.

**Dynamic Groups:** Add, remove or create new groups from Android or Web App.


### **Unified Field Communication**

**Texting:** Send text in VoicePing Mobile or VoicePing Web Texting or Desktop.

**Text to Speech:** Have text read out to you when you receive them. Supports Multiple Languages.

**API:** Send automated Text via API. Send Interactive Text with question and answers. Get location. Manage Groups and group members.

**Send Pictures:** Send HD pictures in VoicePing.

**Send Videos:** Send 720p Videos (Auto Compressed) in VoicePing.

**Auto Forward Pictures to Email:** Pictures can be auto forwarded to email for archival or re-sending.

**Voice/Video Calls:** Make Private Voice/Video Calls using VoIP.


### **Headsets**

**Wired Headset Support: **Hear and PTT via Wired Headset with PTT Toggle Mode Button.

**Bluetooth Headset Support:** Hear Incoming PTT. Best Paired with Bluetooth PTT Button.

**Bluetooth PTT Button Support:** Activates PTT without needing to touch phone


### **Safety**

**Priority Calls:** Override conversation to send urgent messages.

**SOS:** Gets everyone into the emergency channel quickly.

**Paging:** Urgent and constant alert to get someone's attention.

**Default SOS:** Quickly press PTT button five times to send a SOS to a pre-defined channel.


### **Recordings**

**Download Group Conversation:** Download as audio, text and picture files of the entire group conversation as company admin.

**Download Private Conversation:** Download as audio, text and picture files of the entire private conversation between any pair of users.


### **Location**

**Live Location Tracking:** See where everyone is now on a map

**View Historical Location:** See where one person has been

**Download Location Data:** Download the location data via Excel or API

**View Location in App:** Admins can view location of users in the Android or Web App


### **Multi Platform Support**

**[Android Supported](https://play.google.com/store/apps/details?id=com.media2359.voiceping.store):** Android 5 to Android 11 supported. With or Without Google Services.

**[iPhone Supported](https://itunes.apple.com/us/app/voiceping/id1249953303?ls=1&mt=8):** iPhone version available. Runs in Background to allow for Real Time receiving of PTT.

**[Desktop Version](https://www.voicepingapp.com/blog/voiceping-desktop-web-ptt):** Web Based version to connect office and field workers.


## 
Consulting/Partnership, Services & Pricing  

If you would like help on server setup, maintenance, customization, please reach out and we can help you on that. VoicePing Enterprise is also available for customisation, rebranding and source code purchase. 


## 
**Footnote**

[1] time between someone talks in a device until the other hears the audio on another device




# **Server Repo readme**


## **VoicePing Router Server**

This is a router server for the android VoicePing SDK ([https://github.com/smartwalkie/Walkie-talkie-android-by-voiceping](https://github.com/smartwalkie/Walkie-talkie-android-by-voiceping)). This server uses native websocket technology. This server uses multithreading to handle concurrent requests for better performance.

This server needs Redis as database and needs NodeJS exact version 6.

This repo handles the multithreading process. For the core functionality, it’s handled in [VoicePing.js](https://github.com/SmartWalkieOrg/VoicePing.js) library (which will automatically be included when installing this repo).


## **Build Status**



* master: 

<p id="gdcalert2" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: error handling inline image </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert3">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>


* develop: 

<p id="gdcalert3" ><span style="color: red; font-weight: bold">>>>>>  gd2md-html alert: error handling inline image </span><br>(<a href="#">Back to top</a>)(<a href="#gdcalert4">Next alert</a>)<br><span style="color: red; font-weight: bold">>>>>> </span></p>



VoiceOver push-to-talk server


## 
**Setup**

Install dependencies with `npm` and start


```
$ npm install
```


Start development server with `gulp`. It will automatically watch file changes, lint it and restart the server.


```
$ gulp develop
```


Alternatively, use `nodemon`


```
$ nodemon ./app.js
```


Check out the `gulpfile.js` for the supported build or automation tasks. Also learn more about [gulp](http://gulpjs.com/).


## 
**Test**

Run test with npm, Makefile or gulp


```
$ npm test

$ make test

$ gulp test
```



## 
**Changelog**

[Changelog](https://github.com/SmartWalkieOrg/voiceover-server/blob/master/CHANGELOG.md) is updated on each deployment to the production environment. The process is as follows:



1. Update the package.json `version`.
2. Run `gulp changelog`, which will find the new commits since previous tagged commit.
3. `git tag &lt;new vesion>`, then push the tags to origin master.

To generate changelog from commits, we followed [conventional-changelog](https://www.npmjs.com/package/conventional-changelog), which is based on AngularJS commit conventions. This is not that different compared to `grunt-conventional-changelog`, they are just part of gulp tasks instead of grunt tasks.


## 
**Deployment**

Server is currently deployed with [dokku](http://progrium.viewdocs.io/dokku)


## 
**User Authentication / Authorization**

Users are authenticated with OAuth to [VoicePing web server](https://github.com/2359media/voiceping-sails).

The following are the steps required for users to connect to the websocket server and to join the live conversation channels.



1. [Get access token](https://github.com/2359media/voiceping-sails/tree/master#get-access-token) from the web server, and connect to `socket_url` provided in the JSON response via websocket.
2. The user will need to authenticate to the websocket server for live conversation. To do this, from the user's JSON structure, set the `uuid` as the value of `token` HTTP header field as part of the websocket connection request headers.
3. Once a websocket connection is opened, the user will be able to send push-to-talk events to one of the channels returned from `/api/v2/channels` of the web server.
4. Alternatively, a private message could be sent to one of the user being returned from `/api/v2/users`.
5. Use channel's `{ id: ... }` or user's `{ id: ... }` for private message as usual, and set the ids as part of the voice packet or text message being sent for push-to-talk events.

### 
**References**

1. [WebSocket Security: Authentication/authorization](https://devcenter.heroku.com/articles/websocket-security#authentication-authorization).
2. [Websocket 101: Authorization and IPs](http://lucumr.pocoo.org/2012/9/24/websockets-101/)

## 
**Messaging**


Push-to-Talk event message is formatted with [msgpack](http://msgpack.org/) with the following rough structure:


```
|channel_type|message_type|from_id|to_id_or_channel_id|payload|
```


The following channel types are understood by the message router:


```
0: group
1: private
```


The following message types are understood by the message router:


```
1: start_talking
2: stop_talking
3: audio
4: connection
5: status
6: ack_start (only sent from the server side)
7: ack_stop (only sent from the server side)
8: ack_start_failed (only sent from the server side)
9: duplicate_login (only sent from the server side)
10: user_update (only sent from the server side)
11: user_delete (only sent from the server side)
12: channel_update (only sent from the server side)
13: channel_delete (only sent from the server side)
14: trial_expired (only sent from the server side)
15: channel_add_user (internal usage on the server side)
16: channel_remove_user (internal usage on the server side)
17: text
18: image
19: offline_message
20: delivered_message
21: read_message
22: ack_text (only sent from the server side)
```


Where `channel_type`, `message_type`, `from_id`, `to_id_or_channel_id` are integers, and `payload` is a binary data for voice data or a string. Message of type `0` will be ignored.

On connection, the message router needs to identify the connected websockets and which user they belong to. To do this, client sends a user status message with this format:


```
|0|4|from_id|to_id_or_channel_id|optional_device_token|
```


Where `0` is a channel of type `group`, and `4` is a message of type `connection`, and `to_id_or_channel_id` will be ignored in this case. The trailing buffer `optional_device_token` is an optional device token string which is required for iOS, but optional for others such as android.

`connection` message is also being used to retrieve private offline messages for the connected user. group offline message is retrieved separately via HTTP API `/api/v2/channels/2/messages`, documented on the Postman Collection of [voiceping-sails API](https://github.com/2359media/voiceping-sails/blob/master/VoicePing-APIv2.json).

To send a message to a specific user, please send a message with this format:


```
|1|message_type|from_id|to_id|message_or_buffer|
```


Where `1` is a channel of type `private`. `message_type` follows the same values as `group` channel type. This has the same functionality as other message types, but to a specific user.

`user_update` and `channel_update` are used to notify channels and users update from the database. Clients need to refresh / update their channels and contacts from `users` or `channels` API.



* Dashboard to Router (still around)
* Router to clients (retired as causing too many API calls)

`duplicate_login` is used to notify if a new login is done on another device. Then the previous logged-in device should be logged out by the client.

`trial_expired` is used to notify if a user has exceed the trial period. (not in use)


## 
**Read and Delivered Message**

More details on [message identification](https://github.com/SmartWalkieOrg/voiceover-server/blob/master/docs/message_identification.md).


## 
**User status**

Feature not in use at the moment as hard to make reliable without consuming a lot of client battery. More details on [user status](https://github.com/SmartWalkieOrg/voiceover-server/blob/master/docs/user_status.md).


## 
**Keep Alive mechanism**

Every 5 minutes the server will ping connected sockets for inactivity (a keep alive mechanism). This is being used to as one of the ways to keep the iOS device aware of the websocket server, so it could wake up from a suspended state. This might not be required with PubNub implementation.

At the moment, it's expected that the clients support WebSocket protocol versions 5 and above. For more details on ping pong implementation on websocket protocol read chapter 5.5.2 and 5.5.3 of [http://tools.ietf.org/html/rfc6455](http://tools.ietf.org/html/rfc6455)
