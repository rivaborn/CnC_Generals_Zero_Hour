# GeneralsMD/Code/GameEngine/Source/GameNetwork/LANGameInfo.cpp

## Purpose
Manages LAN game session information, including player slots, game state, and network synchronization.

## Responsibilities
- Maintains LAN game slot data (players, state, timing)
- Handles game list display and selection
- Serializes/deserializes game options via string parsing
- Tracks local player status and game hosting

## Key Types
- **LANGameInfo (Class)**: Central manager for LAN game state
- **LANGameSlot (Class)**: Represents individual player slots in a game
- **TheLANGameInfo (Global)**: Singleton instance of LANGameInfo

## Key Functions
### LANDisplayGameList
- Purpose: Populates a UI listbox with active LAN games
- Calls: GadgetListBoxGetSelected, GadgetListBoxReset, GadgetListBoxAddEntryText, GadgetListBoxSetItemData, GadgetListBoxSetSelected, HideGameInfoWindow

### GenerateGameOptionsString
- Purpose: Serializes current game settings to a string
- Calls: GameInfoToAsciiString

### ParseGameOptionsString
- Purpose: Deserializes game settings from a string and updates game state
- Calls: ParseAsciiStringToGameInfo, TheLAN->RequestHasMap, lanUpdateSlotList, updateGameOptions

## Globals
- **TheLANGameInfo (LANGameInfo*)**: Singleton instance of LANGameInfo

## Dependencies
- GameClient headers (GameInfoWindow, GameText, GadgetListBox)
- GameNetwork headers (LANGameInfo, LANAPICallbacks)
- Common/MultiplayerSettings.h
- strtok_r.h
- External symbols: TheLAN, GameInfoToAsciiString, ParseAsciiStringToGameInfo, lanUpdateSlotList, updateGameOptions, LANEnableStartButton
