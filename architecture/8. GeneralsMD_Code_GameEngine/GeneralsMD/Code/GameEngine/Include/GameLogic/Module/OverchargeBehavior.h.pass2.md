# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/OverchargeBehavior.h - Enhanced Analysis

## Architectural Role
This file defines the overcharge power system, a key gameplay mechanic where structures temporarily boost power output at the cost of health. It integrates with the module system, damage handling, and update loop, showing how power mechanics are modularized in the SAGE engine.

## Cross-References
### Incoming
- **Power Management**: Likely called by power grid logic to enable/disable overcharge states.
- **UI/Command System**: Used when players issue overcharge commands via hotkeys or context menus.
- **Damage System**: Triggered during damage events to adjust overcharge behavior.

### Outgoing
- **UpdateModule**: Inherits update logic for periodic health drain.
- **DamageModuleInterface**: Implements damage handling to prevent overcharge when health is low.
- **Thing/Player Systems**: Interacts with object ownership and capture events.

## Design Patterns
- **Module Pattern**: Encapsulates overcharge as a reusable behavior module.
- **Interface Segregation**: Provides `OverchargeBehaviorInterface` for clean external control.
- **Strategy-like Configuration**: Uses `OverchargeBehaviorModuleData` for runtime-configured parameters.
