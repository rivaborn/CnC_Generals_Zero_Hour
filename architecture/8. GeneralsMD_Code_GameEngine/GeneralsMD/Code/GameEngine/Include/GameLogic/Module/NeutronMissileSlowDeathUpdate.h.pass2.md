# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/NeutronMissileSlowDeathUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the behavior module for the neutron missile superweapon's post-impact effects, integrating with the game's damage system and visual effects pipeline. It extends the `SlowDeathBehavior` base class to implement timed blast sequences and scorch mark placement.

## Cross-References
### Incoming
- **GameLogic/Module/SlowDeathBehavior.h**: Base class providing core slow death functionality.
- **FXList**: Used for visual effects, likely defined in the rendering subsystem.
- **MultiIniFieldParse**: Configuration parsing infrastructure for module data.

### Outgoing
- **Damage System**: `doBlast` likely interacts with the game's damage application logic.
- **Physics System**: `pushForceMag` suggests integration with the physics engine for object displacement.
- **Visual Effects**: `doScorchBlast` and `m_fxList` imply calls into the W3D rendering system.

## Design Patterns
- **Template Method**: `update` orchestrates the blast sequence, with `doBlast` and `doScorchBlast` as concrete steps.
- **State Tracking**: Uses `m_completedBlasts` and `m_completedScorchBlasts` arrays to manage phase progression.
- **Data-Driven Design**: `BlastInfo` struct and `buildFieldParse` enable configuration via external files (INI).
