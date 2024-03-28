(This repository contains that publicly accessible content associated with the BirdUp Access app, such as the ReadMe and Privacy Statement. The app’s source code is not public.)

# BirdUp Access V1 User Guide

The BirdUp Access app is based on J. Burn’s BirdUp bird song identification app, and is an exploration into how such an app can be made as accessible as possible. Some technical thoughts on the app are available at [Is Accessibility for the Birds?](https://www.linkedin.com/pulse/accessibility-birds-guy-barker-a8eee). Teh app can be freely downloaded fomr the Gooogle Play Store at [BirdUp Access](https://play.google.com/store/apps/details?id=com.guybarker.birdupaccess).

Based on feedback from users, the usability and accessibility of the app will be improved in future versions.

Today the app runs on Android devices, and can identify specific birds in the UK and other western European countries.

# Identifying bird song

To attempt the identify bird song, click the “Record” button in the “Listen” page in the app. While listening, the app will show a chart with the frequencies of the noises it hears, and once it feels confident that a noise matches a bird, is shows the matched bird song in a list beneath the chart. Once you’re done listening, press the “Stop” button. 

The following are potential reasons why the BirdUp Access app might not be able to match bird noise.

* The bird song is too quiet for the app.
* There’s too much other noise, such as wind or traffic.
* The phone is moving too much, or its microphone is not pointing towards the bird song.
* The bird song is happening while other birds are singing.
* The bird is not in the list of birds associated with the current habitat in the app.

As such, to get the best results, try to have the app hear only the bird song, and as loud as possible.

<img src="/assets/images/BUA_Default_BirdMatch.jpg" alt="TBD" width="540" height="1200">
<img src="/assets/images/BUA_Default_BirdDetails.jpg" alt="TBD" height="1200">
<img src="/assets/images/BUA_Default_BirdList.jpg" alt="TBD" height="1200">

<img src="/assets/images/BUA_LargeFont_BirdMatch.jpg" alt="TBD" height="1200">
<img src="/assets/images/BUA_LargeFont_BirdDetails.jpg" alt="TBD" height="1200">
<img src="/assets/images/BUA_LargeFont_BirdList.jpg" alt="TBD" height="1200">

<img src="/assets/images/BUA_DarkMode_BirdDetails.jpg" alt="TBD" height="1200">
<img src="/assets/images/BUA_DarkMode_BirdList.jpg" alt="TBD" height="1200">
<img src="/assets/images/BUA_DarkMode_BirdMatch.jpg" alt="TBD" height="1200">
<img src="/assets/images/BUA_DarkMode_Session.jpg" alt="TBD" height="1200">

<img src="/assets/images/BUA_TalkBack_BirdDetails.jpg" alt="TBD" height="1200">
<img src="/assets/images/BUA_TalkBack_BirdList.jpg" alt="TBD" height="1200">
<img src="/assets/images/BUA_TalkBack_BirdMatch.jpg" alt="TBD" height="1200">
<img src="/assets/images/BUA_TalkBack_Session.jpg" alt="TBD" height="1200">

<img src="/assets/images/BUA_VoiceAccess.jpg" alt="TBD" height="1200">
<img src="/assets/images/BUA_Magnification.jpg" alt="TBD" height="1200">


# Sessions and Recordings

Every time the app is started, it creates a new session which can be accessed through the “Sessions” page. A session provides access to all the bird songs matched during that session, and provides some information about matched particular bird song. It also provides access to the recording of the bird song, and a sample of the bird song, meaning that the recording and the sample can be compared.

All recordings are stored locally on the device, and can be permanently deleted at any time. You may want to consider deleting sessions and recordings which contain no matches in order to make it more efficient to access sessions that do have matches.

# Birds and Habitats

The app has a currently selected habitat (for example, “Netherland and Belgium Gardens), and with each habitat has a list of associated birds. Please select a current habitat that’s the closest match to your actual location, otherwise there’s an increased chance that a bird heard by the app won’t be in the list of birds it will use to attempt a match. For example, if the current habitat is “UK Parks and Gardens” and a honking Canada Goose flies overhead, a match will not be found as the Canada Goose in not in the list of birds associated with the “UK Parks and Gardens” habitat.

# Settings

There are many configurable settings in the app, which can help to tune the attempt to match bird song. It is suggested that to start with, attempts are made to find matches using the default settings, before adjusting the settings. 

# Large text

While the design of the BirdUp Access V1 app intentionally follows the general design of the original BirdUp app on which it is based, it has been built to accommodate large text, following an increase in the device’s “Font size setting”. The goal is that no text is inaccessible when displayed as large text. This means that multiline content might scroll vertically, or single line content will either scroll horizontally or wrap to a second line.

Important: Due to a limitation in the technology on which the BirdUp Access app is built, in some places text does not wrap. Until this issue is resolved, some text is inaccessible in the app. The issue is being tracked at [BUG] Android: LineBreakMode="WordWrap" not working when label in popup #1664.

Note that the list of matched birds shown on the “Listen” page is sorted by how confident the app is in each match, so the highest confidence matches are at the top of the list. This means that if the full list of matches does not fit on the screen, the list might not appear to change when a new match is added to the list.

# Dark mode

The app shows a different set of colours depending on whether the device’s “Dark mode setting” is “Light” or “Dark”. The colours shown on the chart when listening for bird song are configurable through the app’s “Chart settings”.

# TalkBack

The TalkBack screen reader can navigate through the text and buttons in the app using the standard TalkBack navigation techniques. 

Important: Due to a limitation in the technology on which the BirdUp Access app is built, TalkBack does not announce which item in a list of items is the selected item. Until this issue is resolved, the only way that you can know which setting in a list of setting options is selected, is by noting the details of the selected setting before or after navigating to the list of setting options. The issue is being tracked at Android TalkBack screen reader doesn't tell the user which item is selected in a .NET MAUI CollectionView #21375.

Important: Today the chart shown in the app when listening for birds is not accessible. It is a goal to improve the accessibility of the data shown in the chart based on feedback from users. Note also that while TalkBack’s swipe gesture can more TalkBack to the chart, TalkBack does not move to the chart when moving your finger directly over the chart.

When action is taken in the app which immediately triggers the app to listen (for example, pressing the “Record” button on the “Listen” page), TalkBack does not make an announcement. This is to avoid the TalkBack announcement being heard by the app and the app trying to match the noise to a bird song. When the app stops listening however, TalkBack will make an announcement.

Important: The app attempts to avoid some opportunities for TalkBack’s announcements being considered as noise which should be analysed for a potential bird song match. For example, when a match is found when listening for a bird, the app stops listening for 3 seconds, giving TalkBack a chance to make the match announcement. It is recommended that you don’t move TalkBack around the app while the app is listening for birds. Rather, once a match is found, stop the app listening for birds, and then explore the match results. Today if TalkBack does make extended announcements while listening for birds, the app might incorrectly announce a low confidence match with a bird such as a jackdaw.


Other accessible-related features available on your device, (for example, Speech input and Magnification), will behave in the standard way in the BirdUp Access app.

# Speech input

The Voice Access feature on the device can interact with the text and buttons in the app using the standard Voice Access techniques. For example, speak the number shown beside the button to be clicked.

Note that if a list item has two different numbers shown on it, and speaking one of those numbers only selects the item without clicking it, try speaking the other number.

# Magnification

The app takes no specific action relating to the device’s Magnification feature, and Magnification works in the standard way at the app.


