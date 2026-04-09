# Generals/Code/GameEngine/Source/Common/RTS/Handicap.cpp

## Purpose
This file implements the `Handicap` class, which manages game handicaps for different types of things (e.g., buildings, units) and handicap types (e.g., build cost, build time).

## Responsibilities
- Initialize handicaps to default values.
- Read handicap settings from a dictionary.
- Determine the best thing type based on a template.
- Retrieve handicap values for specific types.

## Key Types
- `Handicap` (Class): Manages game handicaps.
- `ThingType` (Enum): Represents different types of things (e.g., buildings, units).
- `HandicapType` (Enum): Represents different types of handicaps (e.g., build cost, build time).

## Key Functions
### Handicap::init
- Purpose: Initializes all handicap values to 1.0f.
- Calls: None

### Handicap::readFromDict
- Purpose: Reads handicap settings from a dictionary and applies them.
- Calls: `AsciiString::clear`, `AsciiString::set`, `AsciiString::concat`, `TheNameKeyGenerator->nameToKey`, `Dict::getReal`

### Handicap::getBestThingType
- Purpose: Determines the best thing type based on a template.
- Calls: `ThingTemplate::isKindOf`

### Handicap::getHandicap
- Purpose: Retrieves the handicap value for a specific type and template.
- Calls: `Handicap::getBestThingType`

## Globals
- None

## Dependencies
- Key includes:
  - "Common/Handicap.h"
  - "Common/Player.h"
  - "Common/Dict.h"
  - "Common/ThingTemplate.h"
