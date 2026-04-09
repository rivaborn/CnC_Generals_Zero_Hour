# Generals/Code/Tools/WorldBuilder/src/CButtonShowColor.h - Enhanced Analysis

## Architectural Role
This file defines a UI component used in WorldBuilder's color selection interface, bridging the engine's color representation (RGBColor) with Windows GDI's BGR format. It's part of the tooling layer, not the runtime engine.

## Cross-References
### Incoming
- `ParticleEditor/CButtonShowColor.h` (duplicate class definition, suggesting code reuse or shared tooling infrastructure)
- Likely called by WorldBuilder's color picker dialogs or material editors

### Outgoing
- Depends on `CButton` (MFC) for base functionality
- Uses `RGBColor` (engine-defined type) for internal color storage
- Interfaces with Windows GDI via `COLORREF` for rendering

## Design Patterns
- **Adapter Pattern**: Converts between RGBColor and COLORREF (BGR) for Windows compatibility
- **Template Method**: Overrides `OnPaint` to customize button rendering while inheriting MFC behavior
- **Not inferable**: No clear use of other patterns (e.g., no factory, observer, or strategy visible)
