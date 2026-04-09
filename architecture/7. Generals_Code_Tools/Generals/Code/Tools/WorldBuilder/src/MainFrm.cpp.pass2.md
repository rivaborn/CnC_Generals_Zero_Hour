# Generals/Code/Tools/WorldBuilder/src/MainFrm.cpp - Enhanced Analysis

## Architectural Role
This file implements the main application window for WorldBuilder, serving as the central UI controller. It manages the MFC-based window hierarchy, toolbars, and editor panels while coordinating with the document/view architecture.

## Cross-References
### Incoming
- `CWorldBuilderDoc` calls `handleCameraChange` to update camera options
- `WbView3d` and other view classes likely trigger `showOptionsDialog` for tool-specific panels
- Auto-save timer events originate from the MFC framework

### Outgoing
- Directly manipulates `DrawObject` for brush feedback rendering
- Interacts with `CWorldBuilderDoc` for document state (auto-save, active views)
- Controls `LayersList` panel for layer management
- Uses MFC framework classes for window management

## Design Patterns
- **Singleton**: `TheMainFrame` provides global access to the main window instance
- **Command Pattern**: UI commands (brush feedback toggle, camera options) are encapsulated in message handlers
- **Mediator**: Coordinates between multiple UI components (toolbars, panels, views) without direct coupling

*Not inferable*: Exact factory usage for option dialogs or observer pattern for view updates.
