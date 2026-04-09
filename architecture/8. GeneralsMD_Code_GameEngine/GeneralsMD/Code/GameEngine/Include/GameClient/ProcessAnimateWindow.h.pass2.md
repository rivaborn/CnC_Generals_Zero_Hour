# GeneralsMD/Code/GameEngine/Include/GameClient/ProcessAnimateWindow.h - Enhanced Analysis

## Architectural Role
This file defines the animation controller hierarchy for UI window transitions in the SAGE engine. It bridges the UI system with the animation framework, allowing modular window entrance/exit effects.

## Cross-References
### Incoming
- `GameClient/AnimateWindow.cpp` (implements `AnimateWindow` class that uses these processors)
- `GameClient/GameWindow.cpp` (likely instantiates specific animation processors)
- `GameClient/UIShell.cpp` (calls `updateAnimateWindow`/`reverseAnimateWindow` per-frame)

### Outgoing
- None (pure interface, no external calls)

## Design Patterns
- **Template Method**: Base class defines animation lifecycle hooks (`init`, `update`, `reverse`) while derived classes implement specific behaviors.
- **Strategy**: Each animation type is a pluggable strategy for window transitions, selected at runtime.
- **Open/Closed Principle**: New animations can be added via inheritance without modifying existing code.
