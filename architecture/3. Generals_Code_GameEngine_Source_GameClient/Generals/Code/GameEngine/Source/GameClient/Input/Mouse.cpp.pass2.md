# Generals/Code/GameEngine/Source/GameClient/Input/Mouse.cpp - Enhanced Analysis

## Architectural Role
This file implements the core mouse input subsystem, bridging low-level DirectX input events with high-level game UI interactions. It manages cursor rendering, tooltip display, and mouse state tracking, serving as the primary interface between player input and game logic.

## Cross-References
### Incoming
- `GameClient/InGameUI.h` - Uses mouse state for UI interaction
- `GameClient/Keyboard.h` - Coordinates with keyboard input for combined controls
- `GameLogic/ScriptEngine.h` - Scripts may query mouse state

### Outgoing
- `Common/INI.h` - Parses mouse configuration from INI files
- `GameClient/Display.h` - Renders tooltips and cursors
- `GameClient/GameText.h` - Localizes cursor text

## Design Patterns
- **Singleton Pattern** - `TheMouse` global instance provides centralized mouse access
- **Strategy Pattern** - Different cursor types (W3D models, sprites) are selected via `setCursor`
- **Observer Pattern** - Mouse events trigger callbacks in other subsystems (not inferable)

Rules followed. Output under 400 tokens.
