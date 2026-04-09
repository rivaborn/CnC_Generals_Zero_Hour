# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/DynamicGeometryInfoUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements a module for dynamically animating an object's collision geometry (height and radii) over time, supporting interpolation, reversal, and networking synchronization. It bridges the game logic layer with the rendering system by modifying `GeometryInfo` properties that affect both collision and visual representation.

## Cross-References
### Incoming
- `FirestormDynamicGeometryInfoUpdate.cpp` (specialized subclass) calls base class methods (`update`, `xfer`, `buildFieldParse`)

### Outgoing
- Calls `UpdateModule` base class methods (inheritance)
- Uses `INI` parsing infrastructure for module data configuration
- Interacts with `Object` to modify geometry via `setGeometryInfo`
- Leverages `Xfer` system for networking serialization

## Design Patterns
- **Module Pattern**: Encapsulates geometry animation as a reusable, configurable module
- **Interpolation**: Linear interpolation between initial/final values for smooth transitions
- **State Machine**: Tracks update phases (delay, active, reversed, finished) for lifecycle management

*Not inferable*: No clear use of Observer, Factory, or Visitor patterns.
