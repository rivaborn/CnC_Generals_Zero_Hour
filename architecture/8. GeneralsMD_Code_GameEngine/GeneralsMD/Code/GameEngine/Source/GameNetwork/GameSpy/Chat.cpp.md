# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameSpy/Chat.cpp

## Purpose
Handles GameSpy chat functionality, including message sending, receiving, and display with color coding.

## Responsibilities
- Parses chat color definitions from INI files
- Sends and receives chat messages (public/private)
- Manages chat message display with appropriate styling
- Handles player list interactions for private messaging
- Registers/unregisters text windows for chat output

## Key Types
- `GameSpyColorFieldParse` (FieldParse[]): INI field definitions for chat colors
- `GameSpyColor` (Color[GSCOLOR_MAX]): Array of predefined chat colors
- `GameSpyInfo` (class): Main GameSpy chat handler class

## Key Functions
### `INI::parseOnlineChatColorDefinition`
- Purpose: Parses chat color definitions from INI file
- Calls: `INI::initFromINI`

### `GameSpyInfo::sendChat`
- Purpose: Sends chat messages (public or private) to GameSpy server
- Calls: `TheGameSpyPeerMessageQueue->addRequest`, `GadgetListBoxGetSelected`, `GadgetListBoxGetText`

### `GameSpyInfo::addChat`
- Purpose: Displays incoming chat messages with appropriate styling
- Calls: `addText`, `GadgetListBoxSetItemData`, `TheLanguageFilter->filterLine`, `TheAudio->addAudioEvent`

### `GameSpyInfo::addText`
- Purpose: Adds formatted text to chat window with color
- Calls: `GadgetListBoxAddEntryText`, `GadgetListBoxSetItemData`, `TheInGameUI->message`, `TheAudio->addAudioEvent`

### `GameSpyInfo::registerTextWindow`
- Purpose: Registers a GameWindow for chat output
- Calls: None

### `GameSpyInfo::unregisterTextWindow`
- Purpose: Unregisters a GameWindow from chat output
- Calls: None

## Globals
- `GameSpyColorFieldParse` (FieldParse[]): Field definitions for INI parsing
- `GameSpyColor` (Color[GSCOLOR_MAX]): Predefined chat color values

## Dependencies
- `INI.h`, `GameText.h`, `GadgetListBox.h`, `LanguageFilter.h`, `GameWindowManager.h`
- `PeerDefsImplementation.h`, `PeerThread.h`, `InGameUI.h`
- `AudioEventRTS`, `TheGameSpyPeerMessageQueue`, `TheLanguageFilter`, `TheInGameUI`, `TheAudio`
