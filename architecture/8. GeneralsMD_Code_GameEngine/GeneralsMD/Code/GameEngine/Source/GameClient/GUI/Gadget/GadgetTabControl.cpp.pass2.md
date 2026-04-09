# GeneralsMD/Code/GameEngine/Source/GameClient/GUI/Gadget/GadgetTabControl.cpp - Enhanced Analysis

## Architectural Role
This file implements the tab control GUI component, serving as a container for multiple sub-panes that can be toggled via tab buttons. It integrates with the window management system to handle input, layout, and visibility of tabbed interfaces commonly used in the game's UI (e.g., build menus, options panels).

## Cross-References
### Incoming
- **Gadget system**: Calls `GadgetTabControlInput` and `GadgetTabControlSystem` as message handlers for tab control windows.
- **Window management**: `TheWindowManager` creates child windows and sends system messages to tab controls.
- **Game logic**: Likely invoked by UI screens (e.g., `GadgetBuildMenu.cpp`) that require tabbed navigation.

### Outgoing
- **Window system**: Uses `GameWindow` methods (`winGetSize`, `winSetPosition`, `winHide`) to manage sub-panes.
- **Memory management**: Directly allocates/deletes `TabControlData` during window creation/destruction.
- **Layout system**: Computes dimensions and positions for tabs/sub-panes based on parent window geometry.

## Design Patterns
- **Composite**: The tab control acts as a composite of sub-panes, managing their visibility and layout hierarchically.
- **Strategy**: Tab edge placement (top/bottom/left/right) is handled via conditional logic, effectively using a strategy pattern for layout.
- **Observer**: Sub-panes are notified (via `winHide`) when their visibility changes, though this is implicit in the window system.
