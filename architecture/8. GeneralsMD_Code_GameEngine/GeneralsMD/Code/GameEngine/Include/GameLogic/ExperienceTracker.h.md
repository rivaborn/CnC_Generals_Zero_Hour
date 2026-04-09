# GeneralsMD/Code/GameEngine/Include/GameLogic/ExperienceTracker.h

## Purpose
Header defining the `ExperienceTracker` class, which manages experience points and veterancy levels for game objects.

## Responsibilities
- Tracks experience points and veterancy levels for game objects.
- Handles experience gain, level progression, and feedback.
- Supports experience sinks (delegating experience to other objects).
- Provides serialization via `Snapshot` interface.

## Key Types
- **ExperienceTracker (Class)**: Manages experience and veterancy for an object.
- **VeterancyLevel (Type)**: Represents veterancy levels (external).
- **Object (Class)**: Parent object reference (external).
- **Snapshot (Interface)**: Serialization interface (external).

## Key Functions
### `ExperienceTracker(Object *parent)`
- Purpose: Constructs an `ExperienceTracker` for a given parent object.
- Calls: None (constructor).

### `addExperiencePoints(Int experienceGain, Bool canScaleForBonus)`
- Purpose: Adds experience points to the tracker, optionally scaling by bonus.
- Calls: Not inferable (implementation in `.cpp`).

### `gainExpForLevel(Int levelsToGain, Bool canScaleForBonus)`
- Purpose: Grants experience to advance by specified levels.
- Calls: Not inferable.

### `setExperienceSink(ObjectID sink)`
- Purpose: Sets the target object for delegated experience.
- Calls: None.

### `crc(Xfer *xfer)`
- Purpose: Computes CRC for snapshot serialization.
- Calls: `Xfer` methods.

### `xfer(Xfer *xfer)`
- Purpose: Serializes/deserializes tracker state.
- Calls: `Xfer` methods.

## Globals
- **None**

## Dependencies
- `Common/GameCommon.h`, `Common/GameType.h`, `Common/GameMemory.h`, `Common/Snapshot.h`
- `Object`,
