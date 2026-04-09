# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLLadderScreen.cpp

## Purpose
Manages the WOL (Westwood Online) ladder screen UI, including initialization, input handling, and web browser integration.

## Responsibilities
- Initialize and shutdown the ladder screen UI
- Handle user input (keyboard/mouse) for the ladder screen
- Manage web browser window for ladder content
- Process window system messages for the ladder screen

## Key Types
- None

## Key Functions
### WOLLadderScreenInit
- Purpose: Initializes the ladder screen UI and web browser
- Calls: TheShell->showShellMap, TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, TheWebBrowser->createBrowserWindow

### WOLLadderScreenShutdown
- Purpose: Cleans up the ladder screen UI and web browser
- Calls: TheWebBrowser->closeBrowserWindow, TheShell->shutdownComplete

### WOLLadderScreenInput
- Purpose: Handles keyboard input for the ladder screen
- Calls: TheWindowManager->winSendSystemMsg

### WOLLadderScreenSystem
- Purpose: Processes system messages for the ladder screen
- Calls: TheShell->pop

## Globals
- parentWindowID (NameKeyType): ID for the parent window
- buttonBackID (NameKeyType): ID for the back button
- windowLadderID (NameKeyType): ID for the ladder window
- parentWindow (GameWindow*): Pointer to the parent window
- buttonBack (GameWindow*): Pointer to the back button
- windowLadder (GameWindow*): Pointer to the ladder window

## Dependencies
- PreRTS.h, Common/GameEngine.h, GameClient/WindowLayout.h, GameClient/Shell.h, GameClient/KeyDefs.h, GameClient/GameWindowManager.h, GameClient/MessageBox.h, GameNetwork/WOLBrowser/WebBrowser.h
- TheShell, TheNameKeyGenerator, TheWindowManager, TheWebBrowser
