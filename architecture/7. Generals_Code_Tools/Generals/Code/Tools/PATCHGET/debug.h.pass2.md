# Generals/Code/Tools/PATCHGET/debug.h - Enhanced Analysis

## Architectural Role
This header provides minimal debug utilities specifically for the PATCHGET tool, serving as a lightweight alternative to the more comprehensive `wdebug.h` used elsewhere in the codebase. It bridges the gap between tool-specific debugging needs and the broader engine's debug infrastructure.

## Cross-References
### Incoming
- Likely called by PATCHGET tool implementation files (not listed in cross-references)

### Outgoing
- Relies on external `DebugCrash` implementation (not defined here)
- Uses `<cstdarg>` for variadic function support

## Design Patterns
- **Preprocessor Directives**: Heavy use of `#ifdef` to conditionally include debug functionality based on build flags (`DEBUG`, `DEBUG_CRASHING`)
- **Macro Abstraction**: `DEBUG_LOG`, `DEBUG_CRASH`, and `DEBUG_ASSERTCRASH` macros hide implementation details and provide consistent interfaces
- **Global State**: Uses `TheCurrentIgnoreCrashPtr` as a crude mechanism to control crash behavior (not ideal, but pragmatic for tooling)
