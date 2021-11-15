# Walkie Talkie/Push To Talk Android SDK for your Chat Apps
1. Need to add walkie talkie or push-to-talk functionality to your Android app?
2. Worry no more, you can add it quickly with VoicePing Android SDK that works with VoicePing Open Source Router.
3. Simple integration, customizable, and free! What are you waiting for? 🎉

VoicePing Walkie Talkie Android SDK works together with <span style="text-decoration:underline;"> VoicePing Open Source Router</span> to allow you to quickly add group voice broadcast capability to your app. The Android SDK comes with a reference Android App with UI that demonstrates the one button Push-To-Talk interface.  
  
  
## Features of VoicePing Walkie Talkie Push-to-Talk (PTT) Android SDK
1. Easy to integrate to your app; 5 lines of code is all it takes
2. Low data consumption suitable for Mobile Devices: Opus Codec, defined as 16Khz, 60ms Frame size. ~300KB per 1 minute of speech. 
3. Works over all network conditions (2G, 3G, 4G or Wifi) 
4. Auto-reconnect feature when Internet connection is lost
5. Uses WebSecure Socket for transport
6. Works for Android SDK (16 to 30) and Android OS version 4.1 to 11
7. Low battery consumption  
  
  
## Use Cases

1. A Uber like application can connect a group of drivers together based on their location or zipcode
2. For Enterprise applications like housekeeping applications, allow a group call to all housekeepers on a certain floor (level) of the hotel
3. For SOS apps, activate voice broadcast if a user is in distress
4. For Chat Apps, allow some users to send instant voice messages that do not need to be manually played. 

## Get Started
You can test our sample app here: [Google play download link]. The sample app is connected to group channel 1234 and allows you to test the Walkie Talkie function. 


## How simple is it to add VoicePing SDK to your app?

<center><a href="https://www.voicepingapp.com" target="_blank"><img alt="SDK in your app" src="https://i.ibb.co/jzbbcbx/Group-4-1.png" title="This is a sample how the SDK will look like in your app" /></a></center>


See those mic buttons?

Yup, that button is the only thing you need to add to your app to have PTT functionality.

But what if you don't want a mic button but another UI instead?

We have got it covered. You can customize it.


## Integrate walkie talkie sdk to your app

Build it with Android Studio and test on your device.

What you will need to integrate to your code is only 5 lines below.



1. Connect to the VoicePing server.
```
VoicePing.init(appContext, “VP_ROUTER_URL”, "COMPANY_NAME")
VoicePing.connect(“USER ID”, callback)
```



2. Now join the clients to the same channel (group), then they can talk to each other.
```
VoicePing.joinGroup(“GROUP_ID”, callback)
```



3. To start and stop the PTT (which you can then hook with user events like click and release or something else):
```
VoicePing.startTalking(context, “GROUP_ID”)
VoicePing.stopTalking(context)
```



## Customization

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

## VoicePing server URL

VoicePing Android SDK needs a VoicePing server to work. You can test with our hosted server or you can have your own self hosted server later. You can look at this repo (coming soon: open source Router URL) to know how to self-host the server.

The public server URL: `wss://router-lite.voiceping.net`


## Self-hosted server

If you need to self-hosted the server, you can find more documentation on the server repo: 
* [voiceover-server](https://github.com/SmartWalkieOrg/voiceover-server) (This is the repo server, uses VoicePing.js)
* [VoicePing.js](https://github.com/SmartWalkieOrg/VoicePing.js) (This is the library)

## Maintainers
* [VoicePing team](https://www.voicepingapp.com/)

## VoicePing Enterprise


VoicePing Enterprise is the full featured closed source version with support. More features available are [https://www.voicepingapp.com](https://www.voicepingapp.com). You can try VoicePing on:

* [VoicePing Web](https://web.voiceoverping.net/)
* [VoicePing Android](https://play.google.com/store/apps/details?id=com.media2359.voiceping.store)
* [VoicePing iOS](https://itunes.apple.com/us/app/voiceping/id1249953303?ls=1&mt=8)

Join the same public channel ID and try PTT from the web to the Android/iOS app and vice versa. You will find VoicePing has very clear audio and low latency<sup>1</sup>.

VoicePing Enterprise has more features than VoicePing Open Source which can be found here: https://www.voicepingapp.com/blog/design-a-stunning-blog


### Push To Talk

**Push To Talk (1-1):** Make private calls that no one else can hear.

**Push To Talk (Group):** Talk to a group of up to 500 users.


### Group Channels

**Multi Channel Scanning:** Active Channel is switched automatically when someone is talking.

**Mute Groups:** Silent Groups that you do not need to hear right now.

**Leave Groups:** Leave Groups to save on Battery.

**Dynamic Groups:** Add, remove or create new groups from Android or Web App.


### Unified Field Communication

**Texting:** Send text in VoicePing Mobile or VoicePing Web Texting or Desktop.

**Text to Speech:** Have text read out to you when you receive them. Supports Multiple Languages.

**API:** Send automated Text via API. Send Interactive Text with question and answers. Get location. Manage Groups and group members.

**Send Pictures:** Send HD pictures in VoicePing.

**Send Videos:** Send 720p Videos (Auto Compressed) in VoicePing.

**Auto Forward Pictures to Email:** Pictures can be auto forwarded to email for archival or re-sending.

**Voice/Video Calls:** Make Private Voice/Video Calls using VoIP.


### Headsets

**Wired Headset Support:** Hear and PTT via Wired Headset with PTT Toggle Mode Button.

**Bluetooth Headset Support:** Hear Incoming PTT. Best Paired with Bluetooth PTT Button.

**Bluetooth PTT Button Support:** Activates PTT without needing to touch phone


### Safety

**Priority Calls:** Override conversation to send urgent messages.

**SOS:** Gets everyone into the emergency channel quickly.

**Paging:** Urgent and constant alert to get someone's attention.

**Default SOS:** Quickly press PTT button five times to send a SOS to a pre-defined channel.


### Recordings

**Download Group Conversation:** Download as audio, text and picture files of the entire group conversation as company admin.

**Download Private Conversation:** Download as audio, text and picture files of the entire private conversation between any pair of users.


### Location

**Live Location Tracking:** See where everyone is now on a map

**View Historical Location:** See where one person has been

**Download Location Data:** Download the location data via Excel or API

**View Location in App:** Admins can view location of users in the Android or Web App


### Multi Platform Support

**[Android Supported](https://play.google.com/store/apps/details?id=com.media2359.voiceping.store):** Android 5 to Android 11 supported. With or Without Google Services.

**[iPhone Supported](https://itunes.apple.com/us/app/voiceping/id1249953303?ls=1&mt=8):** iPhone version available. Runs in Background to allow for Real Time receiving of PTT.

**[Desktop Version](https://www.voicepingapp.com/blog/voiceping-desktop-web-ptt):** Web Based version to connect office and field workers.


## Consulting/Partnership, Services & Pricing  

If you would like help on server setup, maintenance, customization, please reach out and we can help you on that. VoicePing Enterprise is also available for customisation, rebranding and source code purchase. 


## Footnote

[1] Latency: time between someone talks in a device until the other hears the audio on another device
