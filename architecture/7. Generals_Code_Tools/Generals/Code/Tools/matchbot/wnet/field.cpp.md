# Generals/Code/Tools/matchbot/wnet/field.cpp

## Purpose
Implements the FieldClass for network data field handling, including type conversion and serialization.

## Responsibilities
- Manages field data storage and type conversion
- Handles host-to-network and network-to-host byte order conversion
- Provides field accessors and setters
- Supports multiple data types (char, short, long, string, binary chunks)

## Key Types
- **FieldClass (Class)**: Represents a network data field with ID, type, size, and data
- **TYPE_CHAR, TYPE_UNSIGNED_CHAR, TYPE_SHORT, TYPE_UNSIGNED_SHORT, TYPE_LONG, TYPE_UNSIGNED_LONG, TYPE_STRING, TYPE_CHUNK (Enums)**: Data type identifiers

## Key Functions
### FieldClass::Clear
- Purpose: Releases resources and resets field state
- Calls: delete[]

### FieldClass::Set (various overloads)
- Purpose: Sets field data with specified type
- Calls: Clear(), strncpy(), memcpy()

### FieldClass::Host_To_Net
- Purpose: Converts field data from host to network byte order
- Calls: htons(), htonl()

### FieldClass::Net_To_Host
- Purpose: Converts field data from network to host byte order
- Calls: ntohs(), ntohl()

## Globals
- None

## Dependencies
- string.h, sys/types.h, netinet/in.h (Unix), windows.h (Win32)
- htons(), htonl(), ntohs(), ntohl() (network byte order functions)
