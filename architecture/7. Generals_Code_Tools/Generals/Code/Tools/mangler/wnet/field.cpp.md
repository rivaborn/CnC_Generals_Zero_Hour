# Generals/Code/Tools/mangler/wnet/field.cpp

## Purpose
Implements the FieldClass for network data serialization, handling type conversion between host and network byte order.

## Responsibilities
- Manages field data storage and type identification
- Performs host-to-network and network-to-host byte order conversion
- Supports multiple data types (char, short, long, string, binary chunks)
- Handles memory allocation/deallocation for field data

## Key Types
- **FieldClass (Class)**: Represents a network data field with type, size, and payload
- **DataType (int)**: Enum-like values for field types (TYPE_CHAR, TYPE_SHORT, etc.)

## Key Functions
### FieldClass::Clear
- Purpose: Releases resources and resets field state
- Calls: delete[]

### FieldClass::Set (various overloads)
- Purpose: Initializes field with data of specific type
- Calls: Clear(), strncpy(), memcpy()

### FieldClass::Host_To_Net
- Purpose: Converts field data to network byte order
- Calls: htons(), htonl()

### FieldClass::Net_To_Host
- Purpose: Converts field data from network to host byte order
- Calls: ntohs(), ntohl()

## Globals
- None

## Dependencies
- `<string.h>`, `<sys/types.h>`, `<netinet/in.h>` (Unix), `<windows.h>` (Windows)
- `htons()`, `htonl()`, `ntohs()`, `ntohl()` (network byte order functions)
