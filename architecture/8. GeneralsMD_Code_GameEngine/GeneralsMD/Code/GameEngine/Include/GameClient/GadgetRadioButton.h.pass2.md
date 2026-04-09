# GeneralsMD/Code/GameEngine/Include/GameClient/GadgetRadioButton.h - Enhanced Analysis

## Architectural Role
This header provides a thin abstraction layer over the `GameWindow` class for radio button UI controls. It encapsulates the visual state management (enabled/disabled/highlighted) and selection logic, serving as part of the UI gadget system in the SAGE engine.

## Cross-References
### Incoming
- UI-related files (e.g., menu systems, dialogs) that instantiate radio buttons
- Localization systems (via `GadgetRadioSetText`)

### Outgoing
- Directly delegates to `GameWindow` methods (`winSetEnabledImage`, etc.)
- Implicitly depends on the image/resource system for visual assets

## Design Patterns
- **Facade Pattern**: Provides simplified methods for complex `GameWindow` operations
- **Inline Delegation**: All functions are inlined to avoid runtime overhead
- **State Pattern**: Manages different visual states (enabled/disabled/highlighted) via separate setter/getter methods

*Not inferable*: No clear use of Observer or Strategy patterns despite UI interaction implications.
