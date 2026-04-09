# Generals/Code/GameEngine/Source/GameNetwork/GameInfo.cpp

## Purpose
Manages game session state, player slots, and network synchronization for multiplayer games.

## Responsibilities
- Maintains player slot information (state, color, team, etc.)
- Serializes/deserializes game state for network transfer
- Validates and parses game setup strings
- Handles CRC checks and map data integrity

## Key Types
- **GameSlot (Class)**: Represents a player slot with state, color, team, etc.
- **GameInfo (Class)**: Manages overall game session state and player slots
- **SkirmishGameInfo (Class)**: Extends GameInfo for skirmish-specific behavior
- **SlotState (Enum)**: Defines slot states (SLOT_PLAYER, SLOT_AI, etc.)

## Key Functions
### getSlotIndex
- Purpose: Finds the index of a given GameSlot in TheGameInfo.
- Calls: None

### isSlotLocalAlly
- Purpose: Determines if a slot belongs to the local player or their team.
- Calls: getSlotIndex, getLocalSlotNum, getConstSlot, getTeamNumber

### GameInfoToAsciiString
- Purpose: Serializes GameInfo into a human-readable string format.
- Calls: strtok_r, atoi, various GameSlot getters

### ParseAsciiStringToGameInfo
- Purpose: Parses a string back into GameInfo structure.
- Calls: strtok_r, atoi, GameSlot setters, TheMultiplayerSettings accessors

## Globals
- **TheGameInfo (GameInfo*)**: Global game info instance
- **slotListID (Int)**: Used during string parsing

## Dependencies
- Common/Xfer.h (serialization)
- GameNetwork/GameInfo.h (header)
- GameClient/GameText.h (text access)
- Common/MultiplayerSettings.h (settings)
- Common/PlayerTemplate.h (player templates)
