# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/FirestormDynamicGeometryInfoUpdate.h - Enhanced Analysis

## Architectural Role
This file defines a specialized module for handling Firestorm-specific dynamic geometry effects, bridging the particle system rendering layer with game logic damage application. It extends the base `DynamicGeometryInfoUpdate` to add expansion-specific functionality like particle effects and scorch marks.

## Cross-References
### Incoming
- Likely called by the game's update loop or geometry system (e.g., `GameLogic/Module/DynamicGeometryInfoUpdate.cpp`)
- May be referenced in Firestorm-specific scenario scripts or rules

### Outgoing
- Uses `ParticleSystemTemplate` (likely from `W3D` rendering system)
- Depends on `FXList` (effect system)
- Calls into `DynamicGeometryInfoUpdate` base class methods
- Uses memory pool macros (engine-wide resource management)

## Design Patterns
- **Template Method**: Extends base `DynamicGeometryInfoUpdate` with Firestorm-specific behavior
- **Module Pattern**: Encapsulates Firestorm effects as a self-contained update module
- **Data-Driven Design**: Relies on `MultiIniFieldParse` for configuration (common in SAGE engine)
