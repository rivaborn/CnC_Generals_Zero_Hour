# GeneralsMD/Code/GameEngine/Include/GameNetwork/User.h

## Purpose
Defines the `User` class representing a network user with name, IP address, and port.

## Responsibilities
- Stores user network identification data (name, IP, port)
- Provides basic comparison and assignment operations
- Manages memory allocation via `MemoryPoolObject`

## Key Types
- **User (Class)**: Represents a network user with name, IP, and port.
- **UserMagicEnum (Enum)**: Not inferable (likely unused placeholder).
- **User_GLUE_NOT_IMPLEMENTED (Enum)**: Not inferable (likely unused placeholder).

## Key Functions
### User(UnicodeString, UnsignedInt, UnsignedInt)
- Purpose: Constructs a `User` with name, IP, and port.
- Calls: Not inferable (constructor body not shown).

### operator=(const User*)
- Purpose: Assigns user data from another `User`.
- Calls: Not inferable.

### operator==(const User*)
- Purpose: Compares two `User` objects for equality.
- Calls: Not inferable.

### operator!=(const User*)
- Purpose: Compares two `User` objects for inequality.
- Calls: Not inferable.

### setName(UnicodeString)
- Purpose: Sets the user's name.
- Calls: Not inferable.

## Globals
- None

## Dependencies
- `GameNetwork/networkdefs.h` (for network types)
- `Common/UnicodeString.h` (for string handling)
- `MemoryPoolObject` (base class for memory management)
