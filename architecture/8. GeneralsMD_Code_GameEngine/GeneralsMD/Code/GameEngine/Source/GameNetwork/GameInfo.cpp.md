# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameInfo.cpp

## Purpose
Manages game session state, player slots, and network synchronization for multiplayer games.

## Responsibilities
- Maintains game session metadata (map, seed, player slots)
- Serializes/deserializes game state for network transfer
- Handles player slot management (human/AI/observer)
- Validates game setup parameters

## Key Types
- **GameInfo (Class)**: Central game session state container
- **GameSlot (Class)**: Represents individual player slots (human/AI/observer)
- **SlotState (Enum)**: Defines slot states (open/closed/player/AI levels)

## Key Functions
### `getSlotIndex`
- Purpose: Finds the index of a given GameSlot in TheGameInfo
- Calls: None

### `isSlotLocalAlly`
- Purpose: Determines if a slot belongs to the local player or their team
- Calls: `getSlotIndex`, `getConstSlot`, `getLocalSlotNum`

### `GameInfoToAsciiString`
- Purpose: Serializes GameInfo into a human-readable string format
- Calls: `grabHexInt`, `strtok_r` (via string parsing)

### `ParseAsciiStringToGameInfo`
- Purpose: Deserializes game info from string format
- Calls: `grabHexInt`, `strtok_r`, `atoi`, `ThePlayerTemplateStore` methods

## Globals
- **TheGameInfo (GameInfo*)**: Global game session state instance
- **slotListID (Int)**: Used during string parsing (line 897)

## Dependencies
- Common: `CRCDebug`, `File`, `GameState`, `MultiplayerSettings`, `PlayerTemplate`, `Xfer`
- GameClient: `GameText`, `MapUtil`
- GameNetwork: `FileTransfer`, `GameInfo`, `LANAPI`, `LANAPICallbacks`
- External: `strtok_r`, `FirewallHelperClass`
