# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/OCLSpecialPower.cpp

## Purpose
Handles special powers that create objects via ObjectCreationLists (OCLs) in the game.

## Responsibilities
- Manages OCL-based special power execution
- Determines object creation locations based on configuration
- Handles upgrades and science-based OCL selection
- Adjusts creation positions for passability when needed

## Key Types
- OCLSpecialPowerModuleData (Class): Stores module data including default OCL, upgrades, creation location type, and reference object name
- OCLSpecialPower (Class): Implements the special power logic for object creation
- (anonymous enum) (Enum): Defines creation location types (CREATE_AT_EDGE_NEAR_SOURCE, CREATE_AT_EDGE_NEAR_TARGET, etc.)
- CREATE_ABOVE_LOCATION_HEIGHT (Enum): Height constant for above-location creation
- MAX_ADJUST_RADIUS (Enum): Maximum radius for position adjustment

## Key Functions
### parseOCLUpgradePair
- Purpose: Parses upgrade OCL pairs from INI files
- Calls: INI::parseScience, INI::parseObjectCreationList

### OCLSpecialPower::findOCL
- Purpose: Finds the appropriate OCL based on player's science
- Calls: getOCLSpecialPowerModuleData, getObject, getControllingPlayer, hasScience

### OCLSpecialPower::doSpecialPowerAtLocation
- Purpose: Executes the special power at a specific location
- Calls: getObject, isDisabled, getOCLSpecialPowerModuleData, findOCL, ThePartitionManager->findPositionAround, TheTerrainLogic->findClosestEdgePoint, TheTerrainLogic->findFarthestEdgePoint, ObjectCreationList::create

### OCLSpecialPower::doSpecialPowerAtObject
- Purpose: Executes the special power targeting an object
- Calls: getObject, isDisabled, doSpecialPowerAtLocation

### OCLSpecialPower::doSpecialPower
- Purpose: Executes the special power at the object's position
- Calls: getObject, isDisabled, SpecialPowerModule::doSpecialPowerAtLocation, findOCL, ObjectCreationList::create

## Globals
- TheOCLCreateLocTypeNames (const char*): Array of creation location type names for INI parsing

## Dependencies
- PreRTS.h, Common/Player.h, Common/RandomValue.h, Common/ThingFactory.h, Common/Xfer.h, GameLogic/Object.h, GameLogic/ObjectCreationList.h, GameLogic/PartitionManager.h, GameLogic/TerrainLogic.h, GameLogic/Module/OCLSpecialPower.h
