# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Locomotor.cpp

## Purpose
Handles movement and locomotion behavior for game objects, including physics, pathfinding, and surface interactions.

## Responsibilities
- Manages locomotion templates and behaviors (e.g., thrust, wheels, wings)
- Calculates movement forces, turning, and braking
- Handles surface-specific movement logic
- Provides utility functions for vector math and orientation

## Key Types
- **LocomotorTemplate (Class)**: Defines movement parameters (speed, acceleration, turning rates)
- **Locomotor (Class)**: Runtime locomotion behavior controller
- **LocomotorSet (Class)**: Collection of locomotors for an object
- **LocomotorSurfaceTypeMask (Enum)**: Surface types (e.g., road, water)

## Key Functions
### `calcSlowDownDist`
- Purpose: Calculates distance needed to slow down from current to desired speed.
- Calls: None

### `tryToRotateVector3D`
- Purpose: Rotates a vector toward a target direction within a max angle.
- Calls: `Vector3::Dot_Product`, `Vector3::Cross_Product`, `Matrix3D::Rotate_Vector`

### `calcDirectionToApplyThrust`
- Purpose: Computes optimal thrust direction to reach a target position.
- Calls: `Vector3::Length2`, `Vector3::Normalize`

### `maintainCurrentPositionThrust`
- Purpose: Keeps an object stationary using thrust-based locomotion.
- Calls: `moveTowardsPositionThrust`

### `maintainCurrentPositionWings`
- Purpose: Circles around a target position for winged units.
- Calls: `moveTowardsPositionWings`, `calcMinTurnRadius`

## Globals
- **DONUT_TIME_DELAY_SECONDS (Real)**: Delay before donut-shaped movement.
- **DONUT_DISTANCE (Real)**: Distance threshold for donut movement.
- **TheLocomotorStore (LocomotorStore*)**: Global store for locomotion templates.
- **BIGNUM (Real)**: Large value for default limits.
- **TheLocomotorPriorityNames (char**)**: Priority names for locomotion.

## Dependencies
- **Common/INI.h**: INI file parsing
- **GameLogic/GameLogic.h**: Core game logic
- **GameLogic/Object.h**: Game object definitions
- **GameLogic/PhysicsUpdate.h**: Physics behavior
- **W3D Matrix/Vector math**: For 3D transformations
