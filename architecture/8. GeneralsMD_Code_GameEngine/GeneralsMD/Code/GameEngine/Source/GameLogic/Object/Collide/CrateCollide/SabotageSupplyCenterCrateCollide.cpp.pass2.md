# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SabotageSupplyCenterCrateCollide.cpp - Enhanced Analysis

## Architectural Role
This file implements the sabotage behavior for terrorist units (disguised as crates) that steal money from enemy supply centers. It extends the base `CrateCollide` class to add faction-specific sabotage logic, bridging the gap between unit AI and economic systems.

## Cross-References
### Incoming
- Called by `AIUpdate` modules (e.g., `HijackerUpdate`) when terrorist units collide with supply centers
- Used by `ScriptEngine` for mission-specific sabotage triggers

### Outgoing
- Interacts with `Player` and `Money` systems for economic transactions
- Triggers `Radar` infiltration events and `Eva` voice alerts
- Uses `InGameUI` for floating text feedback
- Relies on `Object` relationship checks for target validation

## Design Patterns
- **Template Method**: Extends `CrateCollide` with specialized sabotage behavior while preserving base collision logic
- **Strategy**: Encapsulates sabotage logic as a module that can be swapped for different crate types
- **Observer**: Notifies global systems (`Radar`, `Eva`) of sabotage events via callbacks

*Not inferable: No clear use of Visitor, Factory, or Decorator patterns.*
