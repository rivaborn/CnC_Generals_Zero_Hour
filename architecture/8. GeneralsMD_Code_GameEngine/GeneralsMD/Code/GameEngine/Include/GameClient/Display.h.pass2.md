# GeneralsMD/Code/GameEngine/Include/GameClient/Display.h - Enhanced Analysis

## Architectural Role
This file defines the core graphics display interface, acting as a bridge between the game's rendering system (W3D) and higher-level game logic. It manages display attributes, view rendering, and UI elements like shroud/fog-of-war, while also handling video playback and debug visualization.

## Cross-References
### Incoming
- **DebugDisplay.h**: Uses `DebugDisplay::drawText` and `DebugDisplay::printf` for debug rendering
- **OSDisplay.h**: Likely uses `OSDisplayWarningBox` for display mode change warnings
- **TheScriptEngine**: Notified of completed videos via `m_currentlyPlayingMovie`

### Outgoing
- **View.h**: Manages attached views via `View *m_viewList`
- **GameFont.h**: Uses `GameFont` for cinematic text rendering
- **VideoBuffer/VideoStreamInterface**: Handles video playback buffers and streams
- **W3D Rendering System**: Implicitly interacts for actual drawing operations

## Design Patterns
- **Singleton Pattern**: `TheDisplay` provides global access to display functionality
- **Interface/Implementation Separation**: Pure virtual methods define the interface, allowing for platform-specific implementations
- **Callback Pattern**: `DebugDisplayCallback` enables modular debug display updates

*Not inferable: Exact W3D integration details or real-time rendering pipeline.*
