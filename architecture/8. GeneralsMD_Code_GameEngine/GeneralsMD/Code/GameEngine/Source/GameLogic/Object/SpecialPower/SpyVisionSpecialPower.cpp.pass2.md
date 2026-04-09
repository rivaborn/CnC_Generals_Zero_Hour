# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/SpecialPower/SpyVisionSpecialPower.cpp - Enhanced Analysis

## Architectural Role
This file implements the SpyVision special power, a game mechanic that grants vision of enemy players based on captured units. It extends the base SpecialPowerModule to add captured-unit-dependent duration logic, bridging the special power system with the containment and vision update subsystems.

## Cross-References
### Incoming
- **SpecialPowerModule**: Base class that calls into this module's overridden methods
- **ContainModuleInterface**: Used to query captured unit count for duration calculation
- **SpyVisionUpdate**: Activated by this module to apply vision effects

### Outgoing
- **SpecialPowerModule**: Base class methods (doSpecialPower, crc, xfer, loadPostProcess)
- **ContainModule**: Accessed via getContain() to determine captured unit count
- **SpyVisionUpdate**: Found via findUpdateModule and activated via activateSpyVision

## Design Patterns
- **Template Method**: Extends base SpecialPowerModule with overridden doSpecialPower
- **Strategy**: Duration calculation varies based on captured units (dynamic behavior)
- **Dependency Injection**: Module data injected via constructor (SpyVisionSpecialPowerModuleData)

*Not inferable*: Exact observer pattern usage with SpyVisionUpdate not clear from this file alone.
