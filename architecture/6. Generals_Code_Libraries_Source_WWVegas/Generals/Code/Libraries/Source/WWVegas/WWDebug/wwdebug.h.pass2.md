# Generals/Code/Libraries/Source/WWVegas/WWDebug/wwdebug.h - Enhanced Analysis

## Architectural Role
Central debug infrastructure header providing cross-cutting utilities for logging, assertions, triggers, and profiling. Serves as the foundation for debug functionality across all engine subsystems.

## Cross-References
### Incoming
- Debug-related macros used throughout engine (e.g., `WWDEBUG_SAY`, `WWASSERT`)
- Likely called by game logic, AI, rendering, and networking modules for debug output

### Outgoing
- References `debug.h` for core debug macros
- Uses Windows-specific `_asm int 0x03` for debugger breaks

## Design Patterns
- **Handler Pattern**: Installable callbacks for messages, assertions, triggers, and profiling
- **Preprocessor Directives**: Heavy use of `#ifdef` for build-configuration-specific behavior
- **Macro Abstraction**: Wraps complex debug functionality in simple macros (e.g., `WWASSERT`)
