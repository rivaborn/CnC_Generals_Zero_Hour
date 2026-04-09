# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLLadderScreen.cpp

## Purpose
Manages the WOL (Westwood Online) ladder screen UI, including initialization, input handling, and web browser integration.

## Responsibilities
- Initialize and shutdown the ladder screen UI
- Handle user input (keyboard/mouse) for the ladder screen
- Manage web browser window for ladder content
- Process window system messages (focus, selection)
- Control shell navigation (popping screens)

## Key Types
None

## Key Functions
### WOLLadderScreenInit
- Purpose: Initializes the ladder screen UI and web browser
- Calls: TheShell->showShellMap, TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, TheWebBrowser->createBrowserWindow, layout->hide, TheWindowManager->winSetFocus

### WOLLadderScreenShutdown
- Purpose: Cleans up ladder screen resources and closes web browser
- Calls: TheWebBrowser->closeBrowserWindow, layout->hide, TheShell->shutdownComplete

### WOLLadderScreenInput
- Purpose: Handles keyboard input for the ladder screen
- Calls: TheWindowManager->winSendSystemMsg

### WOLLadderScreenSystem
- Purpose: Processes window system messages for the ladder screen
- Calls: TheShell->pop

## Globals
- parentWindowID (NameKeyType): ID for parent window
- buttonBackID (NameKeyType): ID for back button
- windowLadderID (NameKeyType): ID for ladder window
- parentWindow (GameWindow*): Pointer to parent window
- buttonBack (GameWindow*): Pointer to back button
- windowLadder (GameWindow*): Pointer to ladder window

## Dependencies
- PreRTS.h, GameEngine.h, WindowLayout.h, Shell.h, KeyDefs.h, GameWindowManager.h, MessageBox.h, WebBrowser.h
- TheShell, TheNameKeyGenerator, TheWindowManager, TheWebBrowser
