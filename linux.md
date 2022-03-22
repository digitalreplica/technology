# Linux

Copy file to clipboard
cat input.txt | xclip -i

Logging console output
script

Temporarily disabling bash history
unset HISTFILE

## Screen / tmux
Creates a session that survives a ssh connection dropping

tmux
* Command prefix CTRL+B
* Start new session: ```tmux```
* List sessions ```tmux ls```
* Reattach to a session ```tmux a -t <session>```. If the default numbered session, ```tmux a -t 0```
