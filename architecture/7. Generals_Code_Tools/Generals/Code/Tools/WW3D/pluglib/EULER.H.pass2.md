# Generals/Code/Tools/WW3D/pluglib/EULER.H - Enhanced Analysis

## Architectural Role
This header defines the mathematical foundation for 3D rotation conversions in the WW3D plugin system, specifically bridging 3DS Max's coordinate system with the game engine's requirements. It's part of the asset pipeline tooling that enables artists to work in Max while ensuring proper orientation in the final game.

## Cross-References
### Incoming
- Likely called by Max plugin tools (e.g., max2w3d) for model orientation conversions
- Potentially referenced by animation exporters needing Euler angle representations

### Outgoing
- Uses `Matrix3` from `<Max.h>` for matrix operations
- Relies on Graphics Gems IV algorithms (external reference)

## Design Patterns
- **Facade Pattern**: Wraps complex Euler angle math behind a simple class interface
- **Strategy Pattern**: Different Euler order constants allow runtime selection of rotation convention
- **Data Transfer Object**: `EulerAnglesClass` primarily serves as a container for conversion results

*Not inferable*: No clear use of Observer or Factory patterns in this header-only file.
