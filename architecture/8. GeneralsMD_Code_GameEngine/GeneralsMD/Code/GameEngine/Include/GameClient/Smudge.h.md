# GeneralsMD/Code/GameEngine/Include/GameClient/Smudge.h

## Purpose
Defines classes for managing smudge effects (e.g., dirt, scorch marks) in the game world.

## Responsibilities
- Manages smudge objects and their rendering
- Tracks smudge sets and their usage
- Handles hardware support for smudge effects
- Provides memory pooling for smudge objects

## Key Types
- **Smudge (Class)**: Represents a single smudge effect with position, size, and vertices
- **SmudgeSet (Class)**: Manages a collection of smudges
- **SmudgeManager (Class)**: Central manager for all smudge effects
- **HardwareSmudgeSupport (Enum)**: Indicates hardware support status for smudge effects

## Key Functions
### SmudgeSet::addSmudgeToSet
- Purpose: Adds a new smudge to the set
- Calls: Not inferable

### SmudgeManager::init
- Purpose: Initializes the smudge manager
- Calls: Not inferable

### SmudgeManager::addSmudgeSet
- Purpose: Creates and adds a new smudge set
- Calls: Not inferable

## Globals
- **TheSmudgeManager (SmudgeManager*)**: Singleton instance of the smudge manager

## Dependencies
- `WW3D2/dllist.h` for doubly-linked list functionality
- `WWMATH/Vector2.h` and `WWMATH/Vector3.h` for vector math
- Uses `DLNodeClass` and `DLListClass` for object management
