# Generals/Code/GameEngine/Source/GameClient/Terrain/TerrainRoads.cpp

## Purpose
Manages terrain road and bridge descriptions, including parsing configuration data and maintaining collections of road types.

## Responsibilities
- Parses INI configuration for road/bridge properties
- Manages collections of road and bridge types
- Provides lookup functionality for road/bridge types
- Handles damage state transitions for bridges

## Key Types
- **TerrainRoadType (class)**: Represents a road or bridge type with properties like texture, width, and damage states
- **TerrainRoadCollection (class)**: Manages collections of road and bridge types
- **FieldParse (struct)**: Used for INI parsing field definitions

## Key Functions
### parseTransitionToOCL
- Purpose: Parses transition effects for bridge damage/repair states
- Calls: INI methods (getNextSubToken, scanIndexList, scanInt)

### parseTransitionToFX
- Purpose: Parses FX transition effects for bridge damage/repair states
- Calls: INI methods (getNextSubToken, scanIndexList, scanInt)

### findRoad
- Purpose: Searches for a road by name in the road list
- Calls: None

### newRoad
- Purpose: Creates a new road type with default values
- Calls: findRoad, newInstance

### newBridge
- Purpose: Creates a new bridge type with default values
- Calls: findBridge, newInstance

## Globals
- **TheTerrainRoads (TerrainRoadCollection*)**: Global instance of the terrain road collection

## Dependencies
- Common/INI.h (for INI parsing)
- GameClient/TerrainRoads.h (header)
- PreRTS.h (engine precompiled header)
- Uses BodyDamageType enum and related constants
