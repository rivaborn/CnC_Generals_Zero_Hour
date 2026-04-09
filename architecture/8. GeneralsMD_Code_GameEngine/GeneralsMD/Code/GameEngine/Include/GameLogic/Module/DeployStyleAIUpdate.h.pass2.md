# GeneralsMD/Code/GameEngine/Include/GameLogic/Module/DeployStyleAIUpdate.h - Enhanced Analysis

## Architectural Role
This file defines the AI behavior module for deployable units, bridging the gap between unit commands and the state machine that governs deployment/undeployment mechanics. It's part of the modular AI system that allows different unit types to have specialized behavior without monolithic conditionals.

## Cross-References
### Incoming
- **AICommandProcessor**: Likely calls `aiDoCommand` to handle player/AI-issued deploy/undeploy orders
- **Thing::update()**: Probably invokes `update()` as part of the game loop for state transitions
- **UnitCommandSystem**: May call `setMyState` directly for forced state changes (e.g., scripted events)

### Outgoing
- **StateMachine** (from Common/StateMachine.h): Inherits state management infrastructure
- **AIUpdateModuleData**: Base class for configuration parsing
- **INI parsing system**: Uses `MultiIniFieldParse` for modding support
- **Animation/Turret systems**: Implicitly interacts with these for `m_manualDeployAnimations` and turret alignment logic

## Design Patterns
- **State Pattern**: Encapsulates deployment states (READY_TO_MOVE, DEPLOY, etc.) with distinct behaviors
- **Module Pattern**: Follows SAGE's modular AI design, allowing pluggable behavior via `AIUpdateInterface`
- **Data-Driven Design**: Configuration via `DeployStyleAIUpdateModuleData` enables modding without code changes

*Cross-cutting insight*: The `m_turretsMustCenterBeforePacking` flag suggests tight coupling with the rendering/animation system, where turret alignment must complete before undeployment animations can proceed. This implies the AI module must coordinate with the W3D renderer's animation state.
