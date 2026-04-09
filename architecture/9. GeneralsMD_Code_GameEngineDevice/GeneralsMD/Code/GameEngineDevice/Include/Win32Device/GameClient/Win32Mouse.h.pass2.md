# GeneralsMD/Code/GameEngineDevice/Include/Win32Device/GameClient/Win32Mouse.h - Enhanced Analysis

## Architectural Role
This file implements the Win32-specific mouse input abstraction, bridging Windows messages with the engine's cross-platform mouse interface. It handles event buffering and cursor management, critical for input consistency across platforms.

## Cross-References
### Incoming
- **GameClient/Mouse.h**: Base class interface
- **Window procedure handlers**: Call `addWin32Event()` to enqueue raw Win32 messages
- **Input system**: Calls `getMouseEvent()` for polled input

### Outgoing
- **Direct3D/DirectInput**: Implicitly via cursor resource loading (`initCursorResources`)
- **GameClient/Mouse**: Base class virtual overrides
- **Cursor rendering**: Manages cursor visibility/capture state

## Design Patterns
- **Adapter Pattern**: Translates Win32-specific messages to engine's `MouseIO` format
- **Event Queue**: Uses circular buffer (`m_eventBuffer`) for asynchronous event handling
- **State Management**: Tracks cursor state (`m_currentWin32Cursor`) and focus state (`m_lostFocus`)
