# GeneralsMD/Code/GameEngine/Include/Common/XferDeepCRC.h

## Purpose
Defines the XferDeepCRC class for hard disk read/write operations with CRC checking.

## Responsibilities
- Implements disk-based transfer with CRC validation
- Manages file I/O for serialization
- Overrides string transfer methods for custom handling
- Provides protected implementation for data transfer

## Key Types
- **XferDeepCRC (Class)**: Disk-based transfer with CRC checking
- **Snapshot (Class)**: Forward-declared, used elsewhere (not defined here)

## Key Functions
### XferDeepCRC::xferImplementation
- Purpose: Handles actual data transfer to/from disk
- Calls: Not inferable (implementation in .cpp)

### XferDeepCRC::open
- Purpose: Initializes a CRC session with a file identifier
- Calls: Not inferable

### XferDeepCRC::close
- Purpose: Terminates the CRC session
- Calls: Not inferable

## Globals
- **m_fileFP (FILE*)**: File pointer for disk operations

## Dependencies
- `Xfer.h` (base class)
- `XferCRC.h` (parent class)
- `AsciiString`, `UnicodeString` (string types)
- `FILE` (C stdio)
