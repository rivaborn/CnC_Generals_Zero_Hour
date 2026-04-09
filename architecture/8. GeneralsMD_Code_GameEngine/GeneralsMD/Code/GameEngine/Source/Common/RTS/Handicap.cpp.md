# GeneralsMD/Code/GameEngine/Source/Common/RTS/Handicap.cpp

## Purpose
Manages handicap modifiers for game entities, allowing adjustments to build costs, build times, and other attributes based on configuration.

## Responsibilities
- Initializes handicap values
- Reads handicap data from configuration dictionaries
- Determines appropriate handicap type for a given thing template
- Provides handicap values for specific attributes

## Key Types
- `Handicap` (Class): Main class handling handicap logic
- `HandicapType` (Enum): Types of handicaps (BUILDCOST, BUILDTIME)
- `ThingType` (Enum): Categories of things (GENERIC, BUILDINGS)

## Key Functions
### `Handicap::init()`
- Purpose: Initializes all handicap values to 1.0
- Calls: None

### `Handicap::readFromDict()`
- Purpose: Loads handicap values from a configuration dictionary
- Calls: `Dict::getReal()`, `TheNameKeyGenerator->nameToKey()`

### `Handicap::getBestThingType()`
- Purpose: Determines the most specific thing type for a template
- Calls: `ThingTemplate::isKindOf()`

### `Handicap::getHandicap()`
- Purpose: Retrieves the handicap value for a specific attribute and template
- Calls: `getBestThingType()`

## Globals
- `m_handicaps[HANDICAP_TYPE_COUNT][THING_TYPE_COUNT]` (Real): 2D array storing handicap values

## Dependencies
- `PreRTS.h`, `Common/Handicap.h`, `Common/Player.h`, `Common/Dict.h`, `Common/ThingTemplate.h`
- `TheNameKeyGenerator` (external symbol)
- `KINDOF_STRUCTURE` (external constant)
