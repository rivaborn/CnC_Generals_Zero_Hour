# GeneralsMD/Code/GameEngine/Include/GameClient/WinInstanceData.h - Enhanced Analysis

## Architectural Role
This file defines the core data structure (`WinInstanceData`) for game UI windows, bridging the presentation layer (rendering, fonts) with game logic (state management, tooltips). It serves as the central container for window properties, enabling dynamic UI updates and state transitions.

## Cross-References
### Incoming
- **UI Rendering System**: Uses `WinDrawData`/`TextDrawData` for visual state management
- **Scripting System**: References `m_id` for script-driven window manipulation
- **Input System**: Relies on `m_state` flags (`WIN_STATE_HILITED`, `WIN_STATE_SELECTED`) for hover/selection logic

### Outgoing
- **DisplayString**: Delegates text rendering via `m_text`/`m_tooltip`
- **GameFont**: Uses `m_font` for text styling
- **Image/VideoBuffer**: Handles background images and video playback

## Design Patterns
- **Data Container**: Encapsulates all window-related data (text, images, state) for modularity
- **State Pattern**: Uses bitflags (`m_state`, `m_style`) to manage window behavior transitions
- **Composite**: `WinDrawData`/`TextDrawData` structs compose visual properties for different states (enabled/disabled/highlighted)

*Not inferable*: No clear use of Observer or Factory patterns in this header.
