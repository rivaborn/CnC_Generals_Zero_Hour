# Generals/Code/GameEngine/Source/GameClient/GUI/GUICallbacks/ControlBarPopupDescription.cpp - Enhanced Analysis

## Architectural Role
This file implements the control bar tooltip system, bridging the UI layer with game logic. It handles dynamic tooltip generation for build commands, power/credit displays, and general UI feedback, with animation support for smooth transitions.

## Cross-References
### Incoming
- Called by `ControlBar` methods when tooltips need display/management
- Used by `InGameUI` for tooltip coordination
- Referenced in `GameWindow` event handling for hover states

### Outgoing
- Queries `GameLogic` for game state (replay, ending)
- Uses `BuildAssistant`/`UpgradeCenter` for affordability checks
- Leverages `DisplayStringManager` for text wrapping
- Interacts with `AnimateWindowManager` for fade/position animations

## Design Patterns
- **Observer Pattern**: Tooltips react to mouse events and game state changes
- **Strategy Pattern**: Different tooltip content strategies for buttons vs. static displays
- **Singleton-like Access**: Global `TheControlBar` pointer suggests centralized control bar management

*Not inferable*: Exact factory usage for `WindowLayout` creation.
