# Generals/Code/Tools/Autorun/CallbackHook.h - Enhanced Analysis

## Architectural Role
This header defines a lightweight callback infrastructure used by the Autorun tooling subsystem, enabling deferred execution of user-provided functions. It bridges the gap between tooling scripts and engine initialization sequences.

## Cross-References
### Incoming
- `Generals/Code/Tools/Autorun/Autorun.cpp` (uses `Callback` for scripted initialization hooks)
- `Generals/Code/Tools/Autorun/CommandLine.cpp` (likely registers CLI-driven callbacks)

### Outgoing
- None (header-only utility with no external dependencies)

## Design Patterns
- **Template Method**: `CallbackHook::DoCallback` defines the interface for callback execution.
- **Strategy**: Encapsulates interchangeable callback behaviors via polymorphism.
- **Pimpl-like**: The `Callback` template hides implementation details behind a stable interface.

*Not inferable*: No observer or command patterns detected in this header alone.
