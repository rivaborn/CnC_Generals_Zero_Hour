# Generals/Code/GameEngine/Source/GameLogic/Object/Body/HighlanderBody.cpp

## Purpose
This file implements the `HighlanderBody` class, which handles damage logic for a game object that cannot be destroyed by normal damage but can be destroyed by "Unresistable" damage.

## Responsibilities
- Handles damage application with special rules.
- Manages CRC and Xfer operations for serialization.
- Extends base class functionality.

## Key Types
- `HighlanderBody` (Class): Inherits from `ActiveBody`, handles special damage logic.
- None

## Key Functions
### HighlanderBody::attemptDamage
- Purpose: Adjusts damage amount to prevent death unless it's "Unresistable" damage.
- Calls:
  - `min`
  - `getHealth`
  - `ActiveBody::attemptDamage`

### HighlanderBody::crc
- Purpose: Handles CRC serialization.
- Calls:
  - `ActiveBody::crc`

### HighlanderBody::xfer
- Purpose: Handles Xfer (serialization) with versioning.
- Calls:
  - `XferVersion`
  - `ActiveBody::xfer`

### HighlanderBody::loadPostProcess
- Purpose: Post-processing after loading.
- Calls:
  - `ActiveBody::loadPostProcess`

## Globals
- None

## Dependencies
- Key includes and external symbols used but not defined here:
  - `PreRTS.h`
  - `Common/Xfer.h`
  - `GameLogic/Module/HighlanderBody.h`
