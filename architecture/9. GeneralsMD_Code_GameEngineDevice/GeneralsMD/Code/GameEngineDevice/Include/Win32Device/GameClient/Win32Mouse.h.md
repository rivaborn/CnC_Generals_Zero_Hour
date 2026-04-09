# GeneralsMD/Code/GameEngineDevice/Include/Win32Device/GameClient/Win32Mouse.h

## Purpose
Defines the Win32Mouse class, handling mouse input via Windows messages.

## Responsibilities
- Manages mouse events from Win32 messages
- Controls cursor visibility and capture state
- Translates Win32 mouse events to internal format
- Buffers mouse events for processing

## Key Types
- **NO_TIME_FROM_WINDOWS (Enum)**: Placeholder for no timestamp.
- **Win32Mouse (Class)**: Win32-specific mouse input handler.
- **Win32MouseEvent (Struct)**: Stores raw Win32 mouse event data.

## Key Functions
### `init()`
- Purpose: Initializes mouse system.
- Calls: None visible.

### `update()`
- Purpose: Updates mouse state.
- Calls: None visible.

### `setCursor()`
- Purpose: Sets the mouse cursor.
- Calls: None visible.

### `addWin32Event()`
- Purpose: Adds a Win32 mouse event to the buffer.
- Calls: None visible.

### `getMouseEvent()`
- Purpose: Retrieves the next buffered mouse event.
- Calls: `translateEvent()`.

### `translateEvent()`
- Purpose: Converts Win32 event to internal format.
- Calls: None visible.

## Globals
- **m_eventBuffer (Win32MouseEvent[16])**: Stores pending mouse events.
- **m_nextFreeIndex (UnsignedInt)**: Tracks next free slot in buffer.
- **m_nextGetIndex (UnsignedInt)**: Tracks next event to retrieve.
- **m_currentWin32Cursor (MouseCursor)**: Current cursor type.
- **m_directionFrame (Int)**: Current frame of directional cursor.
- **m_lostFocus (Bool)**: Flag for focus state.

## Dependencies
- `Mouse
