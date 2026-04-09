# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Damage/BoneFXDamage.cpp - Enhanced Analysis

## Architectural Role
This file implements a damage module that bridges damage logic with skeletal animation effects, enabling visual feedback for damaged units. It enforces a strict dependency on BoneFXUpdate, demonstrating the engine's modular damage system architecture.

## Cross-References
### Incoming
- Damage system core (calls `DamageModule` methods)
- Object lifecycle system (triggers `onObjectCreated`)
- Damage event system (calls `onBodyDamageStateChange`)

### Outgoing
- BoneFXUpdate module (for animation state changes)
- Xfer system (for serialization)
- Object module system (via `findUpdateModule`)

## Design Patterns
- **Dependency Injection**: Requires BoneFXUpdate via constructor/module lookup
- **Observer Pattern**: Notifies BoneFXUpdate of damage state changes
- **Template Method**: Extends base class methods (crc, xfer, loadPostProcess)
