# GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdclassids.h - Enhanced Analysis

## Architectural Role
This header defines the core shader classification system for the W3D rendering pipeline, serving as the contract between shader definitions and their implementations. It enables runtime shader selection based on hardware capabilities and material requirements.

## Cross-References
### Incoming
- `GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shddef.cpp` (uses shader definition IDs)
- `GeneralsMD/Code/Libraries/Source/WWVegas/wwshade/shdimpl.cpp` (uses shader implementation IDs)
- `GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/render.cpp` (references shader types during material setup)

### Outgoing
- None (header-only, no external dependencies)

## Design Patterns
- **Type Object Pattern**: The separation of shader definitions (what) and implementations (how) allows for dynamic shader selection at runtime.
- **Enumeration as Contract**: The class IDs serve as a stable interface between shader creators and consumers, enabling extensibility while maintaining compatibility.
- **Sentinel Values**: `SHDDEF_CLASSID_LAST` and `SHD_CLASSID_LAST` facilitate iteration and bounds checking in shader management code.
