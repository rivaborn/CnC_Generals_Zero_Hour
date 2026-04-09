# GeneralsMD/Code/Libraries/Source/WWVegas/WWLib/PALETTE.H - Enhanced Analysis

## Architectural Role
This file defines the core palette manipulation abstraction used throughout the SAGE engine's rendering pipeline. It bridges the low-level RGB color representation with the hardware palette system, critical for the engine's 256-color rendering mode.

## Cross-References
### Incoming
- Rendering subsystems (W3D) for color palette management
- UI components requiring palette adjustments
- Animation systems for color cycling effects

### Outgoing
- Directly depends on `RGBClass` from `rgb.h`
- Likely called by texture management and color conversion utilities

## Design Patterns
- **Facade Pattern**: Encapsulates complex palette operations behind a simple interface
- **Operator Overloading**: Provides intuitive access via `[]` and comparison operators
- **Resource Management**: Implicit ownership of palette data through conversion operators

*Not inferable*: No clear use of other patterns without implementation details.
