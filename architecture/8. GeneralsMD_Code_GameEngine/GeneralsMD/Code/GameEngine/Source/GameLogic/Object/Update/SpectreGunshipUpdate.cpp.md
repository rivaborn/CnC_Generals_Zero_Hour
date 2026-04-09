# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/SpectreGunshipUpdate.cpp

## Purpose
Handles weapon firing logic for the Spectre Gunship special power in Command & Conquer Generals Zero Hour.

## Responsibilities
- Manages gunship orbiting, targeting, and weapon firing behavior
- Controls gattling gun and howitzer weapon systems
- Handles visual effects and audio for the gunship
- Manages target acquisition and area-of-effect decals
- Coordinates with AI and containment systems

## Key Types
- **SpectreGunshipUpdateModuleData (Class)**: Stores configuration data for the gunship module
- **PartitionFilterLiveMapEnemies (Class)**: Filters objects to find live enemies on the map
- **GunshipStatus (Enum)**: Tracks gunship state (idle, inserting, orbiting, departing)

## Key Functions
### `initiateIntentToDoSpecialPower`
- Purpose: Initializes the gunship special power activation
- Calls: `setLogicalStatus`, `friend_enableAfterburners`, `createRadiusDecal`

### `update`
- Purpose: Maintains gunship behavior and weapon firing logic
- Calls: `iterateObjectsInRange`, `aiAttackObject`, `createAndFireTempWeapon`

### `friend_enableAfterburners`
- Purpose: Controls afterburner visuals and audio
- Calls: `setModelConditionState`, `addAudioEvent`

### `cleanUp`
- Purpose: Cleans up resources when gunship departs
- Calls: `destroyObject`, `clear`

## Globals
- **zero (Real)**: Constant value 0.0f

## Dependencies
- Key includes: `GameLogic/Module/SpectreGunshipUpdate.h`, `PartitionManager.h`, `Weapon.h`
- External symbols: `TheGameLogic`, `ThePartitionManager`, `TheWeaponStore`, `TheAudio`
