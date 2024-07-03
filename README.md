Here's the translated text to English:

---

# UnrealDemoScanner 
#### A .dem file scanner designed to analyze and scan Counter-Strike 1.6 demo files for the presence of prohibited programs.
#### Does not require the game to be running or even installed on the computer, and unlike ViewDemoHelper, it can detect a large number of cheat programs without false positives.

---
Difference from ViewDemoHelper:
-
### Pros:
- Does not require the game to be installed
- Works with clean input data
- Detects all types of cheats released up to 2020
- Ability to scan multiple demo files at once

### Cons:
- Console application without the ability to quickly review moments
- Does not have access to the game API, which leads to additional RAM usage to simulate the game engine and prevents the detection of some types of cheats (e.g., checking if a player is alive, what weapon they have, storing extra data in memory). Scanning a 100MB demo file requires 0.5GB to 1GB of RAM.
- Scanning large demo files can take a considerable amount of time

# Installation and Running
- Unpack the **unrealdemoscanner.zip** archive into a separate folder
- Run **UnrealDemoScanner.exe**
- Drag the player's demo file into the console or enter the path manually
- Press the **Enter** key once
- Wait for the scan to complete
- After scanning, you can enter one of the commands to view additional information

# Description of Aimbots and Other Cheats
- AIM TYPE 1 - Attack delay

- AIM TYPE 2 - Autoattack with pistols

- AIM TYPE 3 - Sharp aim jerks (incomplete)

- AIM TYPE 4, FAKELAG - Fake lag

- AIM TYPE 5 - Smooth angles/etc - Software angle smoothing

- AIM TYPE 6 - HPP Autoattack - Autoattack from HPP v5

- AIM TYPE 7 - HPP Trigger bot - Trigger bot (from HPP) or hard aimbot

- AIM TYPE 8 - Universal AIMBOT detection

- TRIGGER BOT, KNIFEBOT BOT - Old aim hacks

- FPS HACK - A cheat that allows bypassing the FPS limit, part of other cheats

- CMD HACK - Modifying game frames (e.g., CMD HACK TYPE 1 allows hovering in the air)

- MOVEMENT HACK - Programmed movement

- DUCK HACK - Programmed ducking

- JUMP HACK - Programmed jumping

- Many other cheat functions.

# Command Line, Launch Parameters
- **-dump** — saves the entire demo file to a text representation, can be used to analyze cheat programs without modifying the scanner's source code
- **-debug** — outputs debug information
- **-alive** — marks the player as alive at the start of the demo (forcibly)
 
## False Positives
##### Warnings [WARNING] 
- may appear from time to time when the scanner considers a moment suspicious but not enough to be 100% sure it is a cheat. Such moments should be reviewed manually; I recommend using View Demo Helper or a similar program to examine the moment precisely. The presence of several warnings is not a reason to consider a player a cheater without reviewing the moments in the game. 
  
##### Detections [DETECTED] 
- displayed when the scanner is absolutely certain that the moment is a cheat or a cheat script, and there should be no false positives. *(However, due to some exceptional situations, I allow for 1-2 false positives per 10-20 minutes of demo duration)*
- Almost all cheats released up to 2020-2021 are detected, but modern cheats may not be detected by the scanner, so the absence of detections does not mean the player is not a cheater. 

# Support
If you find multiple false positives [DETECTED] in your demo, send the demo to me for analysis and release of fixes.

Due to the fact that I no longer play CS 1.6, scanner updates are rare. If you are a developer and know methods of working with cheats that are not detected by the scanner, or if you want to join the development of the scanner, you can contact me.

To review moments in the demo, I recommend using [ViewDemoHelper](https://github.com/radiusr16/view_demo_helper) or other similar programs.

## Demo files used for checks
- You can take from the archive: https://github.com/UnrealKaraulov/UnrealDemoScanner/tree/1935a1c9ba62c998bdf74125866728b0ddf4b58b, large demo files are left there. The repository only stores short demo files without any extra content.
