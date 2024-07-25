# Echo360 super speed userscript

> _Note that this project is not endorsed by or affiliated with Echo360_

### [Click here to install userscript](https://github.com/peter-tanner/Echo360-Super-Speed/raw/master/echo360-super-speed.user.js)

### [Alternative installation link (Greasyfork)](https://update.greasyfork.org/scripts/501694/Echo360%20Super%20Speed.user.js)

Adds faster speed options (4x, 3x) to Echo360 player and allows the user to add their own speed options. Works on Chromium (Google Chrome, Brave, etc.) and Firefox

<img src="docs/superspeed.png" style="max-height: 40vh" />
<!-- ![Dropdown with 4x and 3x speeds](superspeed.png) -->

## Installation guide

This should only take 5 minutes.

### 1. Install Violetmonkey

If you already have a userscript manager you can skip this step.

Click "Install" or "Get" then accept the permissions

### [Firefox installation](https://addons.mozilla.org/en-US/firefox/addon/violentmonkey/)

### [Google Chrome installation](https://chrome.google.com/webstore/detail/violent-monkey/jinjaccalgkegednnccohejagnlnfdag)

### [Microsoft Edge installation](https://microsoftedge.microsoft.com/addons/detail/eeagobfjdenkkddmbclomhiblgggliao)

### 2. Install this Userscript

Click any one of these links and it should redirect you to an install page.

### [Click here to install userscript](https://github.com/peter-tanner/Echo360-Super-Speed/raw/master/echo360-super-speed.user.js)

### [Alternative installation link (Greasyfork)](https://update.greasyfork.org/scripts/501694/Echo360%20Super%20Speed.user.js)

Click the "Install" button and you should have 4x and 3x speeds on Echo360 (refresh any open Echo360 pages).

![install](docs/install.png)

### Done!

## Adding your own speeds

Open the userscript file, then modify the `selected_speeds` and/or `speed_hotkey_increment` constants which are in the `USER CUSTOMIZATION` section.

For example, if I wanted only 4x, 3x and 2x options, I can replace the `selected_speeds` constant with the following:

```js
const selected_speeds = [4, 3, 2];
```

⚠ Note that there is a browser-set speed limit of 16x and speeds above 4x are muted, according to [the constants set in the brower's source](https://stackoverflow.com/a/32320020). This applies to both Firefox and Chromium.

## Current issues

- When setting `selected_speeds` to a list of speeds which does not include 1x, the player by default loads with 1x speed when the page is loaded. Once the speed is changed manually by clicking on a speed from the dropdown this is not an issue anymore, but it would be nice if the default speed was valid.
