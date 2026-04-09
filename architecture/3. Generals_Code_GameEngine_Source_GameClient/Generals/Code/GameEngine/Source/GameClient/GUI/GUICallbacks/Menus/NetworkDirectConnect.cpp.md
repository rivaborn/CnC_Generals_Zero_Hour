# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/Menus/NetworkDirectConnect.cpp

## Purpose
Handles the LAN direct connect menu UI and networking functionality in Command & Conquer Generals.

## Responsibilities
- Manages LAN game hosting/joining UI
- Handles player name and IP address management
- Interfaces with LANAPI for network operations
- Updates remote IP address list
- Manages menu initialization/shutdown

## Key Types
- **LANbuttonPushed (Bool)**: Tracks if LAN button was pressed
- **LANisShuttingDown (Bool)**: Tracks LAN shutdown state
- **isShuttingDown (Bool)**: Local shutdown flag
- **buttonPushed (Bool)**: Tracks button press state
- **NameKeyType (static)**: Window control IDs
- **GameWindow* (static)**: Pointers to UI controls

## Key Functions
### PopulateRemoteIPComboBox
- Purpose: Populates the remote IP combo box from user preferences
- Calls: GadgetComboBoxReset, GadgetComboBoxAddEntry, GadgetComboBoxSetSelectedPos

### UpdateRemoteIPList
- Purpose: Updates the list of remote IPs in user preferences
- Calls: GadgetComboBoxGetLength, GadgetComboBoxGetSelectedPos, GadgetComboBoxGetText

### HostDirectConnectGame
- Purpose: Initiates hosting a direct connect game
- Calls: TheLAN->RequestGameCreate, TheLAN->RequestSetName

### JoinDirectConnectGame
- Purpose: Joins a direct connect game
- Calls: TheLAN->RequestGameJoinDirectConnect, TheLAN->RequestSetName

### NetworkDirectConnectInit
- Purpose: Initializes the direct connect menu
- Calls: TheLAN->init, TheLAN->reset, PopulateRemoteIPComboBox

### NetworkDirectConnectShutdown
- Purpose: Shuts down the direct connect menu
- Calls: TheShell->reverseAnimatewindow, TheTransitionHandler->reverse

### NetworkDirectConnectInput
- Purpose: Handles keyboard input for the menu
- Calls: TheWindowManager->winSendSystemMsg

### NetworkDirectConnectSystem
- Purpose: Handles system messages for the menu
- Calls: GadgetTextEntryGetText, TheShell->pop

## Globals
- **LANbuttonPushed (Bool)**: Tracks LAN button state
- **LANisShuttingDown (Bool)**: Tracks shutdown state
- **isShuttingDown (Bool)**: Local shutdown flag
- **buttonPushed (Bool)**: Tracks button press state
- **buttonBackID/buttonHostID/buttonJoinID/editPlayerNameID/comboboxRemoteIPID/staticLocalIPID (NameKeyType)**: Control IDs
- **buttonBack/buttonHost/buttonJoin/editPlayerName/comboboxRemoteIP/staticLocalIP (GameWindow*)**: UI control pointers

## Dependencies
- GameSpy/peer/peer.h
- Common/QuotedPrintable.h
- GameClient/AnimateWindowManager.h
- GameClient/WindowLayout.h
- GameClient/Gadget.h
- GameNetwork/IPEnumeration.h
- GameNetwork/LANAPI.h
- TheLAN (LANAPI singleton)
- TheShell, TheWindowManager, TheNameKeyGenerator, TheGameText, TheTransitionHandler
