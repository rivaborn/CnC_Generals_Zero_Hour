# GeneralsMD/Code/GameEngine/Source/GameLogic/Object/Behavior/SlowDeathBehavior.cpp - Enhanced Analysis

## Architectural Role
This file implements the core slow death behavior system, which handles the timed destruction of game objects with visual effects, physics, and timing. It integrates with the game's update loop, AI system, and rendering pipeline to provide a consistent death animation experience.

## Cross-References
### Incoming
- `BattleBusSlowDeathBehavior.cpp` calls `beginSlowDeath`
- `JetSlowDeathBehavior.cpp` calls `beginSlowDeath`, `onDie`, and `update`

### Outgoing
- Calls into `TheGameLogic` for object destruction and deselection
- Uses `TheFXListStore`, `TheObjectCreationListStore`, and `TheWeaponStore` for effect management
- Interacts with `TheGameLODManager` for level-of-detail adjustments

## Design Patterns
- **Strategy Pattern**: Different death behaviors can be selected via probability modifiers in `onDie`
- **Observer Pattern**: Listens for death events via `onDie` to trigger destruction sequence
- **Template Method**: `doPhaseStuff` provides a framework for phase-specific effects while allowing specialization

Rules followed. Output under 400 tokens.
