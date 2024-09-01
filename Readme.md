# Chrome Extension SF

## Description

Chrome Extension SF is a powerful browser extension designed to enhance user experience and automate certain tasks on specific websites. This extension is particularly useful for managing cases and activities within a Salesforce-like environment.

## Features

-   Automatically opens relevant links
-   Navigates to the activity tab
-   Selects the text post option
-   Automates image and attachment uploads
-   Provides keyboard shortcuts for closing cases
-   Enhances vendor information viewing on certain platforms

## Installation

1. Clone this repository or download the ZIP file.
2. Open Chrome and navigate to `chrome://extensions/`.
3. Enable "Developer mode" in the top right corner.
4. Click "Load unpacked" and select the directory containing the extension files.

## Usage

The extension automatically runs on the following sites:

1. Salesforce-like case management system (URL to be added in manifest.json)
2. Vendor information platform (URL to be added in manifest.json)

### Salesforce-like Environment

-   The extension will automatically:

    -   Open relevant links
    -   Navigate to the activity tab
    -   Select the text post option
    -   Prepare for image and attachment uploads

-   Keyboard Shortcuts:
    -   Press 'W' to close the current case

### Vendor Information Platform

-   The extension will automatically:

    -   Open the "More Info" popup for vendor information

-   Keyboard Shortcuts:
    -   Press 'Alt' to close the current window

## Configuration

To configure the extension for your specific sites, modify the `manifest.json` file:

1. Open `manifest.json`
2. In the `content_scripts` section, add the appropriate URLs:

```json
"content_scripts": [
    {
        "matches": [
            "https://your-salesforce-like-site.com/*"
        ],
        "js": ["content.js"]
    },
    {
        "matches": [
            "https://your-vendor-info-site.com/*"
        ],
        "js": ["panda.js"]
    }
]
```

Replace `https://your-salesforce-like-site.com/*` and `https://your-vendor-info-site.com/*` with the actual URLs where you want the extension to run.

## Development

The extension consists of the following key files:

-   `manifest.json`: Extension configuration
-   `content.js`: Main content script for Salesforce-like environment
-   `panda.js`: Content script for vendor information platform
-   `background.js`: Background script (currently empty, can be used for future functionality)

To modify the extension's behavior, edit the respective JavaScript files.

## License

This Chrome extension is free to use and modify for any purpose.

## Disclaimer

This extension is not officially associated with Salesforce or any other platform. Use it at your own risk and ensure compliance with the terms of service of the websites you're using it on.
