# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Collide/CrateCollide/SabotageSupplyDropzoneCrateCollide.cpp - Enhanced Analysis

## Architectural Role
This file implements the sabotage behavior for a specialized "crate" (saboteur unit) that interacts with enemy supply dropzones. It bridges the collision system with game economy and AI systems, demonstrating how modular behavior components (via `CrateCollide`) extend base functionality.

## Cross-References
### Incoming
- **AIUpdate.h**: Uses `AIUpdateInterface` to verify goal object alignment
- **OCLUpdate.h**: Directly manipulates dropzone timers via `OCLUpdate::resetTimer`
- **ContainModule.h**: Accesses player money systems for theft mechanics

### Outgoing
- **Radar.h**: Triggers infiltration events (`tryInfiltrationEvent`)
- **Eva.h**: Plays EVA announcements (`setShouldPlay`)
- **InGameUI.h**: Displays floating text for money changes
- **GameAudio.h/MiscAudio.h**: Implicit audio feedback via EVA system

## Design Patterns
- **Template Method**: Extends `CrateCollide` with specialized `isValidToExecute` and `executeCrateBehavior`
- **Dependency Injection**: Receives `ModuleData` in constructor for configuration
- **Strategy**: Encapsulates sabotage logic as a reusable module for other crate types

*Not inferable*: No clear use of Observer, Factory, or Visitor patterns.
