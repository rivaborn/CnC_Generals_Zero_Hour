# Generals/Code/Libraries/Source/WWVegas/WWLib/keyboard.h - Enhanced Analysis

## Architectural Role
This header defines the core keyboard input abstraction layer for the SAGE engine, bridging Windows API input with game-specific key handling. It serves as the primary interface for all keyboard and mouse input processing, with special handling for modifier keys and input buffering.

## Cross-References
### Incoming
- Game input systems (e.g., `InputClass`) call `KeyboardClass::Get()` and `Check()`
- UI systems use `KeyboardClass::Down()` for key state queries
- Mouse input is consumed by `WWKeyboardClass::Message_Handler` from Windows message loop

### Outgoing
- Calls Windows API via `_xmouse.h` for raw input
- Uses `bool.h` for type consistency
- Interfaces with `win.h` for message handling

## Design Patterns
- **Adapter Pattern**: `KeyboardClass` wraps `WWKeyboardClass` to convert library-specific types to game types
- **Circular Buffer**: Implements a fixed-size queue for key events with `Head`/`Tail` pointers
- **State Machine**: Tracks key states via `KeyState` array for modifier key handling

*Not inferable*: Exact buffering strategy (e.g., FIFO vs. priority) or thread-safety mechanisms.
