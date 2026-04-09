# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/ExperienceTracker.cpp

## Purpose
Manages experience points and veterancy levels for game objects.

## Responsibilities
- Tracks experience points and veterancy levels
- Handles experience distribution to other objects
- Manages level-up logic and callbacks
- Serializes experience data for save/load

## Key Types
- `ExperienceTracker` (Class): Manages experience and veterancy for an object
- `VeterancyLevel` (Enum): Represents veterancy levels (REGULAR, VETERAN, etc.)

## Key Functions
### `addExperiencePoints`
- Purpose: Adds experience points and handles level-up logic
- Calls: `getTemplate()`, `getExperienceRequired()`, `onVeterancyLevelChanged()`

### `setExperienceAndLevel`
- Purpose: Directly sets experience and level, triggering callbacks if changed
- Calls: `getTemplate()`, `getExperienceRequired()`, `onVeterancyLevelChanged()`

### `xfer`
- Purpose: Serializes experience data for save/load
- Calls: `xferVersion()`, `xferUser()`, `xferInt()`, `xferObjectID()`, `xferReal()`

## Globals
- None

## Dependencies
- `Common/Xfer.h` (for serialization)
- `Common/ThingTemplate.h` (for object templates)
- `GameLogic/GameLogic.h` (for game state)
- `GameLogic/Object.h` (for parent object)
