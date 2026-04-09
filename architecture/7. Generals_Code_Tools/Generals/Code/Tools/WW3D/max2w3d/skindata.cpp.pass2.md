# Generals/Code/Tools/WW3D/max2w3d/skindata.cpp - Enhanced Analysis

## Architectural Role
This file is part of the MAX-to-W3D model conversion pipeline, handling serialization/deserialization of skinning data (vertex selections and bone influences) for 3D models. It bridges the 3DS Max plugin interface with the W3D model format.

## Cross-References
### Incoming
- Likely called by MAX plugin export tools (e.g., `max2w3d` exporter)
- Used by W3D model build pipeline tools

### Outgoing
- Depends on MAX SDK's `ISave`/`ILoad` interfaces
- Uses `BitArrayClass` and `InfluenceStruct` from WW3D toolchain

## Design Patterns
- **Chunked Serialization**: Uses MAX's chunk-based I/O for versioned data storage
- **Visitor Pattern**: `ISave`/`ILoad` interfaces imply a visitor-like approach to serialization
- **Data Locality**: Groups related data (flags, selections, influences) in named chunks for modular loading

*Not inferable*: Exact relationship with W3D model format or bone hierarchy handling.
