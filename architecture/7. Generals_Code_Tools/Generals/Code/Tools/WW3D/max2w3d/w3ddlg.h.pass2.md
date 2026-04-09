# Generals/Code/Tools/WW3D/max2w3d/w3ddlg.h - Enhanced Analysis

## Architectural Role
This file defines the UI layer for the max2w3d export tool, bridging 3ds Max's SDK with the W3D export pipeline. It encapsulates dialog management and option validation for W3D asset export.

## Cross-References
### Incoming
- `max2w3d.cpp` (likely the main export tool driver)
- 3ds Max SDK (`Max.h`, `ExpInterface`)

### Outgoing
- `w3dutil.h` (for `W3dExportOptionsStruct`)
- 3ds Max SDK controls (`ISpinnerControl`)

## Design Patterns
- **Mediator**: Centralizes dialog state management and control interactions
- **State**: Uses enable/disable methods to manage UI state transitions
- **Strategy**: Different export formats (WHT/WHA/WTM) are selected via radio buttons with conditional UI updates

*Not inferable*: Concrete implementation details of event handlers or 3ds Max SDK integration.
