# Generals/Code/GameEngine/Source/GameNetwork/GameSpyOverlay.cpp

## Purpose
Manages GameSpy overlay windows and message boxes in the game UI.

## Responsibilities
- Creates/destroys overlay windows (e.g., buddy list, map select)
- Handles message boxes (OK, OK/Cancel, Yes/No)
- Manages overlay visibility and focus
- Handles buddy list reconnection logic

## Key Types
- `GSOverlayType` (Enum): overlay window types (player info, map select, etc.)
- `WindowLayout` (Class): overlay window layout container
- `GameWinMsgBoxFunc` (Type): callback function for message box actions

## Key Functions
### `GameSpyOpenOverlay`
- Purpose: Opens a specified overlay window.
- Calls: `ClearGSMessageBoxes`, `MessageBoxOk`, `MessageBoxOkCancel`, `MessageBoxYesNo`, `TheWindowManager->winCreateLayout`

### `GameSpyCloseOverlay`
- Purpose: Closes a specified overlay window.
- Calls: `overlayLayouts[overlay]->runShutdown`, `overlayLayouts[overlay]->destroyWindows`, `overlayLayouts[overlay]->deleteInstance`

### `GameSpyUpdateOverlays`
- Purpose: Updates all open overlay windows.
- Calls: `overlayLayouts[i]->runUpdate`

### `GSMessageBoxOk`
- Purpose: Displays an OK message box.
- Calls: `ClearGSMessageBoxes`, `MessageBoxOk`

### `GSMessageBoxOkCancel`
- Purpose: Displays an OK/Cancel message box.
- Calls: `ClearGSMessageBoxes`, `MessageBoxOkCancel`

## Globals
- `messageBoxWindow` (GameWindow*): tracks active message box window
- `okFunc`/`cancelFunc` (GameWinMsgBoxFunc): callbacks for message box actions
- `reOpenPlayerInfoFlag` (Bool): flag to reopen player info overlay
- `gsOverlays` (const char*): array of overlay window file paths
- `overlayLayouts` (WindowLayout*): array of overlay window layouts

## Dependencies
- `GameClient/MessageBox.h`, `GameClient/GameText.h`, `GameNetwork/GameSpy/BuddyThread.h`
- `TheWindowManager`, `TheGameText`, `TheGameSpyBuddyMessageQueue`, `TheAudio`
- `SignalUIInteraction`, `SignalUIInteraction`, `AudioEventRTS`
