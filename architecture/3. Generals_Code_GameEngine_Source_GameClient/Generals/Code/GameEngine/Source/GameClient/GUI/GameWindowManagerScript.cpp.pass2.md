# Generals/Code/GameEngine/Source/GameClient/GUI/GameWindowManagerScript.cpp - Enhanced Analysis

## Architectural Role
This file serves as the parser for the game's UI window definition system, bridging the declarative .wnd script files with the runtime GameWindowManager. It's the critical translation layer that allows designers to define UI layouts without direct code access.

## Cross-References
### Incoming
- GameWindowManager.cpp (calls WinCreateFromScript to load window definitions)
- UI event handlers (register callbacks via FunctionLexicon)
- Mod system (loads custom .wnd files)

### Outgoing
- GameWindowManager.h (creates GameWindow instances)
- Gadget subclasses (instantiates specific UI controls)
- FunctionLexicon (resolves callback names to functions)
- GameText system (for localized text)

## Design Patterns
- **Interpreter Pattern**: The script parser treats .wnd files as a domain-specific language
- **Factory Pattern**: createWindow acts as a factory for different window types
- **Strategy Pattern**: GameWindowParse structs implement different parsing strategies for various window properties

Rules followed. Analysis limited to 400 tokens.
