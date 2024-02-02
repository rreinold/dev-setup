# Robs local setup

## General

System Preferences > Sound > PLay sound at startup: Disabled

Prefer tabs: always

Ask to keep changes when closing documents: Disabled

Show scroll bars: automatically

Allow handoff: Disabled

Notifications:

- show preview: When unlocked (see Slack settings for dont preview)

Mission Control

	- Automatically rearrange: Disabled
	- Displays have different spaces: Disabled

## iTerm

.zshrc

source shell_profiles

Ensures true word-by-word moves works, with shell setting:

```
autoload -U select-word-style
select-word-style bash
```

Keyboard shortcuts

| Input                       | Action    | Keyboard Shortcut |
| --------------------------- | --------- | ----------------- |
| i#/bin/bash\n\n             | Send Text | cmd + shift + b   |
| (prevent maximize shortcut) | Ignore    | cmd + Enter       |



Settings:

- Closing
  - Confirm x2: Disabled

## PyCharm

- Appearance and Behavior
  - System Settings
    - Project
      - Reopen: Disable
  - Editor
    - Enable preview tab: Enabled
    - Gutter
      - Line numbers only
    - Inlay Hints
      - All: Disabled
    - General
      - Smart Keys
        - Insert pair quote: Disabled
      - Change font size..mouse
        - Enabled
      - Editor Tabs
        - Show tabs in: Squeeze
        - Show pinned tabs in separate row: Enabled
        - Show file icon: Disabled
        - Show file extension: Disabled
        - Close button: Disabled
      - Tab Order
        - Open new tabs at end: Enabled
      - Closing Policy
        - Tab Limit: 20
  - PEP 8 style violation: ignore
- Version Control
  - Confirmation
    - Disable all

- Key mappings

