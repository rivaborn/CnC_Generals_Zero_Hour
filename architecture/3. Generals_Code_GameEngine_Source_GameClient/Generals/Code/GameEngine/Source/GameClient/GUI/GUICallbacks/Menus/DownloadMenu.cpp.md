# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/DownloadMenu.cpp

## Purpose
Handles the patch download UI, progress tracking, and user interactions during file downloads.

## Responsibilities
- Manages download progress UI elements (progress bar, text labels)
- Handles download success/error callbacks
- Processes user input (cancel button, ESC key)
- Updates time remaining and download status

## Key Types
- **DownloadManagerMunkee (Class)**: Custom download manager with callbacks for progress, errors, and completion
- **None**: No other classes/structs/enums defined

## Key Functions
### closeDownloadWindow
- Purpose: Closes the download window and cleans up resources
- Calls: `runShutdown`, `destroyWindows`, `deleteInstance`, `winSetFocus`

### errorCallback
- Purpose: Handles download errors by showing a message and closing the window
- Calls: `HandleCanceledDownload`, `closeDownloadWindow`

### successQuitCallback
- Purpose: Handles successful downloads requiring game restart
- Calls: `setQuitting`, `closeDownloadWindow`, `appendMessage`

### successNoQuitCallback
- Purpose: Handles successful downloads without requiring restart
- Calls: `HandleCanceledDownload`, `closeDownloadWindow`

### DownloadMenuInit
- Purpose: Initializes the download menu UI and creates the download manager
- Calls: `nameToKey`, `winGetWindowFromId`, `NEW`

### DownloadMenuUpdate
- Purpose: Updates the time remaining display periodically
- Calls: `time`, `GadgetStaticTextGetText`, `GadgetStaticTextSetText`

### DownloadMenuInput
- Purpose: Handles keyboard input (ESC key) for the download window
- Calls: `winSendSystemMsg`

### DownloadMenuSystem
- Purpose: Handles window system messages (creation, destruction, focus, selection)
- Calls: `HandleCanceledDownload`, `closeDownloadWindow`

## Globals
- **buttonCancelID (NameKeyType)**: ID for the cancel button
- **staticTextSizeID (NameKeyType)**: ID for the size text label
- **staticTextTimeID (NameKeyType)**: ID for the time remaining label
- **staticTextFileID (NameKeyType)**: ID for the filename label
- **staticTextStatusID (NameKeyType)**: ID for the status label
- **progressBarMunkeeID (NameKeyType)**: ID for the progress bar
- **staticTextSize (GameWindow)**: Pointer to the size text label
- **staticTextTime (GameWindow)**: Pointer to the time remaining label
- **staticTextFile (GameWindow)**: Pointer to the filename label
- **staticTextStatus (GameWindow)**: Pointer to the status label
- **progressBarMunkee
