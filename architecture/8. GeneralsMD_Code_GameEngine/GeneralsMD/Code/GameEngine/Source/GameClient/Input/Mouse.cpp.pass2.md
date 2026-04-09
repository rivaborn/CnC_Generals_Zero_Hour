# GeneralsMD/Code/GameEngine/Source/GameClient/Input/Mouse.cpp - Enhanced Analysis

## Architectural Role
This file is the central hub for mouse input handling in the SAGE engine, bridging low-level DirectX input with high-level game interactions. It manages cursor rendering across multiple display modes (Windows, W3D, DirectX) and coordinates with UI systems for tooltips and drag operations.

## Cross-References
### Incoming
- `GameClient/InGameUI.h` - Uses mouse state for UI interactions
- `GameLogic/ScriptEngine.h` - Scripts may query mouse position/state
- `GameClient/Display.h` - Renders cursors and tooltips

### Outgoing
- DirectX mouse input functions (via `updateMouseData`)
- `TheDisplay` for rendering operations
- `TheGameText` for localized cursor tooltips
- `Keyboard.h` for combined input handling

## Design Patterns
- **Singleton Pattern**: `TheMouse` global instance ensures single mouse controller
- **Strategy Pattern**: Multiple cursor rendering modes (`RedrawMode`) can be selected
- **Observer Pattern**: Mouse state changes likely trigger UI updates (not shown in file)

*Not inferable*: Exact event dispatch mechanism to UI components.
