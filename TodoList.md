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

- [ ] Distribution Certificate

    - [x] Development Certificate

    - [ ] Production Certificate

- [x] Provisioning Profile for development

- [ ] Test devices

        Need to connect to the Mac via USB
        and allow those devices to be added to the development
        Provisioning Profile for production

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
        Separate screenshots for iPhone/iPod Touch & iPad/iPad mini
        These screenshots will be used in the app store

- [ ] Metadata [apple's guide to metadata](https://developer.apple.com/app-store/product-page/)
  , [category outline](https://developer.apple.com/app-store/categories)

        1. Applications name
              UniteSalisbury
        2. Version number
              v1.1.9
        3. Primary (and an optional secondary) Category
              Primary Category: Social Networking
              Secondary Category: ??????
        4. Concise description
              ???????
        5. Keywords for search in app store (max 100 characters comma separated spaces count...)
              ex. (words,like,ones,that,searches,will,direct,to,Unite,Salisbury)
        6. Support URL (so people that need help with application can contact us...)
              ESRGC.org or github repo ?
        7. Since there is a login function we need to provide Apple with a test/demo account for review process (so they dont have to create an accout for the app... they are lazy)
              UserName: xxxxxx
              password: xxxxxx

#### Submission [submit app to app review](https://developer.apple.com/library/content/documentation/LanguagesUtilities/Conceptual/iTunesConnect_Guide/Chapters/SubmittingTheApp.html)
- [ ] Basic Info

  - [ ] Explain ATS exceptions

        If asked why the oxford server is not setup for https when apple is reviewing application will need to explain.

- [x] Price & Availability  $0

- [ ] Metadata

- [ ] Ready to Upload Binary

#### Upload to the Store
- [ ] must use an apple device to create the archive for upload

#### Wait...
- [ ] Waiting for review process to complete

---
## todo's for Android deployment

[Android deployment checklist](https://developer.android.com/distribute/best-practices/launch/launch-checklist.html)

#### Prerequisites
- [x] Build a release-ready APK

  - [x] Need to update target URL from whatsup to uniteSalisbury

  - [x] Test on bluestacks emulator

  - [x] Test on live device

#### Assets
- [ ] Plan for app's Play store listing (Metadata)

  - [x] Icon

  - [ ] Feature image

  - [ ] Screenshots

  - [ ] Description

  - [ ] Keywords

#### Submission
- [ ] Upload APK to the alpha or beta channel

- [ ] Define app's compatibility

- [ ] Check pre-launch reports

- [ ] Setup app's price and countries of distribution

- [ ] Opt-in to the right distribution options

        ie Android Wear and TV

#### Production
- [ ] Determine app's content rating

- [ ] Final checks and publishing
