# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/TempWeaponBonusHelper.h - Enhanced Analysis

## Architectural Role
This file defines a module for managing temporary weapon bonuses, fitting into the game's object-component system. It extends `ObjectHelper` to provide time-limited buff/debuff effects, likely used for power-ups or tactical advantages.

## Cross-References
### Incoming
- Game logic systems applying temporary bonuses (e.g., power-ups, AI scripts)
- Weapon damage calculation modules checking current bonus state

### Outgoing
- `ObjectHelper` base class for core functionality
- `ModuleData` for configuration
- Likely calls into weapon/attack systems to apply bonuses

## Design Patterns
- **Module Pattern**: Encapsulates bonus logic as a reusable component
- **State Pattern**: Tracks bonus state (`m_currentBonus`) and expiration (`m_frameToRemove`)
- **Memory Pool Pattern**: Uses `MEMORY_POOL_GLUE` for object allocation optimization
