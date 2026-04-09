# Generals/Code/Tools/WW3D/max2w3d/resource.h - Enhanced Analysis

## Architectural Role
This file serves as the resource symbol definitions for the max2w3d tool, which is part of the WW3D (Westwood 3D) plugin suite for 3ds Max. It defines all UI elements, dialogs, and string resources used by the tool, acting as a bridge between the MFC-based UI and the underlying W3D export functionality.

## Cross-References
### Incoming
- Called by MFC dialog classes in the max2w3d tool (e.g., `w3ddlg.cpp`, `floaterdialog.cpp`)
- Referenced by resource compiler during build process

### Outgoing
- No direct outgoing references (declarative file)
- Symbols used by MFC runtime and Windows API

## Design Patterns
- **Resource Pattern**: Centralized resource definitions for UI consistency
- **Magic Number Replacement**: String IDs replace hardcoded strings in code
- **Not inferable**: No behavioral patterns visible in declarative file
