# anki-recall
This is a collection of scripts for MacroDroid that can help you prevent missing Anki on your Android phone.

***
## Installation

### Prerequisites

Operating System: Android
#### Set up MacroDroid
0. Install [AnkiDroid](https://play.google.com/store/apps/details?id=com.ichi2.anki) if it is not already installed. Set up AnkiDroid so that it works properly.
1. Install [MacroDroid](https://play.google.com/store/apps/details?id=com.arlosoft.macrodroid "Play Store link").
2. Open MacroDroid, scroll to the bottom and open `Quick Settings Tiles`. Enable the first one.
3. //here will be some other steps later

#### Download the [Anki Category Script Collection](https://github.com/labmem8/anki-recall/releases/tag/pre-release).
1. Open it with MacroDroid.
2. Give it the necessary permissions: `Accessibility Permission`, `Usage Statistics`, `Notifications` (this one is optional and only needed for a small part of the functionality, which involves clearing old notifications and checking if the alarm application is running).
3. Go to `Macros` and switch `Anki Init` macros. This will initialize all other macros and variables.
4. Go to the Quick Settings Dropdown on your phone (the thing where your Wi-Fi tile is) and edit it. You will see `MacroDroid Tile 1`. Move it to the regular tiles and quit the edit menu.
5. The tile you moved should now have the name `Anki` and an icon of a lamp. Click on it. You will see a popup message saying `Anki is back!`
6. You're done!

***
## Description
The program has 5 states:

### Work sprint state
This state requires you to spend a short amount of time in Ankidroid every n hours, which is set to `45 seconds` every `1 hour` by default.
You can identify this state by seeing the `Anki time!` popup.

### Distracted state
If you fail to spend the required `45 seconds` in Ankidroid, or quit the app for any reason, the program will switch to the distracted state. 
In this state, you are allowed to be distracted for `30 seconds` by default, and then the program will relaunch Ankidroid. Your work progress is saved while you are distracted.
This state is designed to be more pushy and annoying, but it also gives you a small window to be distracted in case it's important and you can't complete your Anki work in one sitting.
You can identify this state by seeing the `Anki is closed, see ya!` popup (if you didn't get another popup before about moving to cooldown state).

### Cooldown state
When you spend a total of `45 seconds` in Ankidroid, you will be rewarded with a `1 hour` cooldown period where Anki won't bother you. After the cooldown period ends, you move back to the `Work sprint state`, and the cycle repeats.
You can identify this state by seeing the `Work sprint done. Good job!` popup.

### Snoozed state (soft turn off)
If you're outside and need your phone to function without interruptions, you can use the `Anki` tile in the Android tile menu to snooze the script for `30 minutes` by default. However, it's not recommended to use this setting constantly, as the purpose of the program is to prevent you from forgetting to do Anki.
You can identify this state by seeing the `Snoozed for 30 min Zzz` popup.

### Finished state (hard turn off)
This state means that you've completed your Anki work for the day. To enter this state, you need to first click on the `Anki` tile, which snoozes the script, and then click on the notification `Done for today?`. This will synchronize your Anki data with the cloud and turn off the program for the rest of the day. You can always turn it back on by clicking the tile again.
You can identify this state by seeing the `Done with Anki for today!` popup.

#### How to customize
If you want to customize the default times for each state, you can modify the values of the Macrodroid variables.

