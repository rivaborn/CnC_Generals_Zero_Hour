# Generals/Code/GameEngine/Source/GameLogic/Object/ObjectCreationList.cpp

## Purpose
This file defines the `ObjectCreationList` class and related classes for creating game objects, handling weapon firing, attacks, payload delivery, and debris generation.

## Responsibilities
- Manage object creation lists.
- Parse INI files to configure object creation behaviors.
- Handle various object creation nuggets like firing weapons, attacking, delivering payloads, and creating debris.

## Key Types
- **FireWeaponNugget (Class)**: Handles weapon firing.
- **AttackNugget (Class)**: Manages attacks with specified parameters.
- **DeliverPayloadNugget (Class)**: Controls payload delivery with formation logic.
- **ApplyRandomForceNugget (Class)**: Applies random forces to objects.
- **GenericObjectCreationNugget (Class)**: Base class for generic object creation.

## Key Functions
### adjustVector
- Purpose: Adjusts a vector based on a matrix transformation.
- Calls: `Rotate_Vector`

### calcRandomForce
- Purpose: Calculates a random force within specified parameters.
- Calls: None

### parseFrictionPerSec
- Purpose: Parses friction per second from an INI file.
- Calls: None

## Globals
- **TheObjectCreationListStore (ObjectCreationListStore*)**: Stores object creation lists.
- **DebrisDispositionNames (const char*[])**: Names for debris dispositions.
- **debrisModelNamesGlobalHack (std::vector<AsciiString>)**: Global hack for debris model names.
- **TheObjectCreationListFieldParse (const FieldParse[])**: Field parsing definitions.

## Dependencies
- Key includes:
  - `Common/AudioEventRTS.h`
  - `Common/DrawModule.h`
  - `Common/GlobalData.h`
  - `Common/INI.h`
  - `GameLogic/ObjectCreationList.h`
  - `GameLogic/ThingTemplate.h`
  - `GameLogic/ThingFactory.h`
  - `GameLogic/WeaponSet.h`
  - `GameLogic/ScriptEngine.h`
  - `GameLogic/PartitionManager.h`
