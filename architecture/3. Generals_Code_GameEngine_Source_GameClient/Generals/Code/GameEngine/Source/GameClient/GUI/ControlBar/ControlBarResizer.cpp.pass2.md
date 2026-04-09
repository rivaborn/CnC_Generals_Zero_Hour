# Generals/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarResizer.cpp - Enhanced Analysis

## Architectural Role
This file implements the dynamic UI scaling system for the control bar, bridging the INI configuration system with the window management subsystem. It enables resolution-independent UI layout by maintaining alternative position/size mappings for different screen resolutions.

## Cross-References
### Incoming
- `ControlBar.cpp` (likely calls `sizeWindowsDefault`/`sizeWindowsAlt` during resolution changes)
- `INI` parser (invokes `parseControlBarResizerDefinition` during config loading)
- `GameWindowManager` (registers windows for resizing)

### Outgoing
- `INI` class (for config parsing)
- `GameWindow` class (for position/size manipulation)
- `Display` singleton (for resolution queries)
- `TheWindowManager`/`TheNameKeyGenerator` (for window lookup)

## Design Patterns
- **Strategy Pattern**: Alternative sizing logic (`sizeWindowsDefault` vs `sizeWindowsAlt`) can be selected at runtime
- **Resource Pool**: Manages a list of `ResizerWindow` objects with lazy initialization
- **INI Parsing Table**: Uses reflection-like `FieldParse` table for declarative config parsing (not inferable if unique to SAGE)
