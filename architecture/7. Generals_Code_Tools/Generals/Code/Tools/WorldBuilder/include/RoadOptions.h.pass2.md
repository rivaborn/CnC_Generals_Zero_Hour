# Generals/Code/Tools/WorldBuilder/include/RoadOptions.h - Enhanced Analysis

## Architectural Role
This header defines the `RoadOptions` class, a UI component in WorldBuilder for configuring road properties. It bridges the terrain editing subsystem with the UI framework, handling road type selection, curve/angle settings, and applying changes to the heightmap.

## Cross-References
### Incoming
- **WorldBuilder UI**: Calls `RoadOptions` methods for road configuration dialogs
- **Terrain Editing**: Likely invoked by `WorldHeightMapEdit` for road property management

### Outgoing
- **UI Framework**: Uses MFC dialog mechanisms (`DoDataExchange`, `OnInitDialog`)
- **Tree View Control**: Manages `CTreeCtrl` for road type hierarchy display
- **Terrain System**: Applies road changes via `applyToSelection`

## Design Patterns
- **Singleton**: Uses `m_staticThis` for global access to the dialog instance
- **Observer**: Handles UI events (`OnTightCurve`, `OnAngled`) to update road properties
- **State Management**: Maintains static state variables (`m_currentRoadIndex`, `m_angleCorners`) for persistent road configuration

*Not inferable: Exact interaction with terrain system or bridge handling logic.*
