<p align="center"> 
  <h3 align="center">VTOP Activity Chrome Extension</h3>
  <p align="center">
    A Chrome extension that keeps your VTOP session active by periodically sending background requests to prevent session timeouts.
    <br /> <br />
  </p>
</p>

---

<details open="open">
  <summary>Table of Contents</summary>
  <ol>
    <li><a href="#about">About</a></li>
    <li><a href="#built-with">Built With</a></li>
    <li><a href="#usage">Usage</a></li>
    <li><a href="#contributing">Contributing</a></li>
  </ol>
</details>

---

## About

The **VTOP Activity Chrome Extension** prevents your VTOP session from timing out by automatically sending requests in the background. It periodically opens a tab in the background, extracts the necessary CSRF token and session data, and sends a request to simulate user activity, all without interrupting your current browsing session.

### Features

- **Automatic Requests**: Periodically sends requests to keep the session active.
- **Background Script**: Works completely in the background requiring zero user interaction.
---

## Built With

- **JavaScript** - The primary programming language for the extension.
- **Chrome Extensions API** - Used for background scripts, alarms, and tab management.
- **Manifest V3** - The extension follows the Manifest V3 structure for Chrome extensions.

---

## Usage

### Setting Up the Extension:

1. **Download the ZIP file**:

   - Go to the [Releases](https://github.com/theg1239/VTOP-activity/releases) page of this repository.
   - Download the latest release `.zip` file.

2. **Extract the ZIP file**:

   - Extract the contents of the ZIP file to a folder on your computer.

3. **Load the extension into Chrome**:

   - Go to `chrome://extensions/` or `brave://extensions` depending on your browser.
   - Enable **Developer mode** (toggle in the top right corner).
   - Click on **Load unpacked** and select the folder where you extracted the extension files. 

4. **Run the extension**:

   Once installed, the extension will automatically keep your VTOP session active by sending background requests.

### Customizing the request interval:

You can modify the interval between requests by adjusting the `periodInMinutes` value in the `background.js` file:

```javascript
chrome.alarms.create('activityAlarm', {
    periodInMinutes: 10 // Adjust this value to change the interval
});

```


