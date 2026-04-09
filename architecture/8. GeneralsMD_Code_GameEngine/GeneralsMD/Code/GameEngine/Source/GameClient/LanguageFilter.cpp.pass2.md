# GeneralsMD/Code/GameEngine/Source/GameClient/LanguageFilter.cpp - Enhanced Analysis

## Architectural Role
This file implements the game's chat censorship system, integrating with the UI layer to sanitize player input. It operates as a singleton service, decoupled from core game logic but tightly coupled to the file system and Unicode string handling.

## Cross-References
### Incoming
- Likely called from UI chat input handlers (e.g., `ChatWindow.cpp`) and possibly network message processing (e.g., `GameClient.cpp` for received messages).

### Outgoing
- Uses `TheFileSystem` for file I/O (common dependency pattern in SAGE).
- Relies on `UnicodeString` for text manipulation (shared utility class).
- No direct calls to rendering or game state systems, confirming its isolated role.

## Design Patterns
- **Singleton**: `TheLanguageFilter` provides global access (common in SAGE for utility systems).
- **Strategy**: `unHaxor()` encapsulates leetspeak normalization as a reusable transformation.
- **Resource Management**: Manual memory handling for `buf` in `filterLine()` (typical of early 2000s C++ engines).
