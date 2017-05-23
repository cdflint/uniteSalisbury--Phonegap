#Todo List
---

<!-- for transmission back and forth to mac

tar --exclude='node_modules/*' --exclude='*.tar.bz2' -cvjf backup-vX.X.X.tar.bz2 .
 -->

## todo's for Apple deployment

[Apple deployment checklist `human-readable`](https://code.tutsplus.com/tutorials/how-to-submit-an-ios-app-to-the-app-store--mobile-16812)

[Apple App Store Review Guidelines `are you ready?`](https://developer.apple.com/app-store/review/guidelines/)

#### on the Mac
- [x] Install Xcode if not already     xcode-select --install

- [x] Deployment Tools                 npm i -g ios-deploy

#### Prerequisites
- [x] AppID

- [x] Distribution Certificate

    - [x] Development Certificate

    - [x] Production Certificate

- [x] Provisioning Profile for development

- [x] Test devices

        Need to connect to the Mac via USB
        and allow those devices to be added to the development
        Provisioning Profile for production

        Beta testing in Test flight

- [x] Provisioning Profile for production/distribution

- [x] Build Settings

    - [x] Need to update URL from whatsup to uniteSalisbury

    - [x] [Need to properly define ATS exceptions for mapbox ](https://developer.apple.com/library/content/documentation/General/Reference/InfoPlistKeyReference/Articles/CocoaKeys.html#//apple_ref/doc/uid/TP40009251-SW33)

- [x] Deployment Target


#### Assets

- [x] Icons

    `Note: may include alpha channel should not have transparent portion`

        Required

            iTunes Artwork: 1024px x 1024px
            iPad/iPad mini: 72px x 72 px & 114px x 114px
            iPhone/iPod Touch: 57px x 57px & 114px x 114px

        Optional

            Search Icon: 29px x 29px & 58px x 58px
            Settings Appkication: 50px x 50px & 100px x 100px

- [ ] Screenshots

    Minimum 1 Max 5
    Separate screenshots for

    - [ ] iPhone/iPod Touch
    - [x] iPad/iPad mini

        These screenshots will be used in the app store

        should consider adding temporary events/data to map for screenshots

- [ ] Metadata [apple's guide to metadata](https://developer.apple.com/app-store/product-page/)
  , [category outline](https://developer.apple.com/app-store/categories), [viewing and changing metadata](https://developer.apple.com/library/content/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Chapters/ChangingAppMetadata.html#//apple_ref/doc/uid/TP40011225-CH3-SW1)

  `Once app status is set to Ready for Sale certain metadata and assets are no longer editable without resubmitting the application`

        1. Applications name
              UniteSalisbury

        2. Version/(build) number
              v1.1 (12)

        3. Primary (and an optional secondary) Category
              Primary Category: Social Networking
              Secondary Category: ??????

        4. Concise description
              Unite Salisbury is a simple way to find and manage events in the Salisbury Maryland
              area.  The application features a map view and calendar view, allowing users
              multiple ways to find events happening near them and on specific days and times.  
              Event hosts can easily create, edit, and manage events.

        5. Keywords for search in app store (max 100 characters comma separated spaces count...)
              Salisbury,event,event hosting,Salisbury MD,whatsup,unitesalisbury,unite salisbury

        6. Support URL (so people that need help with application can contact us...)
              www.ESRGC.org

        7. Since there is a login function we need to provide Apple with a test/demo account for review process (so they dont have to create an account for the app... they are lazy)
              UserName: xxxxxx
              password: xxxxxx

#### Submission [submit app to app review](https://developer.apple.com/library/content/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Chapters/SubmittingTheApp.html) [iTunes Connect](https://itunesconnect.apple.com)

Double check info prior to app Submission

- [ ] Basic Info

  - [ ] Verify App properties prior to submitting for review

      - [ ] App Store text and images

      - [ ] Categories

      - [ ] Keywords

      - [ ] Rating

      - [ ] Optional app previews

      `validate the following properties that will cause app rejection if iTunes Connect information doesn't match`

      - [x] Bundle ID

      - [x] Version Number (the app store version number)

      - [ ] App Sandbox information


  - [ ] Final questions pre-submit

      - [x] Minimum OS Version supported

      iOS 8

      - [x] Export Compliance `contains no encryption regulated by the U.S. BIS`

      - [x] Content Rights

      - [x] Advertising Identifier (IDFA) `no ADs`

  - [ ] Explain ATS exceptions

        If asked why the oxford server is not setup for https when apple is reviewing application will need to explain.

- [x] Price & Availability

        $Free and default

- [ ] Metadata

- [x] Ready to Upload Binary

#### Upload to the Store
- [x] must use an apple device to create the archive for upload

#### Wait...
- [ ] Waiting for review process to complete

---
## todo's for Android deployment

[Android deployment checklist](https://developer.android.com/distribute/best-practices/launch/launch-checklist.html)

#### Prerequisites
- [x] Valid Google Play Store developer account [android developer](https://play.google.com/apps/publish/signup/)

- [x] Build a release-ready APK

  - [x] Need to update target URL from whatsup to uniteSalisbury

  - [x] Test on bluestacks emulator

  - [x] Test on live device

#### Assets
- [ ] Plan for app's Play store listing (Metadata)

  - [x] Icon

  - [x] Feature image

  - [ ] Screenshots

          should consider adding temporary events/data to map for screenshots

          screenshots for tablet
            7-inch
            10-inch

  - [ ] Description

          See iPhone - Description

  - [ ] Keywords

#### Submission [Google Play Console](https://play.google.com/apps/publish)
- [x] Upload APK to the alpha or beta channel

- [x] Define app's compatibility

- [ ] Check pre-launch reports

- [x] Setup app's price and countries of distribution

- [ ] Opt-in to the right distribution options

        ie Android Wear and TV

#### Production
- [x] Determine app's content rating

- [ ] Final checks and publishing
