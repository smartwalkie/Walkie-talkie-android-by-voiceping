# VoicePing Android SDK

<br />  
<center><a href="https://www.voicepingapp.com" target="_blank"><img alt="VoicePing SDK Banner" src="https://i.ibb.co/9pKKf4J/Group-2.png" title="VoicePing SDK Banner" /></a></center>
<br /><br />

## Walkie Talkie/Push To Talk Android SDK for your Chat Apps

1. Need to add walkie talkie or push-to-talk functionality to your Android app?
2. Worry no more, you can add it quickly with VoicePing Android SDK that works with VoicePing Open Source Router.
3. Simple integration, customizable, and free! What are you waiting for? 🎉

VoicePing Android SDK works together with <span style="text-decoration:underline;"> VoicePing Open Source Router</span> to allow you to quickly add group voice broadcast capability to your app. The Android SDK comes with a reference Android App with UI that demonstrates the one button Push-To-Talk interface.  
  
  
## Features of VoicePing Android SDK

1. Easy to integrate to your app
2. Low data consumption suitable for Mobile Devices: Opus Codec, defined as 16Khz, 60ms Frame size. ~300KB per 1 minute of speech. 
3. Works over all network conditions (2G, 3G, 4G or Wifi) 
4. Auto-reconnect feature when Internet connection is lost
5. Uses secure WebSocket for transport
6. Works for Android SDK (16 to 30) and Android OS version 4.1 to 11
7. Low battery consumption  
  
  
## Use Cases

1. A Uber like application can connect a group of drivers together based on their location or zipcode
2. For Enterprise applications like housekeeping applications, allow a group call to all housekeepers on a certain floor (level) of the hotel
3. For SOS apps, activate voice broadcast if a user is in distress
4. For Chat Apps, allow some users to send instant voice messages that do not need to be manually played. 

## Get Started
You can test our sample app here: [Google play download link].  
The sample app allows you to test the Walkie Talkie function.  
Input any user ID and company name. Devices should have same company name to be able to communicate, but different user ID.


## How simple is it to add VoicePing SDK to your app?

<center><a href="https://www.voicepingapp.com" target="_blank"><img alt="SDK in your app" src="https://i.ibb.co/jzbbcbx/Group-4-1.png" title="This is a sample how the SDK will look like in your app" /></a></center>

See those mic buttons?

Yup, that button is the only thing you need to add to your app to have PTT functionality.

But what if you don't want a mic button but another UI instead?

We have got it covered. You can customize it.


## How to use VoicePing Android SDK

1. Initialize

Initialize VoicePing in your Application code, inside onCreate method

```kotlin
class VoicePingClientApp : Application() {
    override fun onCreate() {
        super.onCreate()
        VoicePing.init(this, "voiceping_sdk_server_url")
    }
}
```
  
  
2. Connect

Before you can start talking, you need connect to server. You can do that by call connect
method from VoicePing instance.

```kotlin
VoicePing.connect("your_user_id", "your_company", object : ConnectCallback {
    override fun onConnected() {
        // Do something
    }

    override fun onFailed(exception: VoicePingException) {
        // Do something
    }
})
```
  
  
3. Start Talking

After successfully connected, you can now start talking. You can start talking to individual
receiver using:

```kotlin
VoicePing.startTalking("receiver_id", ChannelType.PRIVATE, this)
```

or in a group using:

```kotlin
VoicePing.startTalking("group_id", ChannelType.GROUP, this)
```  
Before you can talk in a group, you need to join a group first, please look at item 6 below.
  
  
4. Stop Talking

To stop talking, for both Private and Group PTT:

```kotlin
VoicePing.stopTalking()
```
  
  
5. Disconnect

You can disconnect to stop receiving PTT:  

```kotlin
VoicePing.disconnect(object : DisconnectCallback {
    override fun onDisconnected() {
        // Do something
    }
})
```
  
  
6. Join a group

You cannot listen to a group channel before joining it. To join a group channel:

```kotlin
VoicePing.joinGroup("group_id")
```
  
  
7. Leave a group

To leave a group channel:

```kotlin
VoicePing.leaveGroup("group_id")
```
  
  
8. Mute specific channel

To mute specific channel:

```kotlin
VoicePing.mute("target_id", ChannelType.PRIVATE)
// or ChannelType.GROUP if you want to target group
```
  
  
9. Unmute specific channel

To unmute specific channel:

```kotlin
VoicePing.unmute("target_id", ChannelType.PRIVATE)
// or ChannelType.GROUP if you want to target group
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

VoicePing Android SDK needs a VoicePing server to work. You can test with our hosted server or you can have your own self hosted server later. You can look [at this repo](https://github.com/SmartWalkieOrg/walkie-talkie-server) to know how to self-host the server.

The public server URL: `wss://router-lite.voiceping.info`


## Self-hosted server

If you need to self-host the server, you can find more documentation on the server repo: 
* [voiceover-server](https://github.com/SmartWalkieOrg/voiceover-server) (This is the repo server, uses VoicePing.js)
* [VoicePing.js](https://github.com/SmartWalkieOrg/VoicePing.js) (This is the library)


## Maintainers

* [VoicePing team](https://www.voicepingapp.com/)


## VoicePing Enterprise

VoicePing Enterprise is the full featured closed source version with support. More features available are [https://www.voicepingapp.com](https://www.voicepingapp.com). You can try VoicePing on:

* [VoicePing Web](https://web.voiceoverping.net/)
* [VoicePing Android](https://play.google.com/store/apps/details?id=com.media2359.voiceping.store)
* [VoicePing iOS](https://itunes.apple.com/us/app/voiceping/id1249953303?ls=1&mt=8)

Join the same free channel ID and try PTT from the web to the Android/iOS app and vice versa. You will find VoicePing has very clear audio and low latency<sup>1</sup>.

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
