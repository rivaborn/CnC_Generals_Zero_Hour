# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HelixContain.h - Enhanced Analysis

## Architectural Role
This file defines the `HelixContain` module, a specialized transport container used for units like the Helix (GLA's portable missile launcher). It extends the `TransportContain` base class, integrating with the game's containment system for units/structures, damage handling, and UI feedback.

## Cross-References
### Incoming
- **GameLogic/Module/TransportContain.h**: Base class inheritance
- **GameLogic/Module/ContainModuleInterface.h**: Used for container pips logic
- **GameLogic/Object.h**: For `Object` and `Thing` interactions
- **GameLogic/Player.h**: For capture event handling
- **GameLogic/DamageInfo.h**: For damage state callbacks
- **GameLogic/Module/ModuleData.h**: For module data inheritance

### Outgoing
- **GameLogic/Module/DrawModule.h**: Friend access for rider draw order
- **GameLogic/Module/OpenContain.h**: Interface for open container behavior
- **GameLogic/Module/HealContain.h**: For healing container checks
- **GameLogic/Module/TunnelContain.h**: For tunnel container checks
- **GameLogic/Module/PortableStructure.h**: For portable structure handling

## Design Patterns
- **Template Method**: Overrides like `onContaining`/`onRemoving` suggest a framework where base class defines containment flow, but derived classes customize behavior.
- **Strategy**: `isValidContainerFor` and `isPassengerAllowedToFire` imply containment rules are encapsulated as policies.
- **Observer**: Damage/capture callbacks (`onBodyDamageStateChange`, `onCapture`) follow event-driven design.
