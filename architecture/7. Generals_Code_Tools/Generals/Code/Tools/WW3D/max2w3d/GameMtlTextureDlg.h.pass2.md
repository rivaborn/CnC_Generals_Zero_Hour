# Generals/Code/Tools/WW3D/max2w3d/GameMtlTextureDlg.h - Enhanced Analysis

## Architectural Role
This file defines the UI dialog for managing texture properties in the Max2W3D exporter tool, bridging 3ds Max's material system with the W3D format's texture stage requirements. It handles the presentation layer for texture stage configuration, working within the broader asset pipeline for game content creation.

## Cross-References
### Incoming
- Likely called by `GameMtl` class (parent material system) to display texture properties
- May be instantiated by the main Max2W3D plugin UI framework

### Outgoing
- Uses 3ds Max SDK components (`ISpinnerControl`, `ICustButton`)
- Inherits from `GameMtlFormClass` (local form base class)
- Interacts with `GameMtl` instance for property synchronization

## Design Patterns
- **MVC Pattern**: Separates texture property data (Model) from presentation (View) and dialog logic (Controller)
- **Composite Pattern**: Manages multiple texture stages (0 and 1) as sub-components with similar interfaces
- **Observer Pattern**: Likely updates UI when underlying material properties change (inferred from `ReloadDialog`)

*Token count: 198*
