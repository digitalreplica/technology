---
is_a: "[[operating system]]"
urls: https://en.wikipedia.org/wiki/MacOS
---
# Notes
Mac OS Notes

## Keyboard tricks
Emoji keyboard
* Edit > Emoji & Symbols
- ctrl-command-space

Accented letters
* Hold the key down for the letter, and a popup will appear with accents for that letter.

## Open disk image
```
open "diskimage.sparsebundle"
```

## Edit hosts file
https://www.mactip.net/how-to-edit-the-hosts-file-on-a-mac/

## Ejecting disk from CLI
Finding the disk. Look at the `IDENTIFIER` field to find the exact disk to use
```
diskutil list
```

Eject disk
```
diskutil unmount /dev/disk3
```

Remounting, if needed
```
diskutil mount /dev/disk3
```

## Scheduled Tasks using Launchd
[ScheduledJobs | Apple Developer](https://developer.apple.com/library/archive/documentation/MacOSX/Conceptual/BPSystemStartup/Chapters/ScheduledJobs.html)
- Preferred method is launchd, though cron-style jobs still supported
- 2022-06-27: launchagent method broken in MacOS

Create a plist file like `com.user.diskejector.Seagate2TB.plist` in ~/Library/LaunchAgents

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
	<dict>
		<key>Label</key>
		<string>com.user.diskejector.Seagate2TB</string>
		<key>ProgramArguments</key>
		<string>diskutil unmount /dev/disk3</string>
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

### Using crontab
Edit crontab
```
EDITOR=nano crontab -e
```

Schedule task
```
00 11 * * * /usr/sbin/diskutil unmount /dev/disk3
```

## Contacts
Delete contact from group * Click group * Hit delete * Select “Remove from Group”
Groups IOS doesn’t support smart groups (suck). So create a smart group (note contains `#tag`). Create an iCloud group. Create another smart group called Verify where membership is in smart group and membership not in group.

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

## Temporarily prevent idle sleep
* One hour: ```caffeinate -i -t 3600```

# Mac OS Disk Images
## Sparse image
* thin-provisioned disk image, saved as one file
* Best for Dropbox, since they only upload changed blocks

## Sparse Bundle Image
* thin-provisioned disk image, saved as 8MB bands
* Best for iCloud, since it uploads entire changed files
* Do NOT use on dropbox. If opened on two computers, Dropbox conflict detection will create a copy of a band, and Mac OS will show the entire image as corrupted.

# Show hidden and system files
* Open Finder
* <command><shift><.>

Permanantly
```
defaults write com.apple.Finder AppleShowAllFiles true
killall Finder
```

# Troubleshooting
Force power off: Hold power button for 10 seconds

Safe mode: Power on and immediately hold <shift>

Links
* [If your Mac doesn’t start up all the way - Apple Support](https://support.apple.com/en-us/HT204156)
