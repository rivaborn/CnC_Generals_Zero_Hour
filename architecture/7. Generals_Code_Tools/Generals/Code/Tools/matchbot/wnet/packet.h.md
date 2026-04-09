# Generals/Code/Tools/matchbot/wnet/packet.h

## Purpose
Defines the `PacketClass` for creating and managing network packets as linked lists of fields.

## Responsibilities
- Manages a linked list of `FieldClass` objects representing packet data.
- Provides methods to add, retrieve, and serialize packet fields.
- Supports creation from raw buffers or empty initialization.
- Generates COMMS API-compatible linear packet data.

## Key Types
- **PacketClass (Class)**: Manages packet fields and serialization.

## Key Functions
### PacketClass::Add_Field
- Purpose: Adds a field to the packet's linked list.
- Calls: `FieldClass` constructor.

### PacketClass::Find_Field
- Purpose: Locates a field by name in the packet.
- Calls: None.

### PacketClass::Get_Field
- Purpose: Retrieves field data by name (various overloads).
- Calls: `FieldClass` methods.

### PacketClass::Create_Comms_Packet
- Purpose: Serializes the packet into a linear buffer.
- Calls: `FieldClass` methods.

## Globals
- None.

## Dependencies
- `field.h` (for `FieldClass`)
- `wlib/wstypes.h` (for `bit8`, `unsigned`, etc.)
