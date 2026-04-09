# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarResizer.cpp - Enhanced Analysis

## Architectural Role
This file implements the dynamic UI scaling system for the control bar, bridging the INI configuration system with the window management subsystem. It enables resolution-independent UI layout by maintaining alternative position/size mappings and applying them based on current display dimensions.

## Cross-References
### Incoming
- `ControlBar` class (calls `getControlBarResizer()`)
- `INI` parser (invokes `parseControlBarResizerDefinition()`)
- Resolution change handlers (trigger `sizeWindowsAlt()`/`sizeWindowsDefault()`)

### Outgoing
- `GameWindowManager` (via `TheWindowManager` global)
- `Display` subsystem (via `TheDisplay` global)
- `INI` class for configuration loading
- `GameWindow` instances for position/size manipulation

## Design Patterns
- **Strategy Pattern**: Alternative sizing is a strategy selected based on resolution
- **Registry Pattern**: Maintains a list of resizable windows with their configurations
- **Observer-like**: Reacts to resolution changes (though event mechanism isn't visible here)

*Not inferable*: Exact event triggering mechanism for resolution changes.
