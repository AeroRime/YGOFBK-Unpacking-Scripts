# YGOFBK-Unpacking-Scripts
Repository for the bms extraction scripts for the .pac files in YGOFBK.

## How to use 
1. You need to download quickbms to use the .bms scripts, which you can get here: https://aluigi.altervista.org/quickbms.htm

2. Use the .bms scripts to extract the DSP files from str.pac and the grp files from grp.pac.  Please note that you will have to output the same filenames since the generic archives don't have any filenames or paths, just the pointers before the sub-files.

3. Download vgmstream or Foobar2000 with the vgmstream component.  Please refer to one of the two sub-sections below for reference.

4. Enjoy! 

*Disclaimer: Some of the pointers in the .pac containers point to empty files; please disregard them.


### The bgm
The dsp(s) in str.pac are dual-stereo.  Please refer to the usage guide for vgmstream for more details on how to rip dual-stereo music:
https://github.com/vgmstream/vgmstream/blob/master/doc/USAGE.md

When ripping the music, the first dual-stereo pair are empty (might have been for development or for having silence for the opening movie), while both the 23rd DSP pair is a duplicate song of the 9th DSP pair.


### The sfx
For grp.pac, you not only need to extract the grp(s) (the multi-header wave groups for lack of a better term), but you need to use the txth provided in order to rip the sfx from each grp using vgmstream.  Please refer to this guide here to use your txth file with your extractions:
https://github.com/vgmstream/vgmstream/blob/ae23220716f02b2577a087a16c8ef6964c5d1bf3/doc/TXTH.md

The sfx in system.grp can also be ripped via the txth file using vgmstream.  This is speculation, but I'm guessing that the sfx in this specific grp are all unused in-game, so they may have been used during development for the game. 

Please Note: If you are using Foobar2000 with the vgmstream component to rip the sfx, check to make sure that "Enable common exts" is turned on first.  This should allow you to use the txth file that is provided with the bms scripts.


## Needed changes
Let me know if you have any questions about using the bms script or have any suggestions to improve the script itself.  This was a small project I decided to do for fun, so if anyone wants to create a more convenient script based off the bms script, by all means you may use the parts of the script as reference, but please credit me.

The grp(s) in Falsbound Kingdom are linked to specific monsters in-game.  Although the in-game songs are well-known, there's no wiki or any documentation about the monsters (to my knowledge).  Some of the monsters in-game use the same sfx (or some sfx with some more subtle changes) with some sfx being recycled from Yu-Gi-Oh! The Duelist of the Roses.  One of the grp(s) contains all the menu and other UI sfx, as well as some unused voicelines (there are a few voicelines used in-game upon inputting the Konami Code).  I don't have plan on creating a text file with a list of the grp(s) matching the monsters or UI for the time being, but if anyone wants to create a full list of monsters with their corresponding sfx for me to include in this repository, you can let me know by creating an issue, creating a merge request, or by creating a fork of this repository.


## Special Thanks/Credits
bnnm - https://github.com/bnnm (helped with creating the txth file)

aluigi - https://github.com/aluigi (code source)
