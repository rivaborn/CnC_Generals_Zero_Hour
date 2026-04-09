# Generals/Code/Tools/WorldBuilder/include/ImpassableOptions.h - Enhanced Analysis

## Architectural Role
This file defines a UI dialog for the WorldBuilder tool, specifically for configuring terrain impassability settings. It bridges the gap between the editor's UI layer and the underlying terrain system, allowing level designers to mark slopes as impassable for game units.

## Cross-References
### Incoming
- Likely called from WorldBuilder's main editor window or terrain editing context menus
- May be referenced by terrain property dialogs or map validation systems

### Outgoing
- Inherits from MFC's CDialog, using its message handling infrastructure
- Interacts with terrain rendering/preview systems via OnPreview()
- Relies on Real type from the engine's math utilities

## Design Patterns
- **Observer Pattern**: Uses MFC's message map for event-driven UI updates (OnAngleChange, OnPreview)
- **Data Validation**: ValidateSlope() enforces business rules (slope range clamping)
- **Resource-Based UI**: Uses IDD_IMPASSABLEOPTIONS resource ID for dialog layout

*Not inferable*: No clear use of Factory, Strategy, or Composite patterns in this header.
