# GeneralsMD/Code/Libraries/Source/WWVegas/WW3D2/rddesc.h - Enhanced Analysis

## Architectural Role
This file defines data structures for render device abstraction in the SAGE engine's Direct3D 8 wrapper layer. It serves as the interface between the engine's rendering subsystem and hardware capability queries, enabling resolution management and device enumeration.

## Cross-References
### Incoming
- Likely called by `WW3D` and `DX8Wrapper` (declared as friends) for device initialization and capability queries
- Used by rendering initialization code to populate available resolutions

### Outgoing
- Depends on internal WW3D types (`DynamicVectorClass`, `StringClass`)
- Uses Direct3D 8 structures (`D3DCAPS8`, `D3DADAPTER_IDENTIFIER8`)

## Design Patterns
- **Data Transfer Object**: Encapsulates render device metadata for transfer between subsystems
- **Immutable Access**: Public getters with private setters enforce controlled modification
- **Composite**: `RenderDeviceDescClass` aggregates multiple `ResolutionDescClass` objects

*Not inferable*: No clear use of Factory, Observer, or Strategy patterns in this header alone.
