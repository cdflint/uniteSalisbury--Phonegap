## PhoneGap wrapper for node.js app
---
Download qr-code:
![alt text](https://github.com/cdflint/uniteSalisbury--Phonegap/blob/master/platforms/Download_Link_Dev.png "Download link")

---
first time only

```npm install -g cordova```

or

```sudo npm install -g cordova```

#### Setup process from CLI
{} = optional args

```
cordova create app-name {reverse.domain} {apps display text}
cordova create uniteSalisbury org/whatsup/index.esrgc.apps UniteSalisbury

cordova platform add ios
cordova platform add android

cordova platform ls

cordova build
```

or

```
cordova build ios
cordova build android
```

### for InAppBrowser

```
cordova plugin add https://git-wip-us.apache.org/repos/asf/cordova-plugin-inappbrowser.git
```

### setup in config.xml's
./config.xml

```xml
<plugin name="cordova-plugin-inappbrowser" />
```

./platforms/android/res/xml/config.xml

```xml
<feature name="InAppBrowser">
    <param name="android-package" value="org.apache.cordova.inappbrowser.InAppBrowser" />
</feature>
```

./platforms/ios/UniteSalisbury/config.xml

```xml
<feature name="InAppBrowser">
    <param name="ios-package" value="CDVInAppBrowser" />
</feature>
```

check setup with

```
cordova prepare
```

for plaforms iOS and Android set target='_blank'
for browser set target="_self" so a new window event is not triggered

### uri Whitelisting
./config.xml

```xml
<access origin="http://apps.esrgc.org/uniteSalisbury" />
<access origin="http://*.tiles.mapbox.com/*"
```

will allow access to /uniteSalisbury*
and mapbox tiles for mapbox

### Apple iOS App Transport Security (ATS) solution

On mac modify app-name.info.plist
add the following to the record for mapbox
```xml
<key>NSThirdPartyExceptionAllowsInsecureHTTPLoads</key>
<true/>
```
