# GeneralsMD/Code/GameEngine/Include/Common/ActionManager.h - Enhanced Analysis

## Architectural Role
This file defines the central action validation subsystem, bridging UI input, network commands, and game logic. It ensures consistent behavior checks across client-side predictions and server-side validation.

## Cross-References
### Incoming
- **UI System**: Calls validation methods before executing commands
- **Network Layer**: Uses same methods to validate incoming commands
- **AI Subsystem**: Queries action feasibility for decision making
- **Command System**: Relies on `canFireWeapon`/`canDoSpecialPower` for execution gates

### Outgoing
- **Object System**: Checks object states and capabilities
- **Player System**: Validates player-specific permissions
- **SpecialPower/Weapon Systems**: References templates and slot types
- **Coord3D System**: Uses spatial coordinates for location-based checks

## Design Patterns
- **Facade Pattern**: Provides unified interface to complex validation logic scattered across object types
- **Strategy Pattern**: Different validation methods act as interchangeable strategies for different action types
- **Singleton Pattern**: Global `TheActionManager` instance ensures single validation authority (implied by global access)

*Not inferable*: Exact implementation of validation rules or how results are used in command execution flow.
