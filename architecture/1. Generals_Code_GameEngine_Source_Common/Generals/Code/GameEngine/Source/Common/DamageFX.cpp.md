# Generals/Code/GameEngine/Source/Common/DamageFX.cpp

## Purpose
This file contains the implementation for handling damage effects in the game, including parsing configuration data from INI files and managing different types of damage effects based on various conditions.

## Responsibilities
- Parsing damage effect configurations from INI files.
- Managing different types of damage effects (major and minor) based on damage amount and source veterancy level.
- Applying damage effects to objects in the game.

## Key Types
- `DamageFX`: Manages damage effects for different types and levels of damage.
- `DamageFXStore`: Stores and manages multiple `DamageFX` instances.

## Key Functions
### parseCommonStuff
- Purpose: Parses common settings for damage effects from INI files.
- Calls: `INI::scanIndexList`, `INI::parseDurationUnsignedInt`

### doDamageFX
- Purpose: Applies the appropriate damage effect to a victim object based on the type and amount of damage.
- Calls: `getDamageFXList`, `FXList::doFXObj`

### getDamageFXList
- Purpose: Retrieves the correct FX list (major or minor) based on the damage amount and source veterancy level.
- Calls: None

## Globals
- `TheDamageFXStore` (`DamageFXStore*`): Global instance of the DamageFX store.

## Dependencies
- Includes: `PreRTS.h`, `INI.h`, `ThingFactory.h`, `ThingTemplate.h`, `DamageFX.h`, `GameAudio.h`, `FXList.h`, `Damage.h`, `GameLogic.h`, `Object.h`, `GameClient.h`, `InGameUI.h`
- External symbols: `TheVeterancyNames`, `TheNameKeyGenerator`, `TheDamageNames`
