# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Update/AIUpdate/JetAIUpdate.cpp - Enhanced Analysis

## Architectural Role
This file implements the state machine and behavior logic for jet and helicopter AI, bridging the gap between high-level AI commands and low-level locomotion/physics systems. It handles the complex coordination required for airfield operations (takeoff/landing/parking) while integrating with the game's partitioning system for spatial queries.

## Cross-References
### Incoming
- **AIUpdateInterface**: Base class for AI behavior modules
- **ActionManager**: For command processing and state transitions
- **PartitionManager**: For spatial queries (airfield/parking space location)
- **PhysicsUpdate**: For movement and collision handling
- **Weapon**: For ammo status checks and reload behavior

### Outgoing
- **Drawable**: For visual/audio effects (afterburners, ambient sounds)
- **Locomotor**: For movement control (taxiing, takeoff/landing)
- **ParkingPlaceBehavior**: For airfield parking space management
- **AudioSystem**: For sound event management (afterburner sounds)

## Design Patterns
- **State Pattern**: Uses distinct state classes (JetAwaitingRunwayState, etc.) to encapsulate different phases of jet/helicopter behavior
- **Strategy Pattern**: Different state machines for jets vs helicopters (JetAIStateMachine vs HeliAIStateMachine)
- **Observer Pattern**: Tracks targetedBy list to react to enemy threats (cross-referenced with CountermeasuresBehavior)

**Key Insight**: The file shows tight coupling between AI state transitions and physical movement systems, with explicit handling of network synchronization (xfer/CRC methods) for multiplayer consistency. The afterburner sound management reveals a pattern where audio state mirrors physical model conditions.
