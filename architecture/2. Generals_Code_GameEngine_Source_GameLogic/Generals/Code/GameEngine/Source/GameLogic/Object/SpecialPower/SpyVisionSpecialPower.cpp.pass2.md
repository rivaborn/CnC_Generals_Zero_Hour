# Generals/Code/GameEngine/Source/GameLogic/Object/SpecialPower/SpyVisionSpecialPower.cpp - Enhanced Analysis

## Architectural Role
This file is integral to the game's special power system, specifically handling the "Spy Vision" ability. It extends the base `SpecialPowerModule` class to provide specialized functionality for spying on enemy vision, incorporating duration calculations based on captured units and integrating with other modules like `ContainModule` and `SpyVisionUpdate`.

## Cross-References
### Incoming
- Not inferable.

### Outgoing
- **GameLogic/Module/SpecialPowerModule.h**: Calls base class methods (`doSpecialPower`, `crc`, `xfer`, `loadPostProcess`).
- **GameLogic/Module/ContainModule.h**: Retrieves captured unit count.
- **GameLogic/Module/SpyVisionUpdate.h**: Activates the spy vision effect.

## Design Patterns
- **Inheritance**: The class extends `SpecialPowerModule`, demonstrating polymorphic behavior and code reuse.
- **Configuration Management**: Uses a struct (`SpyVisionSpecialPowerModuleData`) to manage configuration data, adhering to a structured approach for settings management.
- **State Management**: Manages the state of the special power through methods like `doSpecialPower` and integrates with other modules for effect activation.
