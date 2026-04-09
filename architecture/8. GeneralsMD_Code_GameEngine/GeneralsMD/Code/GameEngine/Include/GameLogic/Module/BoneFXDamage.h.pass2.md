# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/BoneFXDamage.h - Enhanced Analysis

## Architectural Role
This file defines a damage module specifically for bone animation effects, bridging the game logic layer with the W3D rendering system. It extends the generic damage handling framework to support visual damage states on skeletal models.

## Cross-References
### Incoming
- Likely called by the W3D animation system when damage occurs to objects with skeletal animations
- Probably referenced by the game object creation system during module initialization

### Outgoing
- Inherits from DamageModule, calling its base class methods
- Uses BodyDamageType enum from BodyModule for state tracking
- Interfaces with the memory management system via custom memory pool macros

## Design Patterns
- **Template Method Pattern**: Provides empty virtual methods (onDamage, onHealing) for subclasses to override
- **Memory Pool Pattern**: Uses custom memory allocation macros for performance optimization
- **Module Registration Pattern**: Implements standard module macros for engine integration

*Not inferable*: Exact relationship with W3D bone animation system not visible in header.
