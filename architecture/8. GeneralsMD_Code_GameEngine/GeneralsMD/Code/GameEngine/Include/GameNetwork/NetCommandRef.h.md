# GeneralsMD/Code/GameEngine/Include/GameNetwork/NetCommandRef.h

## Purpose
Manages references to network command messages in a linked list structure for tracking and relaying.

## Responsibilities
- Wraps `NetCommandMsg` with metadata (relay, timing, list pointers)
- Provides linked list navigation (next/prev)
- Tracks last send time per reference
- Memory pool management for object allocation

## Key Types
- **NetCommandRef (Class)**: Reference wrapper for network commands with list and timing metadata.
- **NetCommandRefMagicEnum (Enum)**: Not inferable (placeholder for memory pool glue).
- **NetCommandRef_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (placeholder for memory pool glue).

## Key Functions
### `NetCommandRef(NetCommandMsg *msg)`
- Purpose: Constructs a reference to a network command message.
- Calls: None (constructor).

### `getCommand()`
- Purpose: Returns the wrapped `NetCommandMsg`.
- Calls: None.

### `setRelay(UnsignedByte relay)`
- Purpose: Sets the relay value for this reference.
- Calls: None.

### `setTimeLastSent(time_t timeLastSent)`
- Purpose: Updates the last send timestamp.
- Calls: None.

## Globals
- **NEW_NETCOMMANDREF (Macro)**: Helper for creating instances (with/without debug info).

## Dependencies
- `NetCommandMsg.h` (for `NetCommandMsg`)
- `GameMemory.h` (for `MemoryPoolObject` and memory pool macros)
- `Common/GameMemory.h` (for memory management utilities)