| Action                   | Key              |
| ------------------------ | ---------------- |
| Remove all breakpoints   | shift+cmd+del    |
| Delete Line              | cmd+D            |
| Text End                 | cmd+down         |
| Text Start               | cmd+up           |
| Go to file               | cmd+T            |
| Go to line               | cmd+shift+T      |
| Move line up             | option+up        |
| Move line down           | option+down      |
| Next tab                 | option+cmd+right |
| Prev tab                 | option+cmd+left  |
| Open file                | cmd+O            |
| Rename element           | shift+cmd+R      |
| Restore default layout   | cmd+`            |
| Debugger: Resume Program | ctrl+up          |
| Split Right              | cmd+2            |
| Step Into My code        | ctrl + right     |
| Step Out                 | ctrl + left      |
| Toggle Line Breakpoint   | option + cmd + / |
| Plugins > Python File    | cmd + N          |
| Editor > Pin Active Tab  | cmd + P          |



## Poetry

https://python-poetry.org/docs/

using a curl



## Applications

## Keyboard 

### Text

| Replace | With                     |
| ------- | ------------------------ |
| g@      | <WORK_EMAIL>             |
| rew     | <PERSONAL_EMAIL>         |
| rqq     | <USERNAME>               |
| zmr     | <ZOOM_PERSONAL_ROOM_URL> |
| c@      | category:primary         |

Turn off Correct spelling automatically, Capitalize, Use smart quotes

- Keyboard > Services > Text: Disable All

Keyboard Shortcuts > Screenshots > Set Save screen to file as Cmd + Shift + 3

### Keyboard

Key Repeat: 6/7

Delay Until Repeat: 2/5

Caps Lock: mapped to escape

Shortcuts:

- Mission Control
  - Mission Control (yes again)
    - Move left a space: Disabled
    - Move right a space: Disabled

## Spelling

all off

## Trackpad

- Point & Click:

  - Tracking Speed: 3/10

  - Click: Medium

  - Tap to click: Enabled

  - 

  - Lookup and data detectors: Off

  - Secondary Click: Enabled

  - Force Click and haptic feedback: Disabled

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

Must install via brew, not App Store

- System Settings > Keyboard > Keyboard Shortcuts > Spotlight: Disable
- Launch at login: Enabled
- Alfred Hotkey: command+space
- Search: Applications, Preferences
- Add Applications dir
- Include Home Dir: Disabled
- Appearance > Options > Hide Menu Bar

BetterSnapTool

- Start BetterSnapTool everytime your Mac starts up: Enabled

Maccy

- Size: 30
- Files: Disabled

Micro-Snitch

- Run at login

Fantastical

- Show dock: control+option+space
- Open maps: Google Maps
- General > Play user interface sounds: Disabled

## Chrome

chrome://flags

​	Hardware Media Key Handling: Disabled

Add my fork of chrome extension: https://github.com/rreinold/chrome-bookmark-search

Extensions > Enable Developer Mode > Load unpacked

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

Menu Bar: Automatically hide and show the menu bar on desktop/full screen: Always

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

Desktop & Dock: Shortcuts

​	Remove ctrl up and down

## Typora
Sstting > Disable pair quotes
## Slack

Emojis: Thumbs up, Bow, Eyes

My Keywords: robby, rreinoldsc

Sidebar: Direct, Later, Mentions& Reactions

Spellcheck: Off

Advanced: Choose download location

## Github

one ssh key per gh account

```
ssh-keygen -f ~/.ssh/<KEY_NAME> -N ''
ssh-add ~/.ssh/<KEY_NAME>
```

## Git

git config --global user.email "<EMAIL>"

git config --global user.name "Your Name"

## iTerm

Preferences > Profiles:

- Working Directory: Reuse previous session's directory

- Terminal > Unlimited Scrollback

- Notifications > Silence Bell: Enabled
- Notifications > Notification Center Alerts: Disabled
- Keys
  - Preset > Natural Text Editting

## AWS

https://aws.amazon.com/cli/ install via pkg

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

prepend:

```eval "$(/opt/homebrew/bin/brew shellenv)"
eval "$(/opt/homebrew/bin/brew shellenv)"
```

```
plugins=(git tmux  zsh-autosuggestions zsh-syntax-highlighting fast-syntax-highlighting)
```



## Docker

- General:
  - Start at login: Disabled
  - Start Docker Dashhboard at startup: Disabled
  
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
- Notes
  - control + enter: ignores autocompleted URLs
  - clear history to prevent autocompleting
- Site Settings
  - Notifications
    - Disabled for all



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

## psql cli

```
brew install libpq
brew info libpq
# use libpq instead?
export PATH=/opt/homebrew/Cellar/postgresql@13/13.12/bin/:$PATH
```



## misc

```
brew install bat ca-certificates cmake csvkit curl entr gnupg grep helm httpie jq kubectx md5sha1sum watch tree sops jless glow tmux overmind nmap gh
```

need to add repo for granted, speedtest-cli

## Python

alias python=$(pyenv which python)

then newenv

## Zoom

General:

Always show meeting controls: disabled

ask me to confirm when I leave meeting: Disabled

Stop my video and audio when my display is off: Enabled

Video:

Original ratio: Disabled

HD: Enabled

Mirror my video: enabled

Touch up: 25%

Always display parti names: Disabled

Stop by video when joining a meeting: Enabled

Audio:

- Automaticall join computer audio
- Mute my mic when joining

Video:

​	- 49 participants

## iMessage

Play sound effects: Disabled

## iCloud

Sync just contacts



 ## Control Center

Menu bar > Clock

- 24h
- Show seconds
- Show date: Always

Wifi: Always Show

Bluetooth: Always Show

Sound: Always Show

Focus: Don't Show

Battery: 

- Show Percentage: Yes

Spotlight: Don't show



## Errors

curl error: "error setting certificate verify locations"

Verify:

```
echo $SSL_CERT_FILE
```

Keychain > System Roots > Certificates

```
brew info openssl
=> /opt/homebrew/etc/openssl@3/certs
```

Certificates > Select All > File > Export Items... > /opt/Homebrew/openssl@<VERSION>/certs/cert.pem

add to shell profile:

```
export SSL_CERT_FILE=/opt/Homebrew/openssl@<VERSION>/certs/cert.pem
```





## Vim

.vimrc:

```
:command W w
```



```
```



## node

install nvm: https://github.com/nvm-sh/nvm#usage

```
npm install --global yarn

```



cd where there is a .nvmrc

```
nvm install
```



## Speedtest

```
brew tap teamookla/speedtest
brew update
brew install speedtest
```

## Whatsapp

- Setting > Notifications > Turn off sound

try `fd`

`moom`

## VSCode

Hover delay: 1000ms

Hover disappear: 0ms
