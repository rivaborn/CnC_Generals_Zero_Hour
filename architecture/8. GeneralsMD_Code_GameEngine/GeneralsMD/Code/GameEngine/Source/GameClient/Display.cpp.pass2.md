# GeneralsMD/Code/GameEngine/Source/GameClient/Display.cpp - Enhanced Analysis

## Architectural Role
This file implements the core display management system, acting as the bridge between the game's rendering pipeline and higher-level UI/logic systems. It handles view rendering, video playback, and display mode transitions, serving as a critical abstraction layer for the game's visual output.

## Cross-References
### Incoming
- **Debug Displayers**: AudioDebugDisplay and other debug modules register callbacks through `setDebugDisplayCallback`
- **Script Engine**: Likely triggers movie playback via `playMovie`/`playLogoMovie` (commented-out sync call remains)
- **UI System**: Shell/ingame interfaces call `draw` for rendering

### Outgoing
- **Video System**: Directly controls `TheVideoPlayer` for movie playback
- **Tactical View**: Adjusts dimensions via `TheTacticalView` during resolution changes
- **Text/Font Systems**: Uses `TheDisplayStringManager`, `TheGameText`, and `TheFontLibrary` for copyright displays

## Design Patterns
- **Singleton**: `TheDisplay` global instance ensures single display manager
- **Observer**: Debug display callbacks follow observer pattern for modular debug output
- **Resource Management**: RAII-like cleanup in `stopMovie` for video buffers/streams

*Not inferable*: No clear use of strategy pattern for view rendering despite `drawViews` loop.
