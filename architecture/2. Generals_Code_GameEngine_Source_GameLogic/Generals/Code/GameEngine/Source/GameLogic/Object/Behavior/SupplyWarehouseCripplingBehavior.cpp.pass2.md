# Generals/Code/GameEngine/Source/GameLogic/Object/Behavior/SupplyWarehouseCripplingBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the behavior for a supply warehouse that becomes crippled when damaged and manages its healing process. It fits into the broader engine architecture by handling specific game logic related to object behaviors, particularly focusing on damage response and self-healing mechanisms.

## Cross-References
### Incoming
- `SupplyWarehouseCripplingBehavior::onBodyDamageStateChange` is called by the game logic system when a body damage state changes.
- `SupplyWarehouseCripplingBehavior::onDamage` is called by the game logic system when an object takes damage.
- `SupplyWarehouseCripplingBehavior::update` is called periodically by the update loop to manage healing.

### Outgoing
- Calls `resetSelfHealSupression`, `setWakeFrame`, and `attemptHealing` within the game logic subsystem.
- Calls `startCrippledEffects` and `stopCrippledEffects` on the dock update interface, which is part of the object's module system.

## Design Patterns
- **Observer Pattern**: The behavior responds to damage events (`onDamage`, `onBodyDamageStateChange`) by observing changes in the object's state.
- **State Pattern**: Manages different states (e.g., crippled vs. not crippled) and transitions between them.
- **Strategy Pattern**: Uses configuration data (`SupplyWarehouseCripplingBehaviorModuleData`) to define healing strategies, allowing for flexible behavior customization.
