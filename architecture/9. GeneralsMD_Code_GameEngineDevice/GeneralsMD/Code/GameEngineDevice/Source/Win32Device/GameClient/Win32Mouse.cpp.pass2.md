# GeneralsMD/Code/GameEngineDevice/Source/Win32Device/GameClient/Win32Mouse.cpp - Enhanced Analysis

## Architectural Role
This file implements the Win32-specific mouse input subsystem, bridging Windows messages with the engine's abstract input system. It handles cursor management and input buffering, critical for both in-game and UI interactions.

## Cross-References
### Incoming
- **Win32MessageHandler**: Calls `addWin32Event` to enqueue Windows mouse messages
- **GameClient**: Uses `getMouseEvent` for frame-based input processing
- **UI System**: Likely calls `setCursor` for context-sensitive cursor changes

### Outgoing
- **Win32 API**: Directly calls `SetCursor`, `LoadCursorFromFile`
- **Base Mouse Class**: Extends `Mouse::init()`, `Mouse::reset()`, etc.
- **GameClient**: Queries `TheGameClient->getFrame()` for event timing

## Design Patterns
- **Event Buffer Pattern**: Uses a circular buffer (`m_eventBuffer`) to decouple message processing from input handling
- **Strategy Pattern**: Cursor loading varies by direction (`m_cursorInfo[cursor].numDirections`), allowing dynamic cursor sets
- **Singleton-like Access**: Global `TheWin32Mouse` provides centralized mouse state management

*Not inferable*: Exact relationship with `Win32MessageHandler` (e.g., callback registration).
