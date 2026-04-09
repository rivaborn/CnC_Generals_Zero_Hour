# Generals/Code/Tools/GUIEdit/Source/EditWindow.cpp - Enhanced Analysis

## Architectural Role
This file implements the core edit window for the GUI editor tool, serving as the primary interface for UI design in the SAGE engine. It bridges the Windows API with the engine's rendering and window management systems, handling input, rendering, and tool-specific functionality like grid alignment and control creation.

## Cross-References
### Incoming
- **GUIEdit.h**: Uses `TheEditor` singleton for mode management
- **HierarchyView.h**: Interacts with `TheHierarchyView` for window selection
- **Properties.h**: Initiates property dialogs via `InitPropertiesDialog`
- **GameClient/GameWindowManager.h**: Relies on `TheWindowManager` for window operations

### Outgoing
- **WW3D2/Render2D.h**: Delegates 2D rendering via `m_2DRender`
- **GameClient/Display.h**: Uses `TheDisplay` for line drawing (grid)
- **WW3D2/WW3D.h**: Synchronizes rendering with `WW3D::Sync/Begin_Render/End_Render`

## Design Patterns
- **Singleton**: `TheEditWindow` ensures single edit window instance
- **Observer**: Notifies editor of window deletions via `notifyWindowDeleted`
- **Command**: Popup menu actions (e.g., `newWindow`) encapsulate UI creation logic

*Not inferable*: Factory pattern for control creation (menu IDs suggest it, but implementation truncated).
