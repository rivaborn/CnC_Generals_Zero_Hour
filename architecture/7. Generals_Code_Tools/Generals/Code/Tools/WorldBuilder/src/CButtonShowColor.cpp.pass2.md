# Generals/Code/Tools/WorldBuilder/src/CButtonShowColor.cpp - Enhanced Analysis

## Architectural Role
This file implements a specialized UI control for the WorldBuilder tool, bridging the MFC-based UI layer with the game's color representation system. It handles color visualization and format conversion, serving as a utility for map editors to preview and select colors.

## Cross-References
### Incoming
- Likely called by WorldBuilder's UI dialogs that need color preview buttons (e.g., terrain/unit color pickers)
- May be referenced by other tool modules needing similar color display functionality

### Outgoing
- Uses MFC's GDI classes (CPaintDC, CPen, CBrush) for rendering
- Relies on CColor class (external) for color storage
- Calls Windows API (DestroyWindow) for resource cleanup

## Design Patterns
- **Adapter Pattern**: Converts between RGB/BGR formats to interface with Windows GDI
- **Template Method**: OnPaint() defines a rendering algorithm that subclasses could extend
- **MVC (View)**: Acts as the view component for color data in the WorldBuilder UI

*Not inferable*: No clear use of Factory, Observer, or Strategy patterns in this snippet.
