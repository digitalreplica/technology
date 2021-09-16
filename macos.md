# Mac OS

## Emoji keyboard
* Edit > Emoji & Symbols
* <ctrl><command><space>

## Open disk image
```
open "diskimage.sparsebundle"
```

## Edit hosts file
https://www.mactip.net/how-to-edit-the-hosts-file-on-a-mac/

##Scheduled Tasks using Launchd
Create a plist file like com.user.diskejector.Seagate2TB.plist

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
<key>Label</key>
<string>com.user.diskejector.Seagate2TB</string>
<key>Program</key>
<string>/Users/user/bin/ejectSeagate2TB.sh</string>
<key>StartCalendarInterval</key>
<dict>
<key>Hour</key>
<integer>16</integer>
<key>Minute</key>
<integer>00</integer>
</dict>
</dict>
</plist>
chmod 644 com.user.diskejector.Seagate2TB.plist
cp com.user.diskejector.Seagate2TB.plist ~/Library/LaunchAgents
launchctl load -w ~/Library/LaunchAgents/com.user.eject2TB.plist
```
(Anything in ~/Library/LaunchAgents loads on login automatically, this is to load it after login)

## Contacts
Delete contact from group * Click group * Hit delete * Select “Remove from Group”
Groups IOS doesn’t support smart groups (suck). So create a smart group (note contains #tag). Create an iCloud group. Create another smart group called Verify where membership is in smart group and membership not in group.

## Burn ISO to USB
IMHO the easiest way is in terminal:
First run diskutil list then insert your usb stick and run diskutil list again to see the disk node (e.g. /dev/disk2). Now run diskutil unmountDisk /dev/diskN and do sudo dd if=/path-to.iso of=/dev/rdiskN bs=1m When finished diskutil eject /dev/diskN

## Verify sha1 digest
openssl sha1

## Creating Disk Image
* Disk Utility
* New Blank Image
* Encryption: 256-bit AES
* Image Format: sparse bundle disk image
* Format: APFS

## Preferences

* General: Dark mode, Disable Handoff
* Dock: Left, smaller
* Security: Require password immediately, FileVault on, Firewall on, block all services
* Keyboard, Touch Bar screen lock instead of Siri, dictation on, enchanced
* Trackpad scroll disable natural
* Accessibility: Speech Ava, speak selected text on

## Screenshot location

mkdir ~/Screenshots
defaults write com.apple.screencapture location ~/Screenshots
killall SystemUIServer

## Zsh profile
cat >~/.zshrc

## Terminal Preferences
SF Mono 12. Window 180 x 60

## Disabling Siri Keyboard shortcut
* System Preferences, Keyboard, Shortcuts, Spotlight. Uncheck “Show Spotlight search”

## Wifi disconnecting switching users

wifi - Wi-Fi disconnects when I lock the Mac - Ask Different
As admin:
cd /System/Library/PrivateFrameworks/Apple80211.framework/Versions/Current/Resources
sudo ./airport en0 prefs DisconnectOnLogout=NO

## Mac OS Security

How to Make Your Mac as Secure as Possible

## Launch scheduled tasks on a Mac using launchd

* Schedule script in ~binjournal
* Launch agent in ~LibraryLaunchAgents/com.user.journal.plist

## Using Launchd to run a script every 5 mins on a Mac | Splinter Software
Apple - Scheduling Timed Jobs
Apple - Creating Launch Daemons and Agents
