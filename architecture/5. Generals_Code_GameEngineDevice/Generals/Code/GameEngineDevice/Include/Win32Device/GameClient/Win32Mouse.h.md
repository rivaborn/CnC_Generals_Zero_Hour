# Generals/Code/GameEngineDevice/Include/Win32Device/GameClient/Win32Mouse.h

## Purpose
Defines the Win32Mouse class, handling mouse input via Windows messages.

## Responsibilities
- Manages mouse events from Win32 messages
- Handles cursor visibility and capture
- Translates Win32 mouse events to internal format
- Buffers mouse events for processing

## Key Types
- **NO_TIME_FROM_WINDOWS (Enum)**: Placeholder for no timestamp.
- **Win32Mouse (Class)**: Win32-specific mouse input handler.
- **Win32MouseEvent (Struct)**: Stores raw Win32 mouse event data.

## Key Functions
### `initCursorResources`
- Purpose: Loads Windows resources for 2D cursors.
- Calls: Not inferable.

### `translateEvent`
- Purpose: Converts Win32 mouse events to internal format.
- Calls: Not inferable.

### `getMouseEvent`
- Purpose: Retrieves the next buffered mouse event.
- Calls: `translateEvent`.

### `addWin32Event`
- Purpose: Adds a Win32 mouse event to the buffer.
- Calls: Not inferable.

## Globals
- **m_eventBuffer (Win32MouseEvent[Mouse::NUM_MOUSE_EVENTS])**: Stores raw Win32 mouse events.
- **m_nextFreeIndex (UnsignedInt)**: Tracks where to insert new events.
- **m_nextGetIndex (UnsignedInt)**: Tracks where to retrieve events.
- **m_currentWin32Cursor (MouseCursor)**: Last cursor image sent to D3D.
- **m_directionFrame (Int)**: Current frame of directional cursor.
- **m_lostFocus (Bool)**: Flag for window focus state.

## Dependencies
- `Mouse.h` (base class)
- Win32 types (`UINT`, `WPARAM`, `LP
