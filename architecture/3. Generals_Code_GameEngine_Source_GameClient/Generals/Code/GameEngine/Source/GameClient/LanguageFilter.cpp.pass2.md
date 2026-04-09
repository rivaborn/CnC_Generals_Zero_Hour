# Generals/Code/GameEngine/Source/GameClient/LanguageFilter.cpp - Enhanced Analysis

## Architectural Role
This file implements the game's chat censorship system, a cross-cutting concern that integrates with the networking layer to sanitize player communications. It operates as a singleton service, ensuring consistent filtering across all text inputs.

## Cross-References
### Incoming
- Likely called by chat/networking subsystems (e.g., `GameClient/Chat.cpp`) when processing player messages
- May be referenced during UI initialization for text input fields

### Outgoing
- Uses `FileSystem` and `File` for loading the censorship word list
- Relies on `UnicodeString` for text manipulation (from common utilities)

## Design Patterns
- **Singleton**: Global `TheLanguageFilter` provides centralized access
- **Strategy**: `unHaxor` implements a character transformation strategy for leetspeak decoding
- **Resource Management**: Manual memory handling for `WideChar` buffer in `filterLine` (pre-C++11)

*Not inferable*: Exact integration points with networking/UI not visible in this file.
