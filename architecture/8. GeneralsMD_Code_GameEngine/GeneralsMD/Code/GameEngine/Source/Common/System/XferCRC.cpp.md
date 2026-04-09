# GeneralsMD/Code/GameEngine/Source/Common/System/XferCRC.cpp

## Purpose
Implements CRC (Cyclic Redundancy Check) calculation for data transfer operations in the game engine.

## Responsibilities
- Calculates CRC for data blocks
- Handles file I/O for deep CRC operations
- Manages snapshot CRC computation
- Provides network byte order conversion for CRC values

## Key Types
- XferCRC (Class): Base class for CRC calculation during data transfer
- XferDeepCRC (Class): Extends XferCRC to handle file-based CRC calculation and data saving

## Key Functions
### XferCRC::addCRC
- Purpose: Updates CRC value with a new unsigned integer
- Calls: htonl

### XferCRC::xferImplementation
- Purpose: Processes raw data to compute CRC
- Calls: addCRC, htonl

### XferDeepCRC::xferImplementation
- Purpose: Writes data to file and computes CRC
- Calls: XferCRC::xferImplementation, fwrite

### XferDeepCRC::xferAsciiString
- Purpose: Saves ASCII string data with length prefix
- Calls: xferUnsignedShort, xferUser

### XferDeepCRC::xferUnicodeString
- Purpose: Saves Unicode string data with length prefix
- Calls: xferByte, xferUser

## Globals
- None

## Dependencies
- Common/XferCRC.h
- Common/XferDeepCRC.h
- Common/CRC.h
- Common/Snapshot.h
- winsock2.h (for htonl)
