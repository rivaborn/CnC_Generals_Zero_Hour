# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Contain/HelixContain.cpp - Enhanced Analysis

## Architectural Role
This file implements the containment logic for Helix units (e.g., Gattling Cannon), managing portable structures and payload handling. It extends the base `TransportContain` class to handle Helix-specific behaviors like stealth propagation and weapon bonuses.

## Cross-References
### Incoming
- Called by `Object` class during object creation and containment state changes
- Used by `GameLogic` for object lookup and position synchronization

### Outgoing
- Calls into `TransportContain` for base containment logic
- Uses `ThingFactory` for payload object creation
- Interacts with `GameLogic` for object lookup
- Modifies `Object` state (position, orientation, weapon bonuses)

## Design Patterns
- **Template Method**: Extends base class methods while preserving core containment logic
- **Composite**: Manages hierarchical relationships between container and contained objects
- **Observer**: Notifies contained objects of state changes (e.g., stealth propagation)

*Not inferable*: Exact pattern usage may vary based on unshown code.
