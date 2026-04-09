# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/AIUpdate.h - Enhanced Analysis

## Architectural Role
This header defines the core AI behavior interface (`AIUpdateInterface`) that bridges the game logic layer with the SAGE engine's update system. It serves as the foundation for all unit AI, coordinating pathfinding, state machines, and tactical decision-making.

## Cross-References
### Incoming
- **AI Specializations**: DozerAIUpdate, WorkerAIUpdate, JetAIUpdate, etc. inherit and implement this interface
- **Game Logic**: AIStateMachine, GameLogic modules consume this interface
- **Pathfinding**: PathfindServicesInterface interacts with path computation methods

### Outgoing
- **Locomotion**: Directly manipulates LocomotorSet for movement control
- **State Management**: Drives AIStateMachine transitions
- **Targeting**: Consumes AttackPriorityInfo for threat assessment

## Design Patterns
- **Strategy Pattern**: LocomotorSet allows dynamic movement behavior switching
- **State Pattern**: AIStateMachine delegation for behavior variation
- **Observer Pattern**: Notifications for state changes (friend_notifyStateMachineChanged)

*Cross-cutting insight*: The `m_queueForPathFrame` field with its emphatic warnings reveals a historical concurrency issue where pathfinding requests needed strict serialization. The `LocomotorSetType` enum's persistence requirement (save file compatibility) suggests this was a late-game addition that became critical infrastructure.
