# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/MobNexusContain.h - Enhanced Analysis

## Architectural Role
This file defines the containment system for mobile units (e.g., transports) in the game, bridging UI, AI, and physics systems. It implements the `TransportPassengerInterface` to manage unit loading/unloading, door reservations, and capacity checks.

## Cross-References
### Incoming
- **UI System**: Calls `isValidContainerFor` to validate unit loading
- **AI System**: Uses `tryToEvacuate` for tactical unloading
- **Physics System**: Relies on `update` for movement synchronization

### Outgoing
- **INI Parsing**: Uses `MultiIniFieldParse` for configuration
- **Object System**: Interacts with `Object` and `ThingTemplate` for containment logic
- **Module System**: Inherits from `OpenContain` and `TransportPassengerInterface`

## Design Patterns
- **Strategy Pattern**: `isValidContainerFor` encapsulates container validation logic
- **Observer Pattern**: `onContaining`/`onRemoving` notify other systems of state changes
- **Template Method**: `update` provides a hook for per-frame containment logic
