# Generals/Code/Tools/mangler/wnet/packet.cpp - Enhanced Analysis

## Architectural Role
This file implements the core packet serialization/deserialization logic for the Westwood Auto Registration tool's network layer. It bridges between raw network buffers and structured field data, handling endianness conversion and field management.

## Cross-References
### Incoming
- `Generals/Code/Tools/matchbot/wnet/packet.cpp` (uses `PacketClass` methods)
- Likely called by higher-level network managers (not shown in cross-references)

### Outgoing
- Directly uses `FieldClass` methods (`Host_To_Net`, `Net_To_Host`)
- Depends on standard C networking functions (`ntohs`, `htons`)

## Design Patterns
- **Composite**: `PacketClass` manages a list of `FieldClass` objects
- **Adapter**: Converts between network byte order and host byte order
- **Template Method**: `Get_Field` variants follow a consistent retrieval pattern

*Not inferable*: Exact usage context in Generals/Zero Hour (this appears to be from an older Westwood tool).
