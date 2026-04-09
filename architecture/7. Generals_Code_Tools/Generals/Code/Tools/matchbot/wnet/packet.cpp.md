# Generals/Code/Tools/matchbot/wnet/packet.cpp

## Purpose
Handles packet serialization/deserialization for network communication in the matchbot tool.

## Responsibilities
- Parse incoming network packets into structured fields
- Serialize packet data into network transmission format
- Manage packet field list (addition, lookup, retrieval)
- Handle endianness conversion for cross-platform compatibility

## Key Types
- **PacketClass (Class)**: Main packet container managing fields and serialization
- **FieldClass (Class)**: Represents individual packet fields (not defined here)
- **bit8 (Type)**: Boolean-like type (likely typedef for char/bool)

## Key Functions
### PacketClass::PacketClass(char *curbuf)
- Purpose: Constructs a packet from raw network buffer
- Calls: ntohs, memcpy, FieldClass::Net_To_Host, Add_Field

### PacketClass::Create_Comms_Packet(int &size)
- Purpose: Serializes packet into network transmission format
- Calls: htons, memcpy, FieldClass::Host_To_Net, FieldClass::Net_To_Host

### PacketClass::Find_Field(char *id)
- Purpose: Locates a field by its ID in the packet
- Calls: strncmp

### PacketClass::Get_Field(char *id, [various types])
- Purpose: Retrieves field data of specific types (char, short, int, etc.)
- Calls: Find_Field

## Globals
None

## Dependencies
- **Includes**: stdlib.h, stdio.h, string.h, sys/types.h, windows.h (conditional)
- **External**: FieldClass, ntohs/htons (network byte order functions), memcpy, strncmp
- **Types**: unsigned short, short, long, unsigned long, unsigned, void*
