# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/GameWindowManagerScript.cpp - Enhanced Analysis

## Architectural Role
This file serves as the parser for the game's UI window definition files (.wnd), bridging the declarative script format with the runtime GameWindowManager system. It enables the game's UI to be defined externally, supporting both modding and localization.

## Cross-References
### Incoming
- **GameWindowManager.cpp**: Calls `WinCreateFromScript` to load window definitions
- **Gadget subclasses**: Use parsed properties (colors, fonts) during initialization
- **GameText system**: Relies on parsed font/color defaults for text rendering

### Outgoing
- **Common/FileSystem**: For script file loading
- **GameClient/WindowLayout**: Creates WindowLayoutInfo objects
- **GameClient/Gadget subclasses**: Instantiates specific UI controls (buttons, sliders, etc.)
- **Common/FunctionLexicon**: Resolves callback function names

## Design Patterns
- **Interpreter Pattern**: The script parser treats window definitions as a domain-specific language
- **Factory Pattern**: `createWindow` dynamically instantiates appropriate GameWindow subclasses
- **Strategy Pattern**: Parsing functions are dispatched via lookup tables (LayoutScriptParse/GameWindowParse)
