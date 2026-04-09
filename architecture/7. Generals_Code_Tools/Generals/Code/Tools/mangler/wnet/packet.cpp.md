# Generals/Code/Tools/mangler/wnet/packet.cpp

## Purpose
Handles packet serialization/deserialization for network communication in the Westwood Auto Registration App.

## Responsibilities
- Parses incoming network packets into structured fields
- Constructs outgoing packets from field data
- Manages field list (addition, lookup, retrieval)
- Handles endianness conversion (host â network byte order)

## Key Types
- **PacketClass (Class)**: Manages packet structure and field operations
- **FieldClass (Class)**: Represents individual packet fields (not fully shown here)
- **bit8 (Type)**: Boolean-like type (likely `unsigned char`)

## Key Functions
### `PacketClass::PacketClass(char *curbuf)`
- Purpose: Constructs a packet from raw network buffer
- Calls: `ntohs`, `memcpy`, `FieldClass::Net_To_Host`, `Add_Field`

### `PacketClass::Create_Comms_Packet(int &size)`
- Purpose: Serializes packet fields into a network-transmittable buffer
- Calls: `htons`, `memcpy`, `FieldClass::Host_To_Net`, `FieldClass::Net_To_Host`

### `PacketClass::Find_Field(char *id)`
- Purpose: Locates a field by its ID in the packet
- Calls: `strncmp`

### `PacketClass::Get_Field(char *id, [various types])`
- Purpose: Retrieves field data of specific types (char, short, int, etc.)
- Calls: `Find_Field`

### `PacketClass::Get_Field_At(int position)`
- Purpose: Retrieves field at specific position in list
- Calls: None (direct iteration)

### `PacketClass::Get_Num_Fields()`
- Purpose: Counts fields in the packet
- Calls: None (direct iteration)

## Globals
- None

## Dependencies
- `packet.h` (header for PacketClass/FieldClass)
- `stdlib.h`, `stdio.h`, `string.h` (standard C libraries)
- `sys/types.h` (Unix) / `windows.h` (Win32) for networking types
- `ntohs`, `htons` (network byte order conversion)
- `MIN` macro (for buffer size comparison)
