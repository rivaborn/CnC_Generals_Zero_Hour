# GeneralsMD/Code/GameEngine/Include/GameLogic/Locomotor.h

## Purpose
Defines the Locomotor system for movement behavior in the game, including templates, physics interactions, and movement logic.

## Responsibilities
- Defines movement templates and behaviors for units
- Handles physics-based movement and positioning
- Manages movement states (braking, turning, climbing)
- Provides surface type masking for movement restrictions
- Stores and retrieves locomotor templates

## Key Types
- LocomotorTemplate (Class): Movement behavior template with physics properties
- Locomotor (Class): Runtime movement controller for objects
- LocomotorAppearance (Enum): Visual movement types (legs, wheels, treads, etc.)
- LocomotorBehaviorZ (Enum): Vertical movement behaviors
- LocoFlag (Enum): Movement state flags

## Key Functions
### locoUpdate_moveTowardsPosition
- Purpose: Move object toward a target position
- Calls: Appearance-specific movement handlers

### locoUpdate_maintainCurrentPosition
- Purpose: Maintain current position with physics
- Calls: Appearance-specific maintain handlers

### handleBehaviorZ
- Purpose: Handle vertical positioning behavior
- Calls: Physics calculations

## Globals
- TheLocomotorStore (LocomotorStore*): Global store for locomotor templates

## Dependencies
- Common/NameKeyGenerator.h
- Common/Override.h
- Common/Snapshot.h
- GameLogic/Damage.h
- GameLogic/LocomotorSet.h
