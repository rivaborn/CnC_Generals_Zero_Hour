# GeneralsMD/Code/GameEngine/Source/GameClient/MessageStream/MetaEvent.cpp

## Purpose
Handles translation of raw input events (keyboard/mouse) into game-specific meta-events and manages command mappings.

## Responsibilities
- Translates raw key/mouse messages into meta-events
- Manages command mappings via MetaMap
- Handles modifier key states and double-click detection
- Provides lookup utilities for message types

## Key Types
- **MetaMapRec (struct)**: Stores mapping between input events and game messages
- **MetaMap (class)**: Manages collection of MetaMapRec instances and parsing
- **MetaEventTranslator (class)**: Translates input messages into game commands

## Key Functions
### findGameMessageNameByType
- Purpose: Converts GameMessage::Type enum to human-readable string
- Calls: None

### translateGameMessage
- Purpose: Processes raw input messages and generates meta-events
- Calls: TheMessageStream->appendMessage, TheMessageStream->insertMessage, TheGameClient->getFrame, TheShell->isShellActive, TheGameLogic->getFrame

### parseMetaMap
- Purpose: Parses INI configuration for command mappings
- Calls: INI::initFromINI

## Globals
- **TheMetaMap (MetaMap*)**: Global instance of MetaMap
- **GameMessageMetaTypeNames (LookupListRec[])**: Array mapping message types to names
- **TheMetaMapFieldParseTable (FieldParse[])**: INI parsing rules for MetaMapRec

## Dependencies
- Common/INI.h, Common/MessageStream.h, GameClient/MetaEvent.h
- GameClient/GameClient.h, GameClient/KeyDefs.h, GameLogic/GameLogic.h
- Various other GameClient components for UI and input handling
