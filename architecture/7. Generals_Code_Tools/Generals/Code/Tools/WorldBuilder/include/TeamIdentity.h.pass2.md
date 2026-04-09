# Generals/Code/Tools/WorldBuilder/include/TeamIdentity.h - Enhanced Analysis

## Architectural Role
This header defines the UI layer for team configuration in WorldBuilder, bridging MFC dialog infrastructure with game-specific data structures (Dict, SidesList). It encapsulates team property editing functionality, serving as a specialized property page in the WorldBuilder toolchain.

## Cross-References
### Incoming
- Likely called by WorldBuilder's property sheet manager (e.g., `CPropertySheet`-derived class)
- UI event handlers (e.g., button clicks) from resource script (IDD_TeamIdentity)

### Outgoing
- Interacts with `Dict` and `SidesList` for data persistence
- Uses MFC's `CDataExchange` for DDX/DDV operations
- References `NameKeyType` (likely from game data system)

## Design Patterns
- **Property Page Pattern**: Inherits from `CPropertyPage` to integrate with MFC's tabbed dialog system
- **Dependency Injection**: Uses `setTeamDict()` and `setSidesList()` to decouple from concrete data sources
- **Command Pattern**: Event handlers like `OnUnitTypeButton()` encapsulate UI actions as methods (MFC-specific implementation)
