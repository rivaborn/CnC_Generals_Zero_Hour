# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/ControlBar/ControlBarScheme.cpp - Enhanced Analysis

## Architectural Role
This file implements the control bar's visual scheme system, bridging the UI layer with player-specific data. It handles resolution-independent scaling and side-specific customization, making it a critical component in the HUD rendering pipeline.

## Cross-References
### Incoming
- `ControlBar.h` (uses `setControlCommand` and `findCommandButton`)
- `GameWindowManager.h` (accesses `TheWindowManager` for communicator button)
- `Player.h` (uses `getSide()` for scheme selection)

### Outgoing
- `INIControlBarScheme.cpp` (for INI parsing)
- `Display.h` (for resolution scaling)
- `Image.h` (for image manipulation in animations)

## Design Patterns
- **Strategy Pattern**: Different control bar schemes are selected based on player side/resolution
- **Observer Pattern**: Control bar updates when player changes (via `setControlBarSchemeByPlayer`)
- **Factory Pattern**: Scheme management via `ControlBarSchemeManager` (not inferable in first pass)

*Token count: 198*
