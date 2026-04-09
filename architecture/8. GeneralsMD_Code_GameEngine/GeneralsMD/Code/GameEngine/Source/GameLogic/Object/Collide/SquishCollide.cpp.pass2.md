# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/SquishCollide.cpp - Enhanced Analysis

## Architectural Role
This file implements the collision detection logic for "squish" damage, a key gameplay mechanic where larger units (e.g., tanks) can crush smaller units (e.g., infantry). It integrates with the physics, AI, and damage systems to determine when and how squish damage should be applied.

## Cross-References
### Incoming
- **PhysicsUpdate**: Calls into this module when collision events occur
- **AIUpdate**: Uses AI state to determine if crushing should be ignored (e.g., during hijacking)
- **SpecialAbilityUpdate**: Checks for special abilities (e.g., TNT placement) that should prevent crushing

### Outgoing
- **Damage**: Applies damage via `DamageInfo` when squish occurs
- **PartitionManager**: Uses spatial partitioning for collision detection (`geomCollidesWithGeom`)
- **Object/Thing**: Accesses object properties (position, orientation, physics, AI)

## Design Patterns
- **Module Pattern**: Extends `CollideModule` to encapsulate squish-specific collision logic
- **Strategy Pattern**: Implements collision handling as a strategy that can be swapped or extended
- **Observer Pattern**: Reacts to collision events triggered by the physics system
