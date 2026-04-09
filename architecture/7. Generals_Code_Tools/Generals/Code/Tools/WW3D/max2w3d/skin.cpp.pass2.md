# Generals/Code/Tools/WW3D/max2w3d/skin.cpp - Enhanced Analysis

## Architectural Role
This file implements the skinning pipeline for the Max2W3D exporter, bridging 3DS Max's skinning system with W3D's skeletal animation format. It handles bone assignments, vertex influences, and UI integration for the exporter tool.

## Cross-References
### Incoming
- **max2w3d/export.cpp**: Likely calls skin processing functions during W3D export
- **max2w3d/main.cpp**: Initializes skinning UI components
- **max2w3d/bone.cpp**: Uses bone selection and distance calculations

### Outgoing
- **3DS Max SDK**: Uses IObjParam, ICustButton for UI creation
- **max2w3d/skindata.h**: Accesses skin data structures
- **max2w3d/bpick.h**: Uses bone picker functionality

## Design Patterns
- **Bridge Pattern**: Separates skinning logic (SkinModifierClass) from UI (dialog procedures)
- **Factory Method**: Class descriptors create skinning objects/modifiers
- **Observer Pattern**: Dialog procedures react to UI events (WM_COMMAND)

*Not inferable*: Exact interaction with W3D export pipeline or bone hierarchy processing.
