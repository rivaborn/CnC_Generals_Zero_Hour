# Generals/Code/Tools/WorldBuilder/include/EditCoordParameter.h - Enhanced Analysis

## Architectural Role
This header defines a UI component for the WorldBuilder tool, specifically for editing coordinate-based parameters in the game's scripting system. It bridges the MFC-based dialog system with the game's internal coordinate representation (Coord3D), enabling level designers to modify spatial parameters.

## Cross-References
### Incoming
- Likely called by `EditParameter` (friend class) and other WorldBuilder UI components that need to edit coordinate values
- Part of the parameter editing framework in WorldBuilder

### Outgoing
- Uses `Parameter` from `GameLogic/Scripts.h` for script parameter handling
- Relies on MFC's dialog infrastructure (`CDialog`, `CDataExchange`)
- Interfaces with `Coord3D` type (likely from game math library)

## Design Patterns
- **MVC (Model-View-Controller)**: Separates coordinate data (model) from UI presentation (view) and input handling (controller)
- **Template Method**: Overrides MFC's virtual methods (`DoDataExchange`, `OnInitDialog`) to customize dialog behavior
- **Dependency Injection**: Receives `Parameter` pointer externally to operate on specific script parameters
