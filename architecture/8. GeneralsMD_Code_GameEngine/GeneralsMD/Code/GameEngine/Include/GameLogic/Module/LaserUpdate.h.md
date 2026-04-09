# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/LaserUpdate.h

## Purpose
Defines the `LaserUpdate` module for handling laser rendering and game control updates in the SAGE engine.

## Responsibilities
- Manages laser initialization, positioning, and rendering.
- Handles laser width scaling and decay effects.
- Updates laser start/end positions based on parent/target objects.
- Controls particle effects for muzzle flare and target impact.

## Key Types
- **LaserUpdateModuleData (Class)**: Holds module configuration (particle system names, punch-through scalar).
- **LaserUpdate (Class)**: Core module for laser updates, including position tracking and rendering control.
- **ParticleSystemID (Enum)**: Identifies particle effects used by the laser.

## Key Functions
### `initLaser`
- Purpose: Spawns the laser in the world with given start/end positions.
- Calls: Not inferable (implementation in .cpp).

### `clientUpdate`
- Purpose: Updates laser state per frame (position, width, decay).
- Calls: `updateStartPos`, `updateEndPos`.

### `updateStartPos` / `updateEndPos`
- Purpose: Recalculates laser start/end positions based on parent/target objects.
- Calls: Not inferable.

## Globals
- None.

## Dependencies
- `ClientUpdateModule.h` (base class).
- `Thing`, `Vector3`, `ParticleSystemID` (forward declarations).
- `AsciiString`, `Real`, `Bool`, `UnsignedInt` (primitives).
