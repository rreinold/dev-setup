# Robs local setup

## General

System Preferences > Sound > PLay sound at startup: Disabled

## iTerm

.zshrc

source shell_profiles

## PyCharm

## Applications

## Keyboard 

### Text

| Replace | With                     |
| ------- | ------------------------ |
| g@      | <WORK_EMAIL>             |
| rew     | <PERSONAL_EMAIL>         |
| rqq     | <USERNAME>               |
| zmr     | <ZOOM_PERSONAL_ROOM_URL> |

Turn off Correct spelling automatically, Capitalize, Use smart quotes

### Keyboard

Key Repeat: 6/7

Delay Until Repeat: 2/5

Caps Lock: mapped to escape

## Trackpad

- Point & Click:

  - Tracking Speed: 3/10

  - Click: Medium

  - Tap to click: Enabled

  - Lookup and data detectors: Disabled

  - Secondary Click: Enabled

  - Force Click and haptic feedback: Enabled

- Scroll & Zoom
  - Scroll direction: Natural
  - Zoom in or out: Enabled
  - Smart Zoom: Disabled (this increases double tap response time by 1s!)
  - Rotate: Enabled
- More Gestures
  - Swipe between pages: Disabled
  - Swipe between full-screen apps: 3 fingers

## Sleep

- Hooks

## Tool Configurations

Alfred:

- System Settings > Keyboard > Keyboard Shortcuts > Spotlight: Disable
- Launch at login: Enabled
- Alfred Hotkey: command+space
- Search: Applications, Preferences

BetterSnapTool

- Start BetterSnapTool everytime your Mac starts up: Enabled

Maccy

- Size: 30
- Files: Disabled

Micro-Snitch

- Run at login

Fantastical

- Show dock: control+option+space

## Chrome

Disable media controls

## Hostname

```
sudo scutil --set HostName <hostname>
```

System Preferences > Sharing > Hostname
General > About > Name

## Dock

Size: 50%

Magnification: 20%

Position: Bottom

Minimize windows into application icon: Yes

Show Recent applications in Dock: No

Menu Bar: Automatically hide and show the menu bar on desktop/full screen: No

Applications:

- Chrome
- Zoom
- PyCharm
- iTerm
- Fantastical
- Slack
- [Separator]
- Chrome Canary
- iMessage
- WhatsApp
- Spotify
- [Separator]
- SublimeText
- Typora
- System Preferences

Add Separator:

```
defaults write com.apple.dock persistent-apps -array-add '{"tile-type"="spacer-tile";}'
killall Dock
```



## Slack

Emojis: Thumbs up, Bow, Eyes

My Keywords: robby, rreinolsc

Sidebar: Direct, Later, Mentions& Reactions

Spellcheck: Off

## Github

one ssh key per gh account

```
ssh-keygen -f ~/.ssh/<KEY_NAME> -N ''
ssh-add ~/.ssh/<KEY_NAME>
```

## iTerm

Preferences > Profiles:

- Working Direectory: Reuse previous session's directory

- Terminal > Unlimited Scrollback

- Notifications > Silence Bell: Enabled
- Notifications > Notification Center Alerts: Disabled
- Keys
  - Preset > Natural Text Editting

## Terminal

Settings > Profiles > Bell > Audible & Visual Bell: Disabled

## Homebrew

brew.sh default

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

Update shell profile with <>

```
brew reinstall openssl
brew install --cask keycastr
```



```
brew install zsh wget
```

## Oh my zsh

Run setup here: https://sourabhbajaj.com/mac-setup/iTerm/zsh.html

## Docker

- General:
  - Start at login: Disabled

- Resources:
  - CPUs: 3
  - Memory: 4GB
  - Swap: 1.5GB
  - Virtual Disk: 64GB

## Chrome

- Auofill and passwords
  - Save and fill addresses: Disabled
- Downloads
  - Ask: Enabled
- chrome://flags/
  - Hardware Media Key Handling: Disabled
- Sync
  - chrome://settings/syncSetup/advanced
  - Sync Apps and Bookmarks

## Finder

- Favorites
  - tmp
  - r
  - Applications
  - Downloads
  - Screenshots
  - superco
  - expenses
  - projects
  - Desktop
  - Documents
- Advanced
  - Show all filename extensions: Enabled
  - Show warning before changing an extenson: Disabled
  - Remove items from the Trash after 30d: Enabled

## Screenshots

Open Screenshots > Options > Save to dir

System Preferences > Sound > play user interface sound  effects: Disabled

## Loom

Run at login: Disabled

## Stats

https://github.com/exelban/stats

```
brew install stats
```

## Sublimetext

Key Bindings:

```
[
	{ "keys": ["super+d"], "command": "run_macro_file", "args": {"file": "res://Packages/Default/Delete Line.sublime-macro"} },
	{ "keys": ["alt+up"], "command": "swap_line_up" },
    { "keys": ["alt+down"], "command": "swap_line_down" },

]

```

