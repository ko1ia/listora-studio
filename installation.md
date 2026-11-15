# Installation and updates

[← Getting started](getting-started.md) · [Guide home](README.md) · [Next: License activation →](license-activation.md)

You need Chrome and access to Second Life Marketplace. After purchase, click the delivered HUD in Second Life to open the license website and download the extension. Installing that supplied build does not require Node.js. Building from source requires Node.js 20 or newer.

## Install a supplied build

1. Download the extension from the license website opened by your HUD. If the download is an archive, extract it.
2. Find the folder containing `manifest.json`, `content.js`, `background.js`, `popup.html` and `studio.css`.
3. Open `chrome://extensions` in Chrome, enable **Developer mode**, then click **Load unpacked**.
4. Select that folder, not its parent or the archive. Look for the **Listora Studio** card.
5. Optionally pin the extension icon from Chrome's extensions menu.

## Build from source

1. Download the repository source and open a terminal in its root, beside `package.json`.
2. Run `npm install`, then `npm run build`.
3. Confirm that `dist/manifest.json` exists. Load the `dist` folder using the Chrome steps above.

On PowerShell, `npm.cmd install` and `npm.cmd run build` work if the shell blocks the `npm` script. A GitHub source archive does not include the ignored `dist` folder.

## Update an unpacked installation

Replace the build files with a newer supplied build, or build the newer source into `dist`. On `chrome://extensions`, click **Reload** for Listora Studio, then reload the Marketplace tab. The popup's **check for update** asks Chrome to check; it does not install repository source updates for an unpacked build.

Do not remove the extension as a routine update step. Templates, variable sets and publishing history are stored locally in that Chrome extension's storage.

## If Chrome rejects the folder

Check that the selected folder directly contains `manifest.json`. If you started with source, rebuild and select `dist`. See [troubleshooting](troubleshooting.md).

Need a license? The direct official product link is pending confirmation. Continue to [activation](license-activation.md) with an existing key.
