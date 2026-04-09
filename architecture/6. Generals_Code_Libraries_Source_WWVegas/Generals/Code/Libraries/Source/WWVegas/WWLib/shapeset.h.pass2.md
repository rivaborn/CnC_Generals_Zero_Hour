# Generals/Code/Libraries/Source/WWVegas/WWLib/shapeset.h - Enhanced Analysis

## Architectural Role
This file defines the core data structure for 2D sprite management in the SAGE engine, serving as the foundation for all in-game visual assets. It bridges the gap between raw asset data and the rendering pipeline by providing optimized access to shape metadata and pixel data.

## Cross-References
### Incoming
- Rendering subsystem (uses Get_Data/Get_Rect for sprite batching)
- Animation system (queries Is_Transparent/Is_RLE_Compressed for optimization)
- UI framework (accesses shape dimensions via Get_Width/Get_Height)

### Outgoing
- Directly manipulates memory layout (pointer arithmetic in Fetch_Record_Pointer)
- Relies on Rect class for coordinate management

## Design Patterns
- **Resource Pool**: ShapeSet manages a collection of ShapeRecords with shared header
- **Flyweight**: Shape data is stored once but referenced by multiple game objects
- **Inline Accessors**: Performance-critical methods are inlined to avoid function call overhead

*Not inferable*: No clear use of Observer or Factory patterns in this header-only file.
