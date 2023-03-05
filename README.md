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
  There is a short amount of time, required of you to spend in Ankidroid every n hours. By default it's `45 seconds` every `1 hour`.
  <br><br>You know you are in this state if you see `Anki time!` popup. 
  ### Distracted state
  If for some reason you fail to spent `45 seconds` of time, and\or quit Ankidroid app, the program will let you be distracted for `30 seconds` by default,
  and it will launch Ankidroid again when you unlock your phone or after `30 seconds` have passed. Your progression of work that you've done before 
  getting distracted will be saved. When in distraction state the program is meant to be more pushy and more annoying, while also giving you a small
  window to be distracted in case it's something important and you can't finish your anki working sprint in one sitting.
  <br><br>You know you are in this state if you see `Anki is closed, see ya!` popup (if you didn't get another popup before about moving to cooldown state).
  ### Cooldown state
  If you manage to spend in total `45 seconds` for learning Anki, you will be granted `1 hour` of cooldown time, which means anki won't bother you next `1 hour` as a reward because you did a good job. After `1 hour` you move to `Work sprint state` again, cycle repats.
  <br><br>You know you are in this state if you see `Work sprint done. Good job!` popup.
  ### Snoozed state (soft turn off)
  If you are outside and need your phone to be functional 100% without annoying anki trying to force itself onto your screen, you can click on the `Anki` tile in android tile menu, which will snooze the script for `30 minutes` by default. It's not recommended to use this setting constantly otherwise the whole point of not forgetting to do anki will be lost.
  <br><br>You know you are in this state if you see `Snoozed for 30 min Zzz` popup.
  ### Finished state (hard turn off)
  This state means you're done with anki for today. To go to this state, you need to first click on `Anki` tile, which will snooze it first, and then you need to click on notification `Done for today?`. It will start script that syncronises Anki with cloud and turns it off for the whole day. (you can always click on the tile again to turn it back on)
  <br><br>You know you are in this state if you see `Done with Anki for today!` popup.
  
#### How to customize
IF you want to customize all of those default times, you can do this in Macrodroid variables.
