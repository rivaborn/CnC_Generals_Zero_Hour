# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameSpyOverlay.cpp

## Purpose
Manages GameSpy overlay windows and message boxes in the game UI.

## Responsibilities
- Handles creation/destruction of overlay windows (e.g., buddy list, map select)
- Manages modal message boxes (OK, OK/Cancel, Yes/No)
- Tracks overlay state and ensures proper visibility during screen transitions
- Coordinates with GameSpy buddy system for connection handling

## Key Types
- `GSOverlayType` (Enum): Identifies different overlay types (player info, map select, etc.)
- `WindowLayout` (Class): Represents overlay window layouts loaded from .wnd files
- `GameWinMsgBoxFunc` (Type): Callback function type for message box responses

## Key Functions
### `GameSpyOpenOverlay`
- Purpose: Opens a specified GameSpy overlay window.
- Calls: `ClearGSMessageBoxes`, `BuddyRequest` queue operations, `TheWindowManager->winCreateLayout`

### `GameSpyCloseOverlay`
- Purpose: Closes and cleans up a specified overlay window.
- Calls: `overlayLayouts[overlay]->runShutdown`, `overlayLayouts[overlay]->destroyWindows`

### `GSMessageBoxOk`
- Purpose: Displays an OK-only message box with a callback.
- Calls: `ClearGSMessageBoxes`, `MessageBoxOk`

### `RaiseGSMessageBox`
- Purpose: Ensures message boxes remain visible during screen transitions.
- Calls: `raiseOverlays`, `messageBoxWindow->winBringToTop`

## Globals
- `gsOverlays` (const char*): Array mapping overlay types to .wnd file paths
- `overlayLayouts` (WindowLayout*): Array tracking loaded overlay window layouts
- `messageBoxWindow` (GameWindow*): Currently active message box window
- `reOpenPlayerInfoFlag` (Bool): Flag to reopen player info overlay

## Dependencies
- `GameClient/MessageBox.h` (MessageBoxOk, MessageBoxOkCancel, MessageBoxYesNo)
- `GameClient/GameText.h` (TheGameText for localized strings)
- `GameNetwork/GameSpy/BuddyThread.h` (TheGameSpyBuddyMessageQueue)
- `Common/AudioEventRTS.h` (AudioEventRTS for sound effects)
