# GeneralsMD/Code/GameEngine/Include/GameClient/SelectionInfo.h - Enhanced Analysis

## Architectural Role
This header bridges the UI layer and game logic by providing context-aware selection metadata. It enables the UI to dynamically adjust behavior (e.g., command availability) based on selection composition, while abstracting drawable iteration for spatial queries.

## Cross-References
### Incoming
- **UI Systems**: InGameUI.h (dependency) and likely UI command handlers
- **Selection Logic**: Files managing unit/building selection (e.g., GameClient/SelectionManager.cpp)
- **Input Handling**: Mouse/keyboard input processors for context-sensitive actions

### Outgoing
- **Drawable System**: Uses DrawableList/Drawable for spatial queries
- **Kind System**: Relies on KindOfMaskType for object classification
- **Iteration Framework**: Integrates with iterateDrawablesInRegion (callback pattern)

## Design Patterns
- **Callback Pattern**: `addDrawableToList` serves as a visitor for drawable iteration
- **Data Transfer Object**: `SelectionInfo` encapsulates selection state for UI/logic decoupling
- **Strategy Pattern**: `getPickTypesForContext`/`getPickTypesForCurrentSelection` encapsulate selection logic variants

*Not inferable*: No clear use of Observer or Factory patterns.
