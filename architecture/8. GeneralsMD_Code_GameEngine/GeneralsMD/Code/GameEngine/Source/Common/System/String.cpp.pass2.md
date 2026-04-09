# GeneralsMD/Code/GameEngine/Source/Common/System/String.cpp - Enhanced Analysis

## Architectural Role
This file implements the core `WSYS_String` class, serving as the foundational string abstraction for the entire engine. It provides dynamic string manipulation capabilities used across all subsystems, from UI text rendering to configuration parsing.

## Cross-References
### Incoming
- **GameClient**: `DisplayString` operations rely on `WSYS_String` for text manipulation
- **Common/System**: Other string classes (`AsciiString`, `UnicodeString`) reference its core operations

### Outgoing
- **Memory System**: Uses `MSGNEW` for allocation, tying into the engine's memory management
- **C Runtime**: Directly calls `strlen`, `strcpy`, `vsprintf`, etc., for low-level operations

## Design Patterns
- **RAII**: Manages dynamic memory via constructor/destructor
- **Wrapper Facade**: Abstracts C-style strings with safer C++ interface
- **Factory Method**: `format()` creates formatted strings internally

*Not inferable*: No clear use of Observer, Strategy, or other complex patterns.
