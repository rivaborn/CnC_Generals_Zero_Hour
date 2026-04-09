# Generals/Code/Tools/CRCDiff/debug.h - Enhanced Analysis

## Architectural Role
This file provides a minimal, tool-specific debug logging mechanism for the CRCDiff utility, part of the build/tooling infrastructure. It isolates debug output control from the main game engine's logging systems, allowing tool-specific debug builds without affecting runtime performance.

## Cross-References
### Incoming
- Not inferable (no direct callers visible in context)

### Outgoing
- Relies on `cstdarg` for variadic function support
- Indirectly depends on `DEBUG` preprocessor symbol (likely set by build system)

## Design Patterns
- **Preprocessor Guard Pattern**: Uses `#ifdef DEBUG` to conditionally compile debug code, enabling zero-cost logging in release builds.
- **Macro Abstraction**: `DEBUG_LOG` macro hides variadic function call complexity, promoting consistent usage across tools.
- **Minimalist Dependency**: Avoids heavy logging frameworks (e.g., `MsgManager`) to keep tooling lightweight.
