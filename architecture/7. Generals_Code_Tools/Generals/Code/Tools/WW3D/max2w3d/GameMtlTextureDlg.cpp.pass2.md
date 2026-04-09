# Generals/Code/Tools/WW3D/max2w3d/GameMtlTextureDlg.cpp - Enhanced Analysis

## Architectural Role
This file implements the texture configuration UI for the Max2W3d exporter tool, bridging between 3ds Max's material editor and the W3D material system. It handles platform-specific shader differences (PC vs PS2) and synchronizes UI state with material properties.

## Cross-References
### Incoming
- Called by Max2W3d's material editor framework when texture configuration is needed
- Used by `GameMtl` class to display and modify texture properties

### Outgoing
- Calls into `GameMtl` class methods to get/set texture properties
- Uses 3ds Max SDK components (`IParams`, `ISpinner`, `ICustButton`)
- Accesses resource definitions from `resource.h`

## Design Patterns
- **Observer Pattern**: UI controls observe and update material properties
- **Adapter Pattern**: Bridges between 3ds Max UI components and W3D material system
- **Factory Pattern**: Creates appropriate dialog based on shader type (PC/PS2)

Rules followed. Output under 400 tokens.
