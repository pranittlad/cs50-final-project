# YouTube Video Bookmarking Chrome Extension

## Overview
This project is a Chrome Extension that enhances YouTube by allowing users to bookmark specific timestamps in videos. With features like saving, viewing, playing, and deleting bookmarks, this extension improves video navigation and makes revisiting key moments easier.

---

## Features
- **Bookmark Timestamp**: Save specific timestamps in YouTube videos with a custom description.
- **Persistent Storage**: Bookmarks are saved using Chrome's sync storage for easy access across devices.
- **View Saved Bookmarks**: Access all bookmarks via the popup interface.
- **Play Bookmark**: Instantly jump to a saved timestamp with a single click.
- **Delete Bookmark**: Remove bookmarks directly from the popup.

---

## Technologies Used
- **JavaScript**: Core programming language for logic and interactivity.
- **HTML/CSS**: Used for popup interface and styling.
- **Chrome Extension APIs**: For managing tabs, injecting scripts, and using sync storage.
- **Chrome Sync Storage**: Ensures bookmarks persist across devices if Chrome sync is enabled.

---

## File Structure
| File               | Description                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| **background.js**  | Handles tab-related events and communicates video data to the content script. |
| **contentScript.js** | Injected into YouTube pages to handle bookmarking functionality.           |
| **popup.js**       | Manages the popup interface, including displaying, playing, and deleting bookmarks. |
| **popup.css**      | Styles the popup interface for a user-friendly experience.                  |
| **utils.js**       | Provides utility functions like fetching the active tab URL.                |

---

## How It Works

1. **Detect YouTube Video Pages**:
   - The `background.js` script monitors browser tabs and identifies when a YouTube video page is loaded.
   - Sends the video ID to the content script.

2. **Inject Bookmark Button**:
   - The `contentScript.js` script adds a custom bookmark button to YouTube's player controls.
   - Clicking the button saves the current timestamp and description as a bookmark.

3. **Popup Interface**:
   - The `popup.js` script displays all saved bookmarks in a clean, styled interface.
   - Users can:
     - **Play**: Jump to a specific timestamp.
     - **Delete**: Remove bookmarks directly from the popup.

4. **Persistent Bookmarks**:
   - All bookmarks are stored using Chrome's sync storage, making them available across devices if logged into Chrome.

---


