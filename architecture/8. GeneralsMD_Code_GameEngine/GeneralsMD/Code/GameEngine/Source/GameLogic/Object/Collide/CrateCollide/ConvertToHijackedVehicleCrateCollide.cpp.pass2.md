# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/ConvertToHijackedVehicleCrateCollide.cpp - Enhanced Analysis

## Architectural Role
This file implements the vehicle hijacking mechanic, bridging the crate collision system with the AI and experience systems. It handles the state transition of both the hijacker and target vehicle during the hijacking process.

## Cross-References
### Incoming
- Called by the crate collision system when a terrorist collides with a target
- Referenced by AIUpdateInterface for goal object validation

### Outgoing
- Uses AIUpdateInterface to control vehicle behavior post-hijack
- Interacts with ExperienceTracker for veterancy transfer
- Modifies PartitionManager registration and Drawable visibility
- Triggers Radar infiltration events and Eva announcements

## Design Patterns
- **Strategy Pattern**: Extends CrateCollide base class to customize hijacking behavior
- **State Pattern**: Manages hijacker's state transition (visible â hidden, selectable â unselectable)
- **Observer Pattern**: Notifies Radar and Eva systems of hijacking events

Rules followed. Output under 400 tokens.
