# Generals/Code/GameEngine/Source/GameNetwork/GameSpy/Chat.cpp

## Purpose
Handles GameSpy chat functionality, including message sending, receiving, and display with color coding.

## Responsibilities
- Parses chat color definitions from INI files
- Sends and receives chat messages (public/private)
- Manages chat window registration and text display
- Applies language filtering and audio cues for messages

## Key Types
- `GameSpyColorFieldParse` (FieldParse[]): INI field definitions for chat colors
- `GameSpyColor` (Color[GSCOLOR_MAX]): Array of predefined chat colors
- `GameSpyInfo` (class): Core GameSpy chat functionality (partial)

## Key Functions
### `INI::parseOnlineChatColorDefinition`
- Purpose: Parses chat color definitions from INI file
- Calls: `INI::initFromINI`

### `GameSpyInfo::sendChat`
- Purpose: Sends chat messages (public/private) to GameSpy server
- Calls: `TheGameSpyPeerMessageQueue->addRequest`, `GadgetListBoxGetSelected`, `GadgetListBoxGetText`

### `GameSpyInfo::addChat`
- Purpose: Displays incoming chat messages with appropriate formatting/colors
- Calls: `TheAudio->addAudioEvent`, `TheLanguageFilter->filterLine`, `addText`, `GadgetListBoxSetItemData`

### `GameSpyInfo::addText`
- Purpose: Adds text to chat windows with color coding
- Calls: `TheAudio->addAudioEvent`, `TheInGameUI->message`, `GadgetListBoxAddEntryText`, `GadgetListBoxSetItemData`

### `GameSpyInfo::registerTextWindow`
- Purpose: Registers a chat window for text display
- Calls: None

### `GameSpyInfo::unregisterTextWindow`
- Purpose: Unregisters a chat window
- Calls: None

## Globals
- `GameSpyColorFieldParse` (FieldParse[]): Field definitions for INI parsing
- `GameSpyColor` (Color[GSCOLOR_MAX]): Predefined chat color values

## Dependencies
- `INI.h`, `AudioEventRTS.h`, `GameText.h`, `GadgetListBox.h`, `LanguageFilter.h`, `GameWindowManager.h`, `PeerDefsImplementation.h`, `PeerThread.h`, `InGameUI.h`
- `TheGameSpyPeerMessageQueue`, `TheGameSpyInfo`, `TheAudio`, `TheInGameUI`, `TheLanguageFilter`, `TheGlobalData`
