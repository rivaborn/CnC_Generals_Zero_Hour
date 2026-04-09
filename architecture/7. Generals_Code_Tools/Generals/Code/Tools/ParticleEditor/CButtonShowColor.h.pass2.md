# Generals/Code/Tools/ParticleEditor/CButtonShowColor.h - Enhanced Analysis

## Architectural Role
This file defines a UI component used in the Particle Editor tool, extending MFC's CButton to visually represent colors. It bridges the tool's color manipulation needs with Windows GDI color handling, likely used in particle effect configuration.

## Cross-References
### Incoming
- `WorldBuilder/src/CButtonShowColor.h` (duplicate header in another tool)
- Particle Editor UI code (uses color display buttons)

### Outgoing
- `RGBColor` class (for color storage)
- Windows GDI (`COLORREF` for system color conversion)
- MFC framework (`CButton` base class)

## Design Patterns
- **Adapter Pattern**: Converts between RGB and BGR formats to interface with Windows GDI
- **Template Method**: Overrides `OnPaint` to customize button rendering
- **Property Pattern**: Provides getter/setter methods for color manipulation

*Not inferable*: No clear use of Observer or Factory patterns in this header.
