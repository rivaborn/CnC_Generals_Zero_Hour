# GeneralsMD/Code/GameEngine/Include/GameNetwork/IPEnumeration.h

## Purpose
Defines classes for enumerating local IP addresses and machine name on the network.

## Responsibilities
- Provide an IP wrapper class (`EnumeratedIP`) for storing IP address data.
- Implement `IPEnumeration` to retrieve local IP addresses and machine name.
- Manage memory allocation for `EnumeratedIP` objects via memory pool.

## Key Types
- **EnumeratedIP (Class)**: Wraps an IP address with string and numeric representations, supports linked list traversal.
- **IPEnumeration (Class)**: Facade for enumerating local network interfaces and machine name.
- **EnumeratedIPMagicEnum / EnumeratedIP_GLUE_NOT_IMPLEMENTED (Enum)**: Memory pool glue macros (not directly usable).

## Key Functions
### `EnumeratedIP::getIPstring()`
- Purpose: Retrieves the IP address as a string.
- Calls: None.

### `IPEnumeration::getAddresses()`
- Purpose: Returns a linked list of local IP addresses.
- Calls: None (implementation in .cpp).

### `IPEnumeration::getMachineName()`
- Purpose: Returns the local machine's network name.
- Calls: None (implementation in .cpp).

## Globals
None.

## Dependencies
- `GameNetwork/Transport.h` (for `MemoryPoolObject`, `AsciiString`, `UnsignedInt`, `Bool`).
- Memory pool macros (`MEMORY_POOL_GLUE_WITH_USERLOOKUP_CREATE`, `EMPTY_DTOR`).
