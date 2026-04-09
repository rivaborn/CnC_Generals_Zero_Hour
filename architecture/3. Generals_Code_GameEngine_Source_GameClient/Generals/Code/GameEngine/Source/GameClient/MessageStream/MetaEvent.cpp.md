# Generals/Code/GameEngine/Source/GameClient/MessageStream/MetaEvent.cpp

## Purpose
Handles translation of raw input events (keyboard/mouse) into game-specific meta-events.

## Responsibilities
- Maps key/mouse inputs to game commands via `MetaMap`
- Manages modifier states (Ctrl/Shift/Alt) for input combinations
- Handles double-click detection for mouse buttons
- Provides lookup utilities for game message types
- Parses INI configuration for key bindings

## Key Types
- `MetaMap` (Class): Manages key-to-command mappings
- `MetaMapRec` (Struct): Represents a single key-command mapping
- `MetaEventTranslator` (Class): Core translator handling input events
- `GameMessage::Type` (Enum): Message type identifiers

## Key Functions
### `findGameMessageNameByType`
- Purpose: Converts a message type enum to its string name
- Calls: None

### `translateGameMessage`
- Purpose: Processes raw input messages and generates meta-events
- Calls: `TheMessageStream->appendMessage`, `TheMessageStream->insertMessage`, `TheGameClient->getFrame`, `TheShell->isShellActive`

### `parseMetaMap`
- Purpose: Parses INI configuration for key bindings
- Calls: `findGameMessageMetaType`, `getMetaMapRec`, `INI::initFromINI`

## Globals
- `TheMetaMap` (MetaMap*): Global instance of the meta map
- `GameMessageMetaTypeNames` (LookupListRec[]): Array mapping message types to names
- `TheMetaMapFieldParseTable` (FieldParse[]): INI parsing rules for meta map fields

## Dependencies
- `Common/INI.h`, `Common/MessageStream.h`, `Common/Player.h`
- `GameClient/MetaEvent.h`, `GameClient/GameClient.h`, `GameClient/KeyDefs.h`
- `GameLogic/GameLogic.h` (for frame access)
