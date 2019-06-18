# Harkinius

VBScript-based application. Based off of and music/images sourced from "Snoop Hark" and "Harkinian Dancing (Blue Screen)" by Jimmy Davis on Youtube.

This repository has two applications:

HarkiniusNonMal.exe: Just the graphical/musical payloads of Harkinius.exe.
Harkinius.exe: Malicious edition of HarkiniusNonMal.exe. It WILL delete/change core files (such as .reg and .dll) - best advised to only test it on a VM!

In-depth on the payloads:

Non Malicious:
Not 4/20: It will make Hark dance in the middle of the screen, with the Blue Screen's song playing the background.
4/20: Plays Snoop Hark instead of the Blue Screen song.
6/9: Sets the date to 4/20 with the non-4/20 payload.
After each song is done playing or you quit the application, everything will turn back to normal.

Malicious (adds these functions):
Not 4/20: Disables Task Manager, Regedit and the option to enable hidden folders, changes the background to a tiled version of the application icon, drops the app to startup and increases the date by one day. Kills csrss.exe afterwards.
4/20: Deletes hal.dll with the non-4/20 payload. Does not increase the day by one.
6/9: Sets the date to 4/20, plays a special audio then it kills csrss.exe.
