# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/PhysicsUpdate.h

## Purpose
Defines the physics behavior module for rigid body physics simulation in the game engine.

## Responsibilities
- Simulates rigid body physics (forces, friction, gravity, collisions)
- Manages object velocity, acceleration, and rotation
- Handles collision responses and overlap detection
- Provides interface for applying external forces and shocks
- Controls object movement constraints (ground sticking, falling, bouncing)

## Key Types
- **ObjectID (Enum)**: Identifier for game objects.
- **PhysicsTurningType (Enum)**: Turning direction (-1, 0, 1).
- **PhysicsBehaviorModuleData (Class)**: Configuration data for physics behavior.
- **PhysicsBehavior (Class)**: Main physics simulation module.
- **PhysicsFlagsType (Enum)**: Bit flags for physics state (e.g., airborne, stunned).

## Key Functions
### `applyForce`
- Purpose: Applies a force at the object's center of mass.
- Calls: Updates acceleration and velocity.

### `applyFrictionalForces`
- Purpose: Applies friction based on object state and surface.
- Calls: Uses friction parameters from module data.

### `handleBounce`
- Purpose: Handles collision response and bouncing logic.
- Calls: Plays bounce sounds, applies bounce forces.

### `update`
- Purpose: Main physics update loop (called per frame).
- Calls: `applyGravitationalForces`, `applyFrictionalForces`, `handleBounce`.

### `onCollide`
- Purpose: Handles collision events with other objects.
- Calls: Applies collision forces, checks for damage.

## Globals
- **TheAudio (GameAudio)**: Used for playing bounce sounds.

## Dependencies
- `Common/AudioEventRTS.h`, `Common/GameAudio.h`
- `GameLogic/Module/BehaviorModule.h`, `GameLogic/Module/UpdateModule.h`, `GameLogic/Module/CollideModule.h`
- `Coord3D`, `Real`, `Bool`, `Int`, `UnsignedInt` (from engine core).
