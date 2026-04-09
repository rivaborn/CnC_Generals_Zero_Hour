# Generals/Code/Tools/mangler/wnet/packet.h - Enhanced Analysis

## Architectural Role
This file defines the core networking packet abstraction used by the mangler tool, which is part of the build pipeline for generating network protocol definitions. It bridges the gap between high-level packet construction and low-level COMMS API serialization.

## Cross-References
### Incoming
- `Generals/Code/Tools/matchbot/wnet/packet.h` (duplicate file in matchbot tool)
- Likely called by network protocol generation tools that need to construct packets

### Outgoing
- Directly uses `FieldClass` from `field.h`
- Produces output for COMMS API (external dependency)

## Design Patterns
- **Composite Pattern**: PacketClass contains a linked list of FieldClass objects, treating individual fields and the whole packet uniformly
- **Facade Pattern**: Hides COMMS API complexity behind simple Add/Find/Get methods
- **Template Method**: Overloaded Add_Field/Get_Field methods provide type-safe access to packet data

Rules followed. Output under 400 tokens.
