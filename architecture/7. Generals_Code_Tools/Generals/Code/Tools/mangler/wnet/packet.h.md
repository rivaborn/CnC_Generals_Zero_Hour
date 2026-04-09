# Generals/Code/Tools/mangler/wnet/packet.h

## Purpose
Defines the `PacketClass` for creating and managing network packets as linked lists of field entries.

## Responsibilities
- Manages a linked list of `FieldClass` objects representing packet fields.
- Provides methods to add, retrieve, and manipulate packet fields.
- Converts packet data to a linear COMMS API-compatible format.
- Supports packet creation from scratch or from existing data.

## Key Types
- **PacketClass (Class)**: Manages packet fields and their serialization.

## Key Functions
### PacketClass::Add_Field
- Purpose: Adds a field to the packet's linked list.
- Calls: `FieldClass` constructor (indirectly).

### PacketClass::Find_Field
- Purpose: Locates a field by name in the packet.
- Calls: None.

### PacketClass::Get_Field
- Purpose: Retrieves field data of various types by name.
- Calls: `FieldClass` methods (indirectly).

### PacketClass::Create_Comms_Packet
- Purpose: Serializes the packet into a linear buffer.
- Calls: `FieldClass` methods (indirectly).

## Globals
- None.

## Dependencies
- `field.h` (for `FieldClass`).
- `wlib/wstypes.h` (for basic types like `bit8`).
