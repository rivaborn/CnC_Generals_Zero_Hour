# GeneralsMD/Code/GameEngine/Include/GameLogic/LocomotorSet.h

## Purpose
Defines the LocomotorSet class and related types for managing movement capabilities of game entities across different surface types.

## Responsibilities
- Manages a collection of Locomotor objects
- Tracks valid surface types for movement
- Handles serialization/deserialization for save games
- Provides lookup for appropriate Locomotor based on surface type

## Key Types
- Locomotor (Class): Not inferable (forward declaration)
- LocomotorTemplate (Class): Not inferable (forward declaration)
- LocomotorSurfaceType (Enum): Bitmask flags for surface types (ground, water, cliff, air, rubble)
- LocomotorSurfaceTypeMask (Class): Typedef for Int, used as bitmask for surface types
- LocomotorVector (Class): Typedef for std::vector<Locomotor*>
- LocomotorSet (Class): Manages a set of locomotors and their valid surfaces

## Key Functions
### LocomotorSet::crc
- Purpose: Calculate CRC for snapshot serialization
- Calls: Not inferable

### LocomotorSet::xfer
- Purpose: Handle Xfer serialization
- Calls: Not inferable

### LocomotorSet::loadPostProcess
- Purpose: Post-processing after loading
- Calls: Not inferable

### LocomotorSet::addLocomotor
- Purpose: Add a new Locomotor to the set
- Calls: Not inferable

### LocomotorSet::findLocomotor
- Purpose: Find a Locomotor matching the given surface type mask
- Calls: Not inferable

### LocomotorSet::xferSelfAndCurLocoPtr
- Purpose: Transfer both the LocomotorSet and current Locomotor pointer
- Calls: Not inferable

## Globals
- NO_SURFACES (LocomotorSurfaceTypeMask): Zero mask
