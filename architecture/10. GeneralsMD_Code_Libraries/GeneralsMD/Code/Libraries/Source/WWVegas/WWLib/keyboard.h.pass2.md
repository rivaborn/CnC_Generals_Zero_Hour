# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/keyboard.h - Enhanced Analysis

## Architectural Role
This header defines the core keyboard input abstraction layer for the SAGE engine, bridging Windows API input events with game-specific key handling. It serves as the primary interface for all keyboard and mouse input processing, with a circular buffer design that decouples input events from game logic frames.

## Cross-References
### Incoming
- Game input systems (e.g., `InputClass` in `input.cpp`)
- UI event handlers (e.g., `UIManagerClass`)
- Network input synchronization (e.g., `NetInputClass`)

### Outgoing
- Windows API (`HWND`, `UINT`, `LONG` message handling)
- Mouse coordinate functions (`Get_Mouse_X/Y`)
- Internal buffer management (`Put_Element`, `Buff_Get`)

## Design Patterns
- **Adapter Pattern**: `KeyboardClass` wraps `WWKeyboardClass` to convert library-specific return types (`unsigned short`) to game-specific enums (`KeyNumType`).
- **Circular Buffer**: Input events are stored in a fixed-size ring buffer (`Buffer[256]`) with `Head`/`Tail` pointers, enabling non-blocking input handling.
- **Event Sourcing**: Key/mouse events are stored with metadata (modifiers, release flags) for replayability in networking or input remapping scenarios.
