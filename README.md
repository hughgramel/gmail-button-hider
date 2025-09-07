# Gmail Button Hider

A simple Chrome extension that hides the "Gmail" button from Google's homepage and search results, helping you reduce email checking habits by adding friction to accessing Gmail.

## Features

- 🚫 Hides the Gmail button from Google's interface
- 🎯 Targets the correct Gmail button element (class `gb_X`)
- ⚡ Lightweight and fast - minimal performance impact
- 🔒 No data collection or external requests
- 🛡️ Works with Manifest V3 (latest Chrome extension standard)

## Installation

### Method 1: Load as Unpacked Extension (Recommended for Development)

1. **Download or Clone this Repository**
   ```bash
   git clone https://github.com/yourusername/gmail-button-hider.git
   cd gmail-button-hider
   ```

2. **Open Chrome Extensions Page**
   - Open Chrome and navigate to `chrome://extensions/`
   - Or go to Chrome Menu → More Tools → Extensions

3. **Enable Developer Mode**
   - Toggle the "Developer mode" switch in the top-right corner

4. **Load the Extension**
   - Click "Load unpacked"
   - Select the `gmail-button-hider` folder
   - The extension should now appear in your extensions list

5. **Verify Installation**
   - Visit [google.com](https://google.com)
   - The Gmail button should no longer be visible in the top navigation

### Method 2: Install from Chrome Web Store (Coming Soon)

*This extension will be published to the Chrome Web Store for easier installation.*

## How It Works

The extension uses two methods to hide the Gmail button:

1. **CSS Hiding**: Uses `display: none !important` to immediately hide the button
2. **JavaScript Fallback**: Additional JavaScript ensures the button stays hidden even if dynamically loaded

The extension targets the Gmail button with class `gb_X` which is the current class used by Google's interface.

## Files Structure

```
gmail-button-hider/
├── manifest.json    # Extension configuration
├── content.js       # JavaScript logic
├── styles.css       # CSS to hide the button
└── README.md        # This file
```

## Technical Details

- **Manifest Version**: 3 (latest Chrome extension standard)
- **Target Sites**: All Google domains (`*://*.google.com/*`)
- **Execution**: Runs at `document_start` for immediate effect
- **Permissions**: No special permissions required

## Troubleshooting

### The Gmail button is still visible

1. **Refresh the page** - The extension should take effect immediately
2. **Check if the extension is enabled** - Go to `chrome://extensions/` and ensure it's toggled on
3. **Google may have changed the button class** - If Google updates their interface, the button class might change from `gb_X` to something else

### Extension not working after Chrome update

Google occasionally changes their interface. If the extension stops working:

1. Check if Google has changed the Gmail button's CSS class
2. Update the selectors in `styles.css` and `content.js` if needed
3. Reload the extension in `chrome://extensions/`

## Contributing

Contributions are welcome! If you notice the extension isn't working:

1. Fork the repository
2. Update the CSS selectors to match Google's current interface
3. Test the changes
4. Submit a pull request

## License

This project is open source and available under the [MIT License](LICENSE).

## Why This Extension?

Email can be a significant source of distraction and stress. By hiding the Gmail button from Google's interface, this extension adds a small amount of friction to checking email, helping you:

- Reduce compulsive email checking
- Stay focused on your current tasks
- Break the habit of constantly switching to email
- Maintain better work-life balance

The extension doesn't block access to Gmail entirely - you can still access it directly via `gmail.com` or bookmark it. It simply removes the convenient shortcut from Google's homepage.

## Support

If you encounter any issues or have suggestions for improvements, please:

1. Check the [Issues](https://github.com/yourusername/gmail-button-hider/issues) page
2. Create a new issue with details about the problem
3. Include your Chrome version and any error messages

---

**Note**: This extension is not affiliated with Google or Gmail. It's an independent tool designed to help users manage their email habits.