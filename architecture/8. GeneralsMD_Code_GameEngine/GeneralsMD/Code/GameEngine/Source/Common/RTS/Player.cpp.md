# GeneralsMD/Code/GameEngine/Source/Common/RTS/Player.cpp

## Purpose
Manages player state, resources, relations, and game logic for a single player in the RTS game.

## Responsibilities
- Handles player resources, upgrades, and production
- Manages player relations (alliances/enemies)
- Controls special powers and battle plans
- Manages vision and radar systems
- Handles player serialization/deserialization

## Key Types
- **ClosestKindOfData (Class)**: Helper for finding closest objects of a kind
- **PlayerObjectFindInfo (Class)**: Information for object search operations
- **TypeCountData (Class)**: Data for counting object types
- **VisionSpiedStruct (Class)**: Tracks spied vision information
- **Player (Class)**: Main player class (not shown in snippet)

## Key Functions
### findClosestKindOf
- Purpose: Finds the closest object matching a kind mask
- Calls: ThePartitionManager->getDistanceSquared

### doFindCommandCenter
- Purpose: Locates the player's command center
- Calls: Not inferable from snippet

### doFindSpecialPowerSourceObject
- Purpose: Finds objects that can use special powers
- Calls: Not inferable from snippet

### doCountSpecialPowersReady
- Purpose: Counts ready special powers for a player
- Calls: Not inferable from snippet

### sellBuildings
- Purpose: Handles selling of player buildings
- Calls: Not inferable from snippet

### countExisting
- Purpose: Counts existing objects of a type
- Calls: Not inferable from snippet

### doPowerDisable
- Purpose: Disables player powers
- Calls: Not inferable from snippet

### localApplyBattlePlanBonusesToObject
- Purpose: Applies battle plan bonuses to an object
- Calls: Not inferable from snippet

### iterator_setUnitsVisionSpied
- Purpose: Updates vision spied status for units
- Calls: Not inferable from snippet

## Globals
- **NEUTRAL_PLAYER_COLOR (const)**: Neutral player color value

## Dependencies
- Key includes: ActionManager.h, BuildAssistant.h, GameState.h, Player.h, Team.h, Object.h, Weapon.h, SpecialPower.h
- External symbols: ThePartitionManager, TheTeamFactory, newInstance, deleteInstance
