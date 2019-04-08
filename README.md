# alfred-various-screenshots
[Alfred 3][1] workflow for taking various screenshots.

Currently supported storages are the following.
- Local drive
- Clipboard
- [Dropbox][4] service with an ability to share a link to the uploaded screenshot.
- [Transfer.sh][5] service with an ability to share a link to the uploaded screenshot.
- [0x0.st][6] service with an ability to share a link to the uploaded screenshot.
- [File.io][7] service with an ability to share a link to the uploaded screenshot. After uploaded image is downloaded, the file is completely deleted!!!

## Installation
1) Install [alfred-various-screenshots][2] workflow.
2) All further updates are handled automatically.

## Usage
In Alfred, type `ss`, which stands for ScreenShot and initiates a submenu which offers three options.

1) Screenshot - Area
2) Screenshot - Screen
3) Screenshot - Window

![Alfred menu screenshot](doc/images/alfred-various-screenshots.png?raw=true "")
![Alfred submenu screenshot](doc/images/alfred-various-screenshots-submenu.png?raw=true "")


By default, the screenshot is stored in a file located at your `~/Desktop` directory.
This could be overridden, either by pressing the <kbd>⌘</kbd> key, <kbd>⌥</kbd> key, or <kbd>⌃</kbd>.

- <key>⌘</key> - instructs the workflow to put a screenshot to the clipboard.
- <key>⌥</key> - shares a screenshot via Dropbox and stores a sharing link to the clipboard.
- <key>⌃</key> - shares a screenshot via Transfer.sh and stores a sharing link to the clipboard.
- <key>⇧</key> - shares a screenshot via File.io and stores a sharing link to the clipboard.
- <key>Fn</key> - shares a screenshot via 0x0.st and stores a sharing link to the clipboard.

Screenshot files will be named according to the following pattern `screenshot_%Y-%m-%d_%H-%M-%S.png`

           Y       Year in full form (e.g., 2006).
           m       Numeric month, a number from 1 to 12.
           d       Day, a number from 1 to 31.
           H       Hour, a number from 0 to 23.
           M       Minutes, a number from 0 to 59.
           S       Seconds, a number from 0 to 59.
           
 
Default local screenshot folder `~/Desktop` can be changed by the workflow `DefaultLocalScreenshotFolder` variable.

![Alfre Variable Local](doc/images/alfred-various-screenshots-variable-local.png?raw=true "")
           
### Dropbox
There is no need to install a Dropbox software to your MacOS. The only requirement is to log into the [web Dropbox account][3] and create an access token for the workflow.

![Dropbox App Creation](doc/images/dropbox-app-create.png?raw=true "")

------------------------------

![Dropbox App Key Creation](doc/images/dropbox-app-key.png?raw=true "")

Such generated access token shall be placed to the workflow `DropboxAccessToken` variable.

![Alfred Variable](doc/images/alfred-various-screenshots-variable.png?raw=true "")

[1]: https://www.alfredapp.com/
[2]: https://github.com/vookimedlo/alfred-various-screenshots/releases/latest
[3]: https://www.dropbox.com/developers/apps
[4]: https://www.dropbox.com/
[5]: https://transfer.sh/
[6]: https://0x0.st/
[7]: https://file.io/
