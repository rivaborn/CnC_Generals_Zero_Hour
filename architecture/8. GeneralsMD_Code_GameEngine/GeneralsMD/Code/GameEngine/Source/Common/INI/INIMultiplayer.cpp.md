# GeneralsMD/Code/GameEngine/Source/Common/INI/INIMultiplayer.cpp

## Purpose
Parses multiplayer-related INI entries for the game, including settings and color definitions.

## Responsibilities
- Parses `MultiplayerSettings` and `MultiplayerColor` INI definitions
- Handles creation of `MultiplayerSettings` instance if none exists
- Manages multiplayer color definitions and starting money choices
- Validates override behavior for certain INI types

## Key Types
- **MultiplayerStartingMoneySettings (struct)**: Temporary data store for parsing starting money values and default flags

## Key Functions
### `parseMultiplayerSettingsDefinition`
- Purpose: Parses multiplayer settings from INI file
- Calls: `TheMultiplayerSettings->getFieldParse()`, `ini->initFromINI()`

### `parseMultiplayerColorDefinition`
- Purpose: Parses multiplayer color definitions from INI file
- Calls: `TheMultiplayerSettings->findMultiplayerColorDefinitionByName()`, `TheMultiplayerSettings->newMultiplayerColorDefinition()`, `ini->initFromINI()`, `multiplayerColorDefinition->getRGBValue()`, `multiplayerColorDefinition->getRGBNightValue()`

### `parseMultiplayerStartingMoneyChoiceDefinition`
- Purpose: Parses starting money choices from INI file
- Calls: `ini->initFromINI()`, `TheMultiplayerSettings->addStartingMoneyChoice()`

## Globals
- **TheMultiplayerSettings (MultiplayerSettings*)**: Global instance of multiplayer settings

## Dependencies
- `Common/INI.h`
- `Common/MultiplayerSettings.h`
- `PreRTS.h`
- `Money` class
- `MultiplayerSettings` class
- `MultiplayerColorDefinition` class
