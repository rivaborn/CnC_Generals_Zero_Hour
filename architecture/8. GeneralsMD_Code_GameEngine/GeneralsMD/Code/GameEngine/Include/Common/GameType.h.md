# GeneralsMD/Code/GameEngine/Include/Common/GameType.h

## Purpose
Defines fundamental game types and enums used throughout the SAGE engine.

## Responsibilities
- Declares core identifier types (ObjectID, DrawableID, FormationID)
- Defines game state enums (TimeOfDay, Weather, Scorches)
- Specifies weapon slots and pathfinding layers
- Provides default world dimensions

## Key Types
- ObjectID (Enum): Generic object identifier
- DrawableID (Enum): Identifier for drawable game objects
- FormationID (Enum): Identifier for player formations
- TimeOfDay (Enum): Time periods (morning, afternoon, etc.)
- Weather (Enum): Weather conditions (normal, snowy)
- Scorches (Enum): Scorch mark types
- WeaponSlotType (Enum): Weapon slot categories
- PathfindLayerEnum (Enum): Pathfinding layers (ground, wall)

## Key Functions
None

## Globals
- TimeOfDayNames (char*): Array of time period names
- WeatherNames (char*): Array of weather condition names

## Dependencies
- BaseType.h (included)
- INI class (forward declared)
