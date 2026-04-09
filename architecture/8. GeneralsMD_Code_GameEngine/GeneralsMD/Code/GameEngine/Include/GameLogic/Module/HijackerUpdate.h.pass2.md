# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/HijackerUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the behavior module for the hijacker unit's vehicle attachment system, bridging the game logic layer with the W3D rendering pipeline via bone attachment. It handles state transitions between hijacker and passenger modes, critical for the game's unique unit mechanics.

## Cross-References
### Incoming
- **UnitTemplateSystem**: Likely instantiates this module via INI parsing
- **Thing/Object classes**: Call `update()` during game loop
- **DieModuleInterface**: Potentially called when vehicle is destroyed

### Outgoing
- **UpdateModule base class**: Inherits core update behavior
- **W3D rendering system**: Uses bone attachment via `m_attachToBone`
- **Parachute system**: References parachute asset via `m_parachuteName`

## Design Patterns
- **Module Pattern**: Encapsulates hijacker-specific behavior as a reusable component
- **Data-Driven Design**: Configuration via INI fields (`buildFieldParse`)
- **State Machine**: Implicit state handling (vehicle attached/detached)
