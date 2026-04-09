# Generals/Code/Tools/WW3D/max2w3d/FormClass.cpp - Enhanced Analysis

## Architectural Role
This file implements the UI framework for the max2w3d tool, providing a thin abstraction over Windows dialog creation and initialization. It bridges the tool's internal FormClass hierarchy with the Windows message loop, enabling resource-based UI construction.

## Cross-References
### Incoming
- Tool-specific UI classes (e.g., in max2w3d) inherit from FormClass and override Dialog_Proc
- Resource scripts (.rc) define dialog templates referenced by template_id

### Outgoing
- Directly calls Windows API (CreateDialogParam, SendDlgItemMessageA, etc.)
- Relies on Dllmain.H for AppInstance global
- Uses MFC-style dialog initialization resources (RT_DLGINIT)

## Design Patterns
- **Adapter Pattern**: Converts Windows messages into virtual Dialog_Proc calls, decoupling tool UI from Win32 specifics
- **Resource Pattern**: Uses Windows resources for UI definition, enabling externalization of dialog layouts
- **Property Pattern**: Uses SetProp/GetProp to associate FormClass instances with HWNDs (Win32-specific object association)

*Not inferable*: No clear use of Factory, Observer, or other patterns beyond basic OOP.
