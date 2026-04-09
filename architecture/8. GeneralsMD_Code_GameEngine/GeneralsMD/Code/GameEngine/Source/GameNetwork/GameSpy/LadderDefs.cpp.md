# GeneralsMD/Code/GameEngine/Source/GameNetwork/GameSpy/LadderDefs.cpp

## Purpose
Parses and manages ladder (ranked match) definitions for GameSpy integration in Command & Conquer Generals.

## Responsibilities
- Parses ladder configuration from GameSpy MOTD (Message of the Day)
- Loads local ladder definitions from INI files
- Provides lookup methods for ladders by address/port or index
- Manages three types of ladders: standard, special, and local

## Key Types
- **LadderInfo (struct)**: Contains ladder configuration (name, address, port, factions, maps, etc.)
- **LadderList (class)**: Manages collections of ladders and provides lookup functionality
- **None**: No enums or other key types

## Key Functions
### parseLadder
- Purpose: Parses a single ladder definition from raw text
- Calls: `MultiByteToWideCharSingleLine`, `ThePlayerTemplateStore->getAllSideStrings`, `TheGameState->portableMapPathToRealMapPath`, `TheMapCache->findMap`, `TheGameSpyConfig->getQMMaps`

### LadderList::findLadder
- Purpose: Finds a ladder by address and port
- Calls: None (iterates through ladder lists)

### LadderList::findLadderByIndex
- Purpose: Finds a ladder by its index
- Calls: None (iterates through ladder lists)

### LadderList::loadLocalLadders
- Purpose: Loads ladder definitions from local INI files
- Calls: `TheFileSystem->getFileListInDirectory`, `checkLadder`

## Globals
- **TheLadderList (LadderList*)**: Global instance of the ladder list manager

## Dependencies
- Key includes: `PreRTS.h`, `ThreadUtils.h`, `LadderDefs.h`, `PeerDefs.h`, `GSConfig.h`, `GameState.h`, `File.h`, `FileSystem.h`, `PlayerTemplate.h`, `GameText.h`, `MapUtil.h`
- External symbols: `TheGameSpyConfig`, `ThePlayerTemplateStore`, `TheGameState`, `TheMapCache`, `TheGlobalData`, `TheFileSystem`, `TheGameText`
