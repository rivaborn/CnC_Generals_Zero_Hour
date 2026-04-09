# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/WOLLocaleSelectPopup.cpp

## Purpose
Handles the WOL (Westwood Online) locale selection popup UI in the game.

## Responsibilities
- Initializes and populates the locale selection listbox
- Processes user input for locale selection
- Updates player locale preferences and GameSpy data
- Manages popup window lifecycle (show/hide)

## Key Types
- None

## Key Functions
### WOLLocaleSelectInit
- Purpose: Initializes the locale selection popup and populates the listbox with available locales
- Calls: TheNameKeyGenerator->nameToKey, TheWindowManager->winGetWindowFromId, GadgetListBoxAddEntryText, GadgetListBoxSetSelected, TheWindowManager->winSetFocus, TheWindowManager->winSetModal

### WOLLocaleSelectShutdown
- Purpose: Cleans up and hides the locale selection popup
- Calls: layout->hide, TheShell->shutdownComplete

### WOLLocaleSelectInput
- Purpose: Handles keyboard input for the locale selection popup
- Calls: None

### WOLLocaleSelectSystem
- Purpose: Processes system messages for the locale selection popup, including selection confirmation
- Calls: GadgetListBoxGetSelected, TheGameSpyPSMessageQueue->addRequest, GameSpyCloseOverlay, cPref.write, TheGameSpyPSMessageQueue->findPlayerStatsByID, TheGameSpyPSMessageQueue->trackPlayerStats, TheGameSpyInfo->getCachedLocalPlayerStats, TheGameSpyInfo->setCachedLocalPlayerStats, TheGameSpyPSMessageQueue->addResponse, CheckReOpenPlayerInfo

## Globals
- parentLocaleSelectID (NameKeyType): ID for the parent locale select window
- buttonOkID (NameKeyType): ID for the OK button
- listboxLocaleID (NameKeyType): ID for the locale listbox
- parentLocaleSelect (GameWindow*): Pointer to the parent locale select window
- buttonOk (GameWindow*): Pointer to the OK button
- listboxLocale (GameWindow*): Pointer to the locale listbox

## Dependencies
- GameClient/GameText.h
- Common/CustomMatchPreferences.h
- Common/GameEngine.h
- Common/GameSpyMiscPreferences.h
- GameClient/WindowLayout.h
- GameClient/Gadget.h
- GameClient/Shell.h
- GameClient/KeyDefs.h
- GameClient/GameWindowManager.h
- GameClient/GadgetListBox.h
- Common/GlobalData.h
- GameNetwork/GameSpyOverlay.h
- GameNetwork/GameSpy/PeerDefs.h
- GameNetwork/GameSpy/PeerThread.h
- GameNetwork/GameSpy/PersistentStorageDefs.h
- GameNetwork/GameSpy/P
