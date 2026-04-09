# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/refcount.cpp - Enhanced Analysis

## Architectural Role
This file implements a debug-only reference counting system for tracking object lifetimes. It's part of the WWLib utility library, providing memory management diagnostics for the SAGE engine.

## Cross-References
### Incoming
- Likely called by game object constructors/destructors (e.g., W3D models, game entities)
- Used by memory management systems (e.g., WWLib's memory allocators)

### Outgoing
- Uses `RefCountListClass` for maintaining active reference list
- Relies on `windows.h` for basic types and `assert` for validation

## Design Patterns
- **Singleton-like management**: Global `ActiveRefList` and `TotalRefs` track all references
- **Debug-only instrumentation**: Entire implementation is wrapped in `#ifndef NDEBUG`
- **Observer pattern**: Tracks reference ownership with file/line metadata for debugging

*Not inferable*: Exact callers of reference counting functions (would require full call graph analysis)
